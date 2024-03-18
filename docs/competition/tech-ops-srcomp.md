# Tech Ops (SRComp etc.)

At the competition event we use "competition software" to record and manage the
state of the competition as well as various aspects of the event production.
This includes the timings and scoring of matches, controlling lighting & audio
around the arena as well as displaying relevant information to competitors &
volunteers around the venue.

We use the [_SRComp_](https://github.com/PeterJCLaw/srcomp/wiki) suite of tools
to achieve this.

The following links are useful entry points into SRComp's own documentation:

* [Competition Preparation][comp-prep] outlines the steps which are needed to
  set up for each year
* [Common Operations][common-ops] and the [`srcomp-cli` docs][srcomp-cli] for
  anyone working with SRComp at or before the event
* [Component Overview][component-overview] for anyone developing SRComp or
  things on top of it

We also have our own specific pieces which builds on SRComp:

* [SRComp Mixtape][srcomp-mixtape] -- a service which performs actions in
  response to events throughout a competition; this is used to control lighting
  and music around the arena
* [Competition website][competition-website] -- a sub site of our website which
  is dedicated to the competition and builds on SRComp's HTTP API; this also
  includes a replacement homepage used during the event, toggled via
  `enable_competition_homepage` in our main [ansible][srobo-ansible] config

## Preparation for a competition

### Compstate

Information for a given competition is stored in a [_compstate_][compstate].
This is a git repository containing configuration and data about the state of
the competition.

We host our compstates on GitHub, named `srYYYY-comp` (e.g:
[`sr2024-comp`][sr2024-comp]). Setup of each year's compstate is as documented
in SRComp's documentation on [Competition Preparation][comp-prep].

### Public Compbox

We host a public SRComp deployment at <https://srcomp.studentrobotics.org>. This
is an Ubuntu Virtual Machine configured with [srcomp-puppet][srcomp-puppet],
hosted within our VM hosting provider and suitably added to our DNS.

This machine is usually created with a low capacity spec and temporarily bumped
one or two rungs for the week around the competition. In recent years we have
created it shortly before the Virtual Competition and kept it live until a
couple of months after the main Competition event. This provides enough time for
the pages it powers to be used for that cycle, while keeping costs to a minimum.

### Venue Compbox

Within the venue we use a Raspberry Pi 3 Model B (typically part code
[`srL1CX`][inventory-srL1CX]), which is also configured with
[srcomp-puppet][srcomp-puppet]. This Pi and its power supply are stored together
in a cardboard box, itself is stored within the same RUB as contains the 3L RUB
([`sr1VU19`][inventory-sr1VU19]) which houses the Raspberry Pi 2011.12s that
have historically been the drivers for the various in-venue displays.

The venue compbox is typically given internal hostname `compbox.lan` or similar,
depending upon the internal TLD being used. Historically we included the year
number in the name, however this created unnecessary friction each year when
deploying related parts of the competition network.

Due to differences between Raspberry Pi OS and Ubuntu, preparation of the Pi
deployment of srcomp-puppet typically requires more effort than the public
deployment.

### Competition network

Within the venue we typically have an isolated computer network used to connect
the various Tech Ops devices. This network is hardwire as much as possible as
various aspects of our system depend are timing dependent and thus these
connections need to be reliable and very low latency.

For convenience of volunteers connecting to it we also offer a connection into
it via WiFi, typically SSID `SRNet`.


[common-ops]: https://github.com/PeterJCLaw/srcomp/wiki/Common-Operations
[comp-prep]: https://github.com/PeterJCLaw/srcomp/wiki/Competition-Preparation
[competition-website]: https://github.com/srobo/competition-website/
[component-overview]: https://github.com/PeterJCLaw/srcomp/wiki/Component-Overview
[compstate]: https://srcomp.readthedocs.io/en/latest/compstate.html
[inventory-sr1VU19]: https://github.com/search?q=repo%3Asrobo%2Finventory%20sr1VU19&type=code
[inventory-srL1CX]: https://github.com/search?q=repo%3Asrobo%2Finventory%20srL1CX&type=code
[sr2024-comp]: https://github.com/srobo/sr2024-comp/
[srcomp-cli]: https://srcomp-cli.readthedocs.io/en/latest/
[srcomp-mixtape]: https://github.com/srobo/srcomp-mixtape/
[srcomp-puppet]: https://github.com/PeterJCLaw/srcomp-puppet/
[srobo-ansible]: https://github.com/srobo/ansible/

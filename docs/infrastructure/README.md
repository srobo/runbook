# Overview

Student Robotics has a variety of infrastructure in order to support its mission.
This document aims to provide an outline of the general structure.

Currently our infrastructure as a whole does not have a designed owner, instead
individual pieces are looked after by volunteer Teams or just by volunteers who
have historically maintained them.

Since September 2021 SR has had an Infrastructure Team which is responsible for
maintaining the common aspects of the organisation's infrastructure. That team's
remit has signficant overlap with the services mentioned in this section, though
there are things mentioned here which other teams are responsible for.

## Website

Our website consists of a main public facing site at https://studentrobotics.org
as well as a collection of other sites which appear at various paths off the
root domain. This runbook is an example of such a sub-site, as are the
competitor-facing documentation which appears at [`/docs`][slash-docs].

These sub sites (and the main website itself) are hosted as GitHub Pages, with a
separate NGINX instance acting as a [reverse-proxy][reverse-proxy] to facade
these and other services onto the root domain. Currently we use Digital Ocean
for the hosting of our [infrastructure][infrastructure] as well as for DNS and
TLS termination. Our domains are registered with Namecheap.

[slash-docs]: https://studentrobotics.org/docs
[reverse-proxy]: https://github.com/srobo/reverse-proxy
[infrastructure]: https://github.com/srobo/infrastructure

### Competitor Services

During the competition, there are a number of [hosted services](./competitor-services.md)
which the competitors use. These have their own managed configuration and are
typically hosted for the duration of the *competition year* only.

### Competition Services

During the competition event we use the [SRComp suite][srcomp-suite] of tools to
help run the matches, including a VM to host a public-facing copy of the HTTP
API for use on the website.

[srcomp-suite]: https://github.com/PeterJCLaw/srcomp/wiki

## Development: GitHub

A lot of our collaborative work (including hardware and software development, as
well as general task management) takes place [on GitHub][git-and-github], within our
[`srobo`](https://github.com/srobo) organisation.

We also have a separate [`srobo-legacy`](https://github.com/srobo-legacy)
organisation which contains some archived git repositories that pre-date our use
of GitHub. Moving these over to the main organisation and de-duplicating the
repositories is an [ongoing project][legacy-repository-migration].

[git-and-github]: ../volunteering/git-and-github.md
[legacy-repository-migration]: https://github.com/srobo/tasks/issues/179

## Email, Documents: Google

For our email (`@studentrobotics.org`) accounts as well as document sharing we
use Google Workspace. Google Groups are used for various mailing lists.

## Mailing lists

For sending some batch emails we use Mailchimp and Google Groups.

For many of our mailing lists we compose the emails in the form of pull requests
to repositories on GitHub, enabling review & feedback before sending as well as
providing a history which acts as a wealth of templates for sending similar
emails in the future.

Some such repositories are:

* [team-emails](https://github.com/srobo/team-emails/): Emails to competitor teams
* [volunteer-emails](https://github.com/srobo/volunteer-emails/): Emails to volunteers from other volunteers

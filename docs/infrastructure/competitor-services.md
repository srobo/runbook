# Competitor Services

During the competition season, there are a number of hosted services which the
competitors use. These are [managed using `puppet`][server-puppet] to configure
a "competitor services" VM, typically within Digital Ocean.

[server-puppet]: https://github.com/srobo/server-puppet/

The services typically include:

**Forums**
:   A space which the competitors can use to chat with each other and with
    mentors and to ask for help with developing their robots.
    Historically we have used [PHPBB](https://phpbb.com), although for SR2021 we
    have moved to using Discord with a bot to [gate entry](discord-gated-entry).

**[IDE](https://github.com/srobo/srobo-ide/)**
:   A hosted web-based environment which allows competitors to develop code for
    their robots without needing to install anything on their own computers.

**User accounts**
:   User accounts are needed for access to the IDE and our self-hosted forums.
    We also host a [management interface](https://github.com/srobo/nemesis/) so
    that team-leaders can administer the user-accounts of their teams.

**Ticket access**
:   At the physical competition we gate entry through the use of tickets which
    competitors download from the website ahead of time.

**[Code submitter](https://github.com/PeterJCLaw/code-submitter/)**
:   For the virtual competitions, this is a mechanism for competitors to submit
    the code for their virtual robots.


[discord-gated-entry]: https://github.com/srobo/discord-gated-entry/

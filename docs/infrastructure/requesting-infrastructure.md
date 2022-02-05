# Requesting infrastructure

This page details the process for requesting new infrastructure. This aims to be
as lightweight as possible, while capturing all the information that's needed.

Unless otherwise noted, the way to request things is to contact the
Infrastructure Team by starting a new conversation thread in the
[`#infrastructure` channel][slack-infra] in Slack. Please ping
`@infrastructure-committee` to ensure that your message is seen.

In general you can expect a response within a couple of days (often much
sooner), though note that the team may not always be able to act on your request
for some time.

Requests for new infrastructure must be made by (or confirmed by) members of a
Team Committee.

Where infrastructure requests would incur additional spending (for example a new
machine from Mythic Beasts), you must include a reference to the line in the
Team's budget to which that spending would relate.

[slack-infra]: https://studentrobotics.slack.com/messages/infrastructure

## Container hosting

In the future the Infrastructure Team hope to offer a shared hosting platform
for small services. These services will need to be provided as Docker
containers, however the exact details (both technical and budgetary) of this
setup have not yet been worked out.

For now we encourage the use of containers for ease of deployment and the
Infrastructure Team can help in running the host machine, but note that you will
need to budget for your own machine for the containers to run on.

Think of this as the "contact our Sales team for pricing" option where the other
items listed here are much more "off the shelf" offerings, so please allow for
some discussion around how container hosting will work when planning your
services.

## GitHub

When requesting changes related to GitHub, please include the GitHub username of
the users affected (if applicable) as well as the names of any teams or repos
those people will need access to.

Note that in general you are encouraged to add individuals to teams and grant
teams access to repos (rather than adding individuals to repos) as this makes it
easier to maintain consistency.

## Google

**Note:** The Infrastructure Team do not yet have administrative access to
Google Suite, so account management requests must be made to the trustees
instead. The Infrastructure team will be taking this over at some point in the
future.

## Mythic Beasts

[Mythic Beasts](https://www.mythic-beasts.com/) are a hosting provider.

For new resources please include in your request:

- Kind of resource (VM, bare metal, DNS entry, etc.)
- Level of urgency
- Spec level (please use Mythic's order forms to determine what you want and use
  their terminology when making requests)
- Expected cost (as a check to help ensure the right options are selected)
- Purpose/name
- Operating System
- SSH keys for bootstrap access (or where to get them)
- Team budget line the resource relates to (if it has cost)

Please be aware that:

- it is your responsibility to manage the resource, including using a suitable
  configuration management solution
- the Infrastructure Team will retain access to the resource
- the Infrastructure Team will initially setup the resource in a secure manner
  and provide guidance on how to keep it that way, however it is your
  responsibility to ensure that the resource remains secure

# Machine Setup

This is a checklist of things for setting up a new machine in Mythic Beasts.
The target audience of this document is the Infrastructure Team.
Other volunteers should refer to the documentation on [requesting
infrastructure](./requesting-infrastructure.md#mythic-beasts).

## Checklist

* Create the machine (choose "Raise Invoice" for billing)
* Secure the OS
* Email Mythic to apply our sponsorship
* Add DNS entries

## Creating the machine

* Don't select "managed hosting", even if we want it.<br>
  As part of our sponsorship from Mythic Beasts we can request their [managed
  hosting](https://www.mythic-beasts.com/sales/managed) option. This can be
  applied when creating the machine, however doing so means waiting for them to
  create the machine before we can start using it. Instead we've found it easier
  to create the machine, set it up and then ask for them to add this on later.

* Use planned DNS name for the machine as the Service Name.

* Our servers are mostly in "sov", so putting other machines there is probably a good idea.

* Prefer the latest Ubuntu LTS unless there's a good reason to pick something else.

* No need to put anything in the other fields

* Choose "Raise Invoice" as the billing option

## Securing the OS

<!-- Updating this? Also update "Servers" in ./security.md -->

Exactly what is needed to secure a new machine will depend on its intended
use-case, operating system and other factors. In general though we expect that:

* the firewall will block everything that's not needed
* root SSH is disabled
* password SSH is disabled (i.e: keys only)
* individuals have their own user accounts

These are included for all machines configured via our [ansible config][srobo-ansible],
which also creates users for members of the Infrastructure Team.

## Applying our sponsorship

Once the machine is created, you'll then need to email Mythic's support asking
for them to apply our sponsorship to the new machine. Here's a typical email for
that:

Subject: "Student Robotics server '&lt;machine-name>'"
> Hi,
>
> I've just created a new VM '&lt;machine-name>' within Student Robotics' account (number &lt;number>).
> Please could you apply our sponsorship discount and discard the invoice.
>
> I've configured this machine without managed monitoring for now,
> however if it would be possible to apply that it to it (also as part
> of our sponsorship), that would be great.
>
> I'm in the process of configuring the machine with &lt;link to ansible or puppet>
> and can let you know when that's complete.
>
> Thanks,<br>
> &lt;name><br>
> Student Robotics volunteer

You should send this from the same email address you use for your Mythic user account.

You can get our account number from the UI once you've logged in (in the top
right, where it also shows your user id).

If we're not adding managed hosting then the paragraphs about configuring the
machine can be dropped.

## Managed hosting

If you also want them to apply managed hosting to the machine this can be
requested at the same time (as the above example does). Note that for managed
hosting they'll need password-less `sudo` access to the machine and to poke a
hole in the firewall for their monitoring systems to talk through.

If using our [ansible config][srobo-ansible] then the firewall rule is included
in the default firewall config for all machines.

Typically we set them up with a `mythic` user which has sudo access enabled.
They'll be able to provide the SSH key to allow access for -- it's a single one
for our account and is common to the similarly named account on our other
machines.

Mythic will need to know what services the machine will run and how they should
be monitored. You can include this upfront or wait until they've got set up.

### Shared wiki

There is an internal shared wiki which allows us to share notes with the Mythic
support team. It is linked from the My Account page in their UI. It can be
useful to put information there regarding what a given server is running and how
it's configured.

## DNS

Our forward DNS entries are managed in Digital Ocean.

Reverse DNS entries are managed in Mythic Beasts. We should add reverse DNS
entries for all machines, even if they don't have forward DNS.

Remember to add IPv4 as well as IPv6 entries if the machine has connectivity on both.


[srobo-ansible]: https://github.com/srobo/ansible/

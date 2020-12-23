# Overview

Student Robotics has a variety of infrastrcture in order to support its mission.
This document aims to provide an outline of the general structure.

Currently our infrastructure as a whole does not have a designed owner, instead
individual pieces are looked after by volunteer Teams or just by volunteers who
have historically maintained them.

## Website

Our website consists of a main public facing site at https://studentrobotics.org
as well as a collection of other sites which appear at various paths off the
root domain. This runbook is an example of such a sub-site, as are the
competitor-facing documentation which appears at [`/docs`][slash-docs].

These sub sites (and the main website itself) are hosted as GitHub Pages, with a
separate NGINX instance acting as a [reverse-proxy][reverse-proxy] to facade
these onto the root domain. Currently we use Digital Ocean for the hosting of
our [infrastructure](https://github.com/srobo/infrastructure) as well as for DNS
and TLS termination. Our domains are registered with Namecheap.

[slash-docs]: https://studentrobotics.org/docs
[reverse-proxy]: https://github.com/srobo/reverse-proxy

## Development: GitHub

Our hardware and software development takes place on GitHub, within our
[`srobo`](https://github.com/srobo) organisation.

We also have a separate [`srobo-legacy`](https://github.com/srobo-legacy)
organisation which contains some archived git repositories that pre-date our use
of GitHub. Moving these over to the main organisation and de-duplicating the
repositories is an [ongoing project][legacy-repository-migration].

[legacy-repository-migration]: https://github.com/srobo/tasks/issues/179

## Email, Documents: Google

For our email (`@studentrobotics.org`) accounts as well as document sharing we
use Google's G-Suite. Google Groups are used for various mailing lists.

## External mailing lists: Mailchimp

For sending some batch emails we use Mailchimp.

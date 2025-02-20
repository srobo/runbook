# Contributing to the runbook

Contributions to Student Robotics' Runbook should follow Student Robotics'
[Code of Conduct][code-of conduct] and made under a compatible [license][license].

You may also find the [Zen of Python][pep-20] provides useful guidance.

[code-of conduct]: https://opsmanual.studentrobotics.org/about-the-charity/code-of-conduct
[license]: https://github.com/srobo/runbook/blob/main/LICENSE
[pep-20]: https://www.python.org/dev/peps/pep-0020/

## Making big changes

As the runbook is a resource which expects to be read by a large number of
people, its current shape & content form a public API of sorts -- the way to
navigate it as well as the locations of much of the content are likely
muscle-memory to many contributors and readers. Making big changes to it
therefore needs careful consideration to ensure that their workflows are not
disrupted unduly.

It's a good idea therefore to raise any large changes as a [new issue][new-issue]
before committing to them.

Alternatively, if your change is more easily explained as a demonstration of the
outcome, it's fine to raise a pull request showing that. Note however that your
suggestion will still be discussed and may not be accepted, so you may wish to
focus on a small example of the change first.

[new-issue]: https://github.com/srobo/runbook/issues/new

## Work in progress

The runbook is very much a work in progress, in two distinct ways.

Firstly: the content here is never going to be "complete". There will always be
more that could be added or better ways to explain things. We prefer to have
content which is present and correct, even if imperfect, where that allows for
easier and faster contribution. This isn't to say we should be sloppy, but
rather that we shouldn't let perfect become the enemy of good.

Secondly: in a more practical sense a lot of the content here has been imported
from legacy documentation which had a very different approach. As a result,
there are a number of apparent conventions here that are not compatible with the
approach described in this contribution guide. In general you are encouraged to
follow the guidance in this document, even when working around existing pages
which do not.

## Structure

The runbook aims to be available to and welcome contributions from all
volunteers, regardless of their situation. As a result, the runbook is organised
into topics which relate to volunteers as a whole, rather than any specific
group.

This is a deliberate change from a previous approach where content was arranged
around the people who worked on specific areas. Unfortunately that approach lead
to isolated silos of information which varied wildly in their internal
structure, content approach, utility and discoverability. While the runbook was
pulled together from a number of those sources (and may have sections which are
show that heritage) it aims to be topic-oriented.

## Content Guidance

The runbook aims to document all the information which a volunteer might need,
without substantially duplicating information which is better served as
documentation closer to the thing it documents. For example, the runbook does
not contain detailed information about using the [SR Tools][srtools] suite of
tools, though may indicate places where those tools should be used.

The [runbook's homepage][home] has some additional commentary about this.

[srtools]: https://srtools.readthedocs.io/en/latest/
[home]: ../README.md

### Record reasons

Aim to record the reasons why things happen, because:

* this provides context for a task or behaviour, which generally leads to better understanding
* this makes it easier to understand when a thing is outdated or no longer relevant
* this removes the need to re-learn why a thing is important

### Avoid dead ends

For any processes, try to ensure there are no dead ends.

For example: if we need to contact someone about something, ensure the person
being contacted will have the ability to resolve the situation rather than
themselves needing to contact someone else. (Note that contact-by-proxy is ok,
as long as the eventual recipient meets the preceding criteria)

This does _not_ mean that the runbook needs to exhaustively document all
possible outcomes! For example: it may be the case that someone needs to use
their judgement to resolve something. In that case it would be reasonable for
the runbook to document that that's the case.

### Disambiguate year-specific concerns

For anything which is specific to a single year, ensure that it's either clearly
marked as such. One way to achieve this is with headings, though for anything
non-trivial consider whether somewhere else is a better place for it. Having a
separate file prefixed by e.g: sr2019 is a good way to mark this sort of thing.

### Reference existing documentation

For any tooling, software, hardware or the like it's a good idea to reference
its own documentation (rather than duplicating it). This applies to our own tools
as well as third party ones.

However, It's a good idea to provide a brief guide towards applicable usage
where that will be helpful to the reader.

If struggling to express what you want to say within a brief guide, consider
contributing to improved upstream documentation!

## A note on links

`mkdocs` has the power to resolve and validate links, however only when they're
in a specific format. Links to pages inside the runbook should be relative, and
end with the `.md` file extension (ie `[some other page](./tasks.md)`
produces [some other page](./tasks.md)). This way, `mkdocs` will
correctly validate these links. Links which don't follow this format are not
validated.

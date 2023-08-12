# Security

!!! note
    This page is about digital & information security.

We take security considerations very seriously.
If you have any concerns please contact the Infrastructure Committee in the
first instance or the Trustees.

## Multi Factor Authentication

[Multi-factor authentication][wikipedia-mfa] (MFA) offers improved
authentication when accessing online accounts by requiring that the user provide
stronger proof of their identity before accessing an account.

All volunteers are encouraged to make use of multi-factor authentication on all
platforms which support it. Volunteers in positions of responsibility are
strongly encouraged to do so and should discuss with the Infrastructure
Committee any cases where this is impractical.

Useful links:

- [Discord two factor authentication](https://support.discord.com/hc/en-us/articles/219576828-Setting-up-Two-Factor-Authentication)
- [GitHub two factor authentication](https://docs.github.com/en/authentication/securing-your-account-with-two-factor-authentication-2fa/about-two-factor-authentication)
- [Google two factor authentication](https://support.google.com/accounts/answer/185839)
- [Mythic Beasts two factor authentication](https://www.mythic-beasts.com/blog/2020/01/27/two-factor-auth-totp-now-available/)
- [Slack two factor authentication](https://slack.com/intl/en-gb/help/articles/204509068-Set-up-two-factor-authentication-Set-up-two-factor-authentication)

[wikipedia-mfa]: https://en.wikipedia.org/wiki/Multi-factor_authentication

## Servers

<!-- Updating this? Also update "Securing the OS" in ./machine-setup.md -->

Exactly what is needed to secure a given server will depend on its intended
use-case, operating system and other factors. In general though we expect that:

* the firewall will block everything that's not needed
* root SSH is disabled
* password SSH is disabled (i.e: keys only)
* individuals have their own user accounts

These are included for all machines configured via our [ansible config][srobo-ansible],
which also creates users for members of the Infrastructure Team.

[srobo-ansible]: https://github.com/srobo/ansible/

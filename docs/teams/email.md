# Emailing Teams

The primary communication method between Student Robotics and team leaders is in the form of emails. An archive of emails sent to team leaders exists in the [`team-emails`](https://github.com/srobo/team-emails) repository.

Each year, a new mailing list is created to send emails to teams for a specific year. The Potential Team Leaders mailing contains all team leaders, and is used when announcing the start of a competition year.

## How to send an email:

Emails should be written in markdown, and committed to the [`team-emails`](https://github.com/srobo/team-emails) repository. The location of the file should represent which competition year the email is regarding, and when you expect it to be sent (this doesn't need to be accurate).

1. Write your email
2. Clone the repository. If you don't have push access to the repository, you'll need to fork it and clone your fork
3. Create a new branch for your email
4. Save your email in the relevant location (eg `SR2020/SR2020/2019-08-31-announce-SR2020.md`)
5. Add in the required `to` and `subject` metadata for the email
6. Open a PR with your new branch against `master` ([example](https://github.com/srobo/team-emails/pull/24)), noting why it's being sent, and recommending reviews
7. Await review, amend email if necessary.
8. Once the email has been approved, someone with the access to the mailing lists will send it, and then merge the PR

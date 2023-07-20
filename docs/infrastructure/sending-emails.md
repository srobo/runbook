# Sending emails

Student Robotics sends various emails to volunteers and team supervisors.

Emails may be sent a few different ways, depending on how the mailing list is managed.

| Mail list | Description | How to send |
|-----------|-------------|-------------|
| Potential Team Supervisors | Anyone who has [expressed an interest](https://studentrobotics.org/compete/) in running a team. They may or may not have competed before | Mailchimp |
| Team supervisors for a specific competition year | The supervisors for teams competing in a given year | GMail |
| Potential volunteers | Anyone who has [expressed an interest](https://studentrobotics.org/volunteer/) in volunteering | Mailchimp |
| "Active" volunteers | Active volunteers (those with `@studentrobotics.org` accounts) | GMail |
| SR(A)WN subscribers | Those interested in reading [SR(A)WN](../volunteering/srawn.md) | Google Groups |

## Drafting content

Emails sent to team supervisors and volunteers are stored in GitHub repositories, allowing their content to be reviewed, to easily look back at historical communications, and potentially copy wording for future use.

- [Team emails](https://github.com/srobo/team-emails)
- [Volunteer emails](https://github.com/srobo/volunteer-emails/)

Before an email is sent, it should be reviewed.

1. Write your email, in [markdown](https://guides.github.com/features/mastering-markdown/)
2. Fork the relevant repository, and open a pull request with your changes. The file should be named based on the expected send date, in a directory corresponding to the competition cycle year.
3. Request the PR be reviewed. Either by using the 'Reviewers' functionality in GitHub, or by sending a message in Slack.
4. Confirm there aren't any other emails planning to be sent soon
5. Once the PR is approved, request it be sent. Currently, this is a manual process. Once sent, merge the PR.

You will need some front-matter at the top of your markdown file to add some extra information, such as:

```yml
---
to: All Volunteers
subject: Help us run Kickstart 2023!
---
```

## Sending emails

The process for sending an email will vary depending on where the mailing list is held

### Mailchimp

We use Mailchimp to power the public sign-up forms on our website.

The Mailchimp account we have is very old, and on a legacy plan. Upgrading would limit the number of users we could have, so we stay on the legacy tier.

!!! note
    Only a few volunteers have access to Mailchimp. If you need to send an email, follow the below process, and reach out to the Competition or Marketing teams once the email is ready to send.

#### 1. In the sidebar, create a "campaign" of type "regular email"

#### 2. Populate the metadata

| Field | Value |
|-------|-------|
| To | The required mailing list |
| Send to | "All subscribers in audience" |
| Personalize the "Send to" field | Checked |
| Merge tag | "\*\|FNAME\|\* \*\|LNAME\|\*"
| From / Email Address | Whoever the email should come from (eg `teams@`, `competition-team@` etc) |
| Subject | From your email content |
| Preview text | blank |

#### 3. Design the email

Next to "Content", select "Design email"

In the resulting popup, select "Classic Builder"

!!! note
    Classic builder is Mailchimp's legacy builder, but is the one with our branded template

When prompted to select a template, click the "Saved templates" tag and choose "Student Robotics". The preview should contain "I love Titles.".

In the builder, change the "I love Titles." text with your subject.

In place of "Text goes here", enter your email content. When copying from GitHub, it's best to use the rendered preview (of the file, not the diff), rather than manually reformatting the content in Mailchimp.

!!! tip
   If your email calls for an explicit Call To Action, consider using the Button block to make the link more prominent

Once your content is in place, click "Continue" in the top right. A preview of the finished email can then be seen on the right.

!!! note
   All the placeholder content in the footer will be replaced automatically

#### 4. Send the email

Once all sections have been completed, click "Send" in the top right. A popup will appear confirming the recipients.

### Gmail

Sending an email through GMail is much easier than [Mailchimp](#mailchimp).

Sending Student Robotics related emails **must** be done using your Student Robotics Google account.

#### Multi-send mode

To ensure email deliverability, and prevent leaking addresses, we use GMail's ["multi-send mode"](https://support.google.com/mail/answer/12921167) to do mail-merge.

To enable multi-send mode, click the corresponding button at the bottom of the Compose modal.

Multi-send mode is not necessary when sending emails to a group, such as "Active" volunteers.

#### 1. Select recipients

The email needs to be sent to people, so grab their email addresses.

For team supervisors from a specific competition year, these can be found in the relevant "Teams Organisation" sheet. Be sure to exclude teams who have dropped out if required.

For "Active" volunteers, simply enter `volunteers@studentrobotics.org`.

#### 2. Select the "From" address

Sent emails should rarely come from your individual address. Exactly who it should come from will vary on the sender and target audience of the email.

!!! tip
    If you're the member of a group, you can [send emails as that group](https://support.google.com/googlecloud/answer/10635789).

#### 3. Add your content

Enter your email content in the body of the message, and the subject in the subject field. When copying from GitHub, it's best to use the rendered preview (of the file, not the diff), rather than manually reformatting the content in GMail.

You can also remove the automatically-created "Unsubscribe" link, as it's not relevant to our use case.

#### 4. Send the email

Once the email is ready, click "Send". A popup will appear confirming you're happy with no "Unsubscribe link" (you are), and whether you want to send a test email (personal preference).

## Replies

Chances are, someone will reply to the email asking for follow-up, especially in the case of Team Supervisors. `teams@` in particular receives many questions from supervisors.

When sending a reply, be sure to reply [as the group](https://support.google.com/googlecloud/answer/10635789), and CC in the group itself so others can see what you sent.

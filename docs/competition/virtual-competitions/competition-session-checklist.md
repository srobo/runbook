# Competition Session Checklist

This checklist enumerates the tasks that need to be completed to run a virtual competition session with a module announcement.

## Pre Event

- Advertise the code submission deadline to teams
- Create the YouTube livestream
- Update the event page on the website with the correct livestream URL
- Update the compstate with the correct livestream URL
- Create a folder for session uploads in Google Drive
- Create a presentation detailing the new module
- Assign roles for this session
    - Match Runners - Run the simulations of the matches
    - Presenters - Present and commentate the livestream
    - Producer - Runs the technical aspects of the livestream
    - Scorer - Updates the compstate with match files
    - Chat Mods - Monitor the livestream and Discord chats
- Check for any new dropouts and update the compstate as necessary
- Check that the `@commentators` group in Slack points at the right people
- Presenters prepare a scripted introduction to the session
- Revise the rules for the new module
- Update the simulator for the new module in the private repo
- Draft a post-event website article with details of the new module (any game sensitive content to be reviewed via Google Drive)
- Set a volunteer start time for the day of the live stream (10am seems to work well for livestreams happening around lunchtime)

## After the Code Submission Deadline

- Download the team code at the deadline
- Negotiate with teams and handle any late submissions
- Check for any no-shows
- Construct the league for the session
- Import the league into the compstate

## Match Running

- Get a copy of the updated compstate
- Run the simulations
- Post-process the animation files to work around <https://github.com/cyberbotics/webots/issues/6426>
- Upload the entire output to our Google Drive Folder

## Scoring & Production Prep

- Score the matches
- Identify things of interest, capture screenshots & videos, prepare a document describing these for the producer
- Prepare a document with summaries of previous/next match and notes for the commentators

## Pre Go Live

- Check the compbox services (SRComp etc.) are still running
- Create and set thumbnail for the livestream
- Put the website into competition mode
- Producer downloads the recordings and configures the video scheduler to find the files correctly
- Producer downloads the screenshots & videos of things of interest
- Scorer downloads the match score files
- Presenters rehearse any presentations they need to give
- Presenters join a pre-livestream call to rehearse their interactions

## Go Live

- Presenters present
- Scorer deploys the match files to the compstate as they are broadcast
- Scorer copies match summaries into Slack `#livestream` for the commentators as the matches are broadcast
- Chat Mods to monitor chat and forward on any relevant messages to presenters or producer via Slack (the `@commentators` group may be useful for this)

## Module Announcement

- Present the prepared presentation
- Chat Mods collect questions from the livestream and Discord then paste into a Slack channel
- Available volunteers comment on questions (in threads) with any answers or thoughts
- Presenters read the questions, any answers in the thread, and add their own comments
- Release the rules
- Release the simulator update
- Publish the prepared website article with the module announcement
- End the livestream

## Post Livestream

- Archive the livestream so that it can be watched as a Video on Demand (VOD)
- Cut down the VOD on YouTube to remove the countdown
- Add chapters to the VOD
- Distribute logs and animation files to teams
- Schedule a Retro after a brief break
- Announce the final scores, VOD, and next competition time to the teams
- Revert the website back to non competition mode

## Retro

- Have a Retro
- Record actions to be taken

## Post Retro

- Plan next event

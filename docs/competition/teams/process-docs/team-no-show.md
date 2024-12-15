# No-show Teams Process

This process outlines how we detect and respond to teams who do not arrive at the competition event.

This process is ultimately part of Team Support at the venue, though is likely to be delegated to another volunteer rather than run by the Team Support Area Owner.
The person running this process is referred to as the "No-show-teams volunteer".

We expect teams to have all arrived in time for the opening ceremony, so if any teams aren't present when that starts Saturday we consider them no-show and reach out to them.
The overview of this process is:

* Contact the missing teams
* Record whether or not they're coming
* Inform the Match Ops Area Owner, who will
    * decide if and how this affects the match schedules
    * disseminate the information to those who need it

This is run *twice* on Saturday -- once when the opening ceremony starts and again 20 minutes before the start of the first match.
It is assumed that there will be about an hour between those two times; if that is not the case this process may need updating.

It is also run once on Sunday, however drop-outs at that stage are unlikely.

!!! note
    On each day, after the process has been run then reception must switch to actively informing the Match Ops Area Owner of any teams which arrive as they arrive (rather than simply logging that fact and waiting for the Area Owner to look it up).

## Contacting the missing teams

* Compare actual arrivals to those expected, identifying those missing.
  For SR2025, the actual arrivals are stored in the Helpdesk system and the expected arrivals are in the Teams Organisation (internal) Google Sheet.

* Check in Discord and on teams@ to see if they've posted that they're on their way & running late; ignore those teams for now.

* Phone the supervisors for any which are missing.
    * If you get through, explain who you are (first name, volunteer for SR) and why you're calling (just checking they're on their way, how's their travel going, do they have an ETA).
      If the team are dropping out, be clear that this needs to be definite and they will be unable to compete if they were to arrive. We would prefer to leave them as a "maybe" if they might still arrive.
    * If you don't get through, leave a voicemail and invite them to get back to us (ideally a phone call).
      TODO: can we have a phone number for the venue so we don't need to give our volunteers' own numbers?

## Record whether or not they're coming

Make notes of the call and classify teams into one of: on their way, left voicemail, dropped out.
For SR2025, this will be recorded in the Helpdesk system.

If the team confirm they aren't coming we will update the compstate to mark them as such. This is handled by the Competition Software Coordinator and typically means either:

* Deleting the team from the compstate, if they haven't had any other interactions in the compstate, or (more likely)
* Marking them as `dropped_out_after` the last match of the previous stage of the competition -- probably the Virtual League if there was one, or match `-1` if there are no prior matches

!!! warning
    This is very hard to undo once matches start, so only mark them as dropped out if the team explicitly confirm they're not coming.

## Decide if and how this affects the match schedules

If there are lots of dropouts and matches haven't started and we have a ready-to-go schedule for the reduced number of teams we should swap to that, to avoid lots of gaps in matches. This is only worthwhile if the number of such teams is more than two, but somewhat depends on how the match schedule looks.

In general we would only change the schedule after the first round of calls on the first day of the competition.
Changes to the schedule after the second round are expected to be too close to matches and would be disruptive.
On later days, the schedule cannot easily be changed as doing while preserving the fairness of the matches in aggregate is very difficult.

## Disseminate the information to those who need it

Once the status of the relevant teams have been established and any changes to the competition schedule have been decided, the Match Ops Area Owner will
inform:

* the Competition Software Coordinator, who will implement the necessary changes in the compstate, and
* the (current shift) Head Shepherd, who will pass the information on to their shift and include it in their handover when shifts change

Other roles will have access to this information via Helpdesk, which is coordinating the other affected activities and has access to the system recording the status of teams.

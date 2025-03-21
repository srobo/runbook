---
original:
  authors: Richard Barlow
  url: https://bitbucket.org/richardbarlow/sr-comp-team-support-coord/wiki/Helpdesk
---
# Helpdesk

Helpdesk is the teams' primary source of support. Volunteers are expected to advise teams in a similar fashion to mentoring - that is they should not tell teams what to do, but offer advice and guidance. The volunteers also help with kit related issues that may or may not be caused by a problem with the kit. It is the responsibility of the Helpdesk volunteers to assess teams' problems and, if necessary, swap out bits of kit hardware. In some situations teams may need to be put in contact with a person with more in-depth knowledge of the kit to help diagnose and fix issues.

## Equipment

* Physical copies of the rules
* A physical copy of this document
* Spare kit in the 'spare kit box'
* Broken kit box
* Red insulating tape (to mark broken kit)
* Permanent marker
* Large post-it notes
* Radio
* Spare robot flags for teams to borrow to try for size (must not leave helpdesk)
* Spare robot flag pipe fittings to give to teams

### Documents

* Kit Swap Forms
* Overnight Battery loan form
* Safety inspection forms
* Regulations inspection forms
* Tinker time schedule
* Kit return forms
* Kit return list
* Missing Kit forms

Some of these may be physical documents, and others may be [linked to from the helpdesk system](./helpdesk-system.md#links).

## Volunteer Requirements

At least one volunteer on Helpdesk must have prior experience of the use of the Student Robotics kit.

It's recommended that all helpdesk volunteers have a laptop or tablet to access the [helpdesk system](./helpdesk-system.md), docs and other online resources. The system can be used from a smartphone.

## Procedures

Almost all of Helpdesk's operations are covered by the following procedures.

### Handling of all requests

Whenever a team comes to Helpdesk with an issue that cannot be solved instantly, create a [ticket](./helpdesk-system.md#tickets). This ensures that no problems get dropped while they are being investigated. When the issue is resolved the ticket will be closed.

### Robot safety checks

The robots require safety checking before they are allowed to compete in the competition. Teams must not be given a battery until their robot has passed the safety check procedure. Helpdesk volunteers should perform a safety check according to the safety checklist (linked in the helpdesk system) and record the result.

Regulations checks will be done by [other volunteers](./regulations-inspector.md) visiting a team in their pit. Helpdesk volunteers do not need to do regulations checks, but may need to answer questions.

### General robot development queries

Many teams will come to Helpdesk requesting help with the development of their robot or, more likely, help using the Student Robotics kit and associated software. As mentioned earlier, Helpdesk volunteers are not expected to tell teams what to do, but rather offer advice. Helpdesk volunteers should strive to answer questions about the use of the kit and software.

Some queries may require a volunteer to visit the team in their pit to observe behaviour in situ. This must only be done by a Helpdesk volunteer if it will leave no fewer than two volunteers actively manning Helpdesk.

In some rare situations it may be necessary to request the assistance of a person with more in-depth knowledge of the kit to help solve an issue. Escalate the issue to the head helpdesker.

### Suspected damaged kit

If a team comes to Helpdesk with a suspicion of some of the Student Robotics kit being damaged then the following procedure should be followed:

 1. Request that the team take a freshly charged battery and see if the problem persists.
 1. Request that the team tries swapping the USB and power cables to the device in question, where applicable.
 1. If the kit contains multiple of the device in question (e.g. USB hub, motor board), request that the team tries swapping it with the other one in the kit.
 1. Request that the team tests the device in question with a very simple code project that only attempts to control that one device.
 1. If all previous steps indicate that the device is probably faulty then continue with the kit swap procedure.

#### Swapping out kit

After determining that a piece of kit is most likely faulty it must be swapped with a working spare. Helpdesk has a supply of spare kit. To swap a piece of kit please fill in a Kit Swap Form (linked in the helpdesk system) and follow the instructions on there.

Since there is a limited quantity of spare kit, all attempts must be made to verify that the issue being observed is not caused by something else. However, since issues may prevent a team from testing or competing, we should avoid debugging our own kit where possible, instead replacing a component and debugging it later.

### Swapping out batteries

See [Battery charging](./battery-charging.md#swapping-a-teams-battery-helpdesk)

### Requests for batteries / chargers / bags on Saturday evening

See [Overnight battery loan](./overnight-battery-loan.md).

### Flag fittings

Teams may request a pipe connector to use on their robot for the purpose of attaching the robot flags. As we have a limited supply, make sure that you only let each team only take one, so that they can't keep coming back for more.

Also, please show teams how to remove the fittings, as they are very strong and need to be released in the correct way (Press down on the center ring)

Also on helpdesk is an example flag teams can use to test their mounts. These example flags should not leave helpdesk.

### Team name changes

Teams are allowed to request that the name on the scoreboard is changed. This is an action that needs to be performed by a volunteer that is trained to use the SRComp software or GitHub repository.

Changes of name should be reviewed by the team supervisor before being actioned, to ensure the change is accepted by the entire team.

!!! note
    The name is the name of their "team" not the name of their "robot".

### Teams leaving early

If a team wishes to leave early, they must [return their kit](./kit-return.md) to helpdesk.

If a team wants to leave before the knockouts begin, contact the Event Coordinator.

### Booking tinker time

See [Tinker time](./tinker-time.md#booking-slots).

## Frequently Asked Questions

Based on issues handled in previous years, the following may be helpful:

| Key phrase | Resolution |
|------------|------------|
| Need to initialise servos to non-zero position | Use [Custom Robot Object Initialisation](https://studentrobotics.org/docs/programming/robot_api/#custom-robot-object-initialisation) and set position between `Robot(wait_for_start=False)` and `.wait_start()`. |
| How to access starting corner/zone number in code | Use `robot.zone` (On 'Programming / Robot API' page of docs in the 'Other Robot Attributes' section) |
| Where can I find out when my matches are | On our website: [studentrobotics.org](https://studentrobotics.org) |

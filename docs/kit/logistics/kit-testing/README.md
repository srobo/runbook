# Kit Testing

Prior to SR2025, Kit Collation and Kit Testing were separate events.
From SR2025, we have combined the two events to reduce the number of times that volunteers need to travel for kit events over the summer.
The key improvements that have allowed for this are the increased automation of the test scripts and the included functionality of recording board asset codes during testing.
This allows for the removal of the manual collation step.

All the automated test scripts are included in the [kit-test-scripts package](https://github.com/srobo/kit-test-scripts).
This can be installed through pip:

```bash
pip install sr-kit-test
```

## Preparation

Prior to starting, some preparation of the work area is required.
You will want 4-8 clear tables to work on.
This is to allow space to separate out and group the items of the kit.

First empty out all the boxes containing kits and create piles of each item in the kit.
The entire testing process focuses on individual elements of the kit so multiple different parts of the kit can be tested in parallel.

The final part of preparation is allocating the boxes things will end up in.
For this you will want:

- A box for each each of the items in the kit, they will be placed in this box after passing the functionality test.
- A box for items that failed the functionality test.
- A box for items that have damaged cases.

!!! note

    A single box can contain more than one type of item (i.e. boards and servo boards) but all of one type of item should be in a single box.

## Testing Steps

The processes of testing and collation are encapsulated by the following 4 steps.

- [Functional test](#functionality-tests) - Test each part functions as we expect and record each part's asset code for automated collation.
- [Visual inspection](#visual-inspection) - Visually inspect each part for damage.
- [Cleaning](#cleaning) - Clean off any adhesive residue.
- [Casing repairs](#case-repairs) - If there is remaining time, attempt to fix some broken cases by recovering parts from other failures.

## Functionality Tests

The first step that each item will go through is the functionality test to confirm that all the elements of the device are still functional and record the location of the item.
For certain (primarily non-electronic) items we do not have a test for and do not inventory the items.
Instead these items are simply counted and the total count recorded.

Below lists the tests to carry out for each element of the kit and notes any items that must be inventoried by scanning their asset tags rather than automated means.
Any new items that are added to the kit should also be added to this table as the testing for them is decided.

Item | Testing Step
--- | ---
Brain Board | [Automated Brain Board test](./test-procedures.md#brain-board)
Power Board | [Automated Power Board test](./test-procedures.md#power-board)
Motor Board | [Automated Motor Board test](./test-procedures.md#motor-board)
Servo Board | [Automated Servo Board test](./test-procedures.md#servo-board)
Arduino | [Automated Arduino test](./test-procedures.md#arduino)
USB Webcam | [Automated Camera test](./test-procedures.md#camera)
Battery (LiPo) | [Storage charged and manually inventoried](./test-procedures.md#batteries-and-chargers)
Battery Charger | [Storage charged and manually inventoried](./test-procedures.md#batteries-and-chargers)
Charger Supply | [Storage charged and manually inventoried](./test-procedures.md#batteries-and-chargers)
Battery bag | Manually inventoried
USB Memory Stick | Count & wipe
USB A to B cable | [Count and cable test](./test-procedures.md#usb-cable-testing)
Micro USB cable | [Count and cable test](./test-procedures.md#usb-cable-testing)
USB Hub | Count only
CamCon (7.5mm) | Count only
MiniCamCon (5mm) | Count only
MicroCamCon (3.81mm) | Count only
Screwdriver | Count only
Screw shields | Count only

Once this step is completed each type of item will be grouped into a box.
This is the box they will remain in for the rest of testing unless they fail a step.

## Visual Inspection

Once items have passed their functionality test, they need to go through a visual inspection.

What we are checking for here is:

- The asset sticker is still readable, including that the barcode is not damaged.
- The case doesn't have any holes large enough to poke a finger through.
- Any broken case pieces aren't creating sharp edges.

For items that need replacement asset codes create a separate pile so that all the new asset labels can be printed as a single batch.

For items that have broken cases, record the asset codes so that the `physical_condition` field can be updated in the inventory and place the item in the broken cases box.

Items that pass visual inspection can be returned to the box they were stored in after functionality testing.

## Cleaning

Where adhesives have been used to attach the kit to the robot there will be sticky residue that needs to be cleaned off.
Since we have started recommending alternative fixing methods to teams the number of boards returning with residue has decreased greatly.

Any remaining sticky chunks can be scraped off flat surfaces using a flat metal scrapper.
After this a wipe down with isopropyl alcohol can remove the remaining residue.

## Case Repairs

Where time allows, a first pass can be taken at replacing broken or missing cases by removing cases from boards that failed the functionality tests and spare case parts.

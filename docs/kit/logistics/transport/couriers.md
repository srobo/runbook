---
original:
  authors: Richard Barlow
  url: https://srobo-legacy.gitbooks.io/student-robotics-kit-logistics/kit-transport/couriers.html
---
# Couriers

Kit data for couriers:

* Dimensions: 48cm x 39cm x 20cm
* Weight: 6kg (A kit weighs approx. 4.95kg; 6kg gives some headroom)
* Value (for insurance): £500
* Batteries: Lithium Ion. Packed with equipment. Batteries less than 100Wh.

In all circumstances a shipment of a kit must have at least £500 worth of insurance.

Note that the above package details are repeated in the loan extension instructions in [return-shipping-pack.git](https://github.com/srobo/return-shipping-pack/tree/master/instructions) and therefore should be updated there when the details change.

## [DPD Local](https://www.dpdlocal.co.uk/)

We have used Interlink [http://www.interlinkdirect.co.uk/](http://www.interlinkdirect.co.uk/) in the past to ship kits. Interlink were bought by DPD and rebranded to "DPD Local" in 2017.

We were unable to send LiPo batteries via DPD Local when preparing for SR2022, as the majority of our batteries (any batteries not manufactured by Overlander) do not have the appropriate certifications.

## [UPS](https://www.ups.com/gb/en/Home.page)

UPS are willing to ship our kits, including LiPos.

When creating shipments using UPS, the recommended approach is to "create a shipment" that will be dropped off, and then separately "schedule a parcel collection" for them. This means collection only needs to be paid for once.

### Additional Packing Requirements for UPS

- Lithium Polymer batteries must be individually packaged and sealed
  - This is to prevent shorts.
  - The batteries do not need to be in a LiPo bag, although we would strongly recommend that they are.
- A LiPo warning sticker must be affixed to the outside of the box.
- The LiPos must be secured such that they will not move during shipping.
- The box must be flat-sided and "square" to qualify for low shipping rates

### Create a shipment

The "Create a shipment" form is quite long and complex. The form should be completed as below.

!!! note
    UPS recently created a new form, which hides some options and changes the wording. UPS recommend using the "Previous Experience" for more complex shipments, so that's what's assumed below.

- Ship From:
  - Wherever the kits will be collected from
  - Return address: UKPostBox
  - Use your own email (`@studentrobotics.org`) and phone for contact details
- Ship To:
  - Team address
    - Full name or Company Name: Institution name
    - Contact Name: Supervisor name
  - Include email and phone
- Parcel information
  - Packaging type: "My Packaging"
  - Total Identical parcels: 1
  - Weight per parcel: 6kg
  - Length, Width, Height: 50cm, 40cm, 20cm
  - Total parcel value: £500
- Do you need to schedule a collection?: "I'll drop off my shipment or include it in another collection"
  - Set the "Estimated Ship Date" as needed
- "Hold for customer collection at a UPS Access Point™ location?": "No, deliver to receiver"
- What are you shipping: "Robotics kit with battery"
- Signature Options: Signature required

Once the form is submitted, the PDF for the shipping label will be opened in a new tab, where it can then be saved. The tracking code is printed on the label, and shown in the window below.

!!! warning
    Once you leave this page, it may not be possible to retrieve the label or tracking code again. It's important the label be saved immediately.
    Submissions will **not** send you an email confirmation.

!!! bug
    When completing the form, sometimes it freezes when submitting. If it takes more than 15 seconds, cancel the shipment, reload the page, and complete the form again.
    It's **strongly** recommended to reload the form after each submission, even after being redirected to the form afresh.

### Schedule a parcel collection

Once the shipments have been created, the collection can be scheduled.

- "Do you have a pre-printed UPS SHipping Label for your shipment?": Yes
  - Enter the tracking codes as instructed
- "Collection Information and Location": Wherever the kits will be collected from. Should match the ship from address when creating the labels.
- Service and Packaging Information:
  - Packages in your collection: As needed
  - Total Weight of Your Collection: 6kg × number of packages
  - Select the matching UPS services (the shipping labels state which they're for, it should be consistent)
- "Does your collection contain Items that weigh more than 32 Kg.?": No
- Collection Date and Time
  - Complete as needed
- Collection Notifications
  - Your SR email address

Once requested, you'll receive an email with the request details.w

## S5-UPS

For SR2022 and SR2023, we shipped kits via the UPS Business account of a friendly company, herein referred to as S5-UPS.

### Additional Packing Requirements for S5-UPS

* LiPos must be individually inside jiffy bags, then inside the LiPo bag.
  * LiPo are manually checked before shipping
* S5-UPS kindly provided LiPo warning stickers for SR2022
* Boxes must be unsealed so that the contents can be checked before shipping.
* SR part code must be clearly printed on the box, ideally with a 2D barcode available to scan.
* Addresses must be provided in CSV format, with the SR part code of each box and the destination.

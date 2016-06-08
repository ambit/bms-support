---
title: Service - Jobs And Activities
permalink: "/docs/service-jobs-and-activities/"
position: 27
layout: docs
prev_section: stock-maintaining-businesses
next_section: service-raising-supply-orders
---

Create Jobs and track Job Activities through Labour, Parts and Supplies.

## New Jobs

If a single job needs to be logged against more than one Asset, additional assets are added after creation of the job, where each asset will have it's own Activities.

Selecting an existing contact will auto-populate the Contact Phone and Contact Email fields. When Other Contact is selected, the Contact Name input field is displayed, so the user can manually enter a name.

Save and Email Confirmation will not only save the new job, it will also send a confirmation email to the selected contact, indicating the job has been logged.

## Job Summary

The Job Status is displayed in the coloured 'Summary' bar on the right hand side. Note: this is different from the Job Activity Statuses.

The Callback on Job link has a tooltip with the Job and Agent on the first line, and the Job Description below.

'To Invoice' or 'Closed' Job Statuses also have an additional option in their menu dropdown for 'Create Callback on Job'.

The Job info fields are editable inline through an edit button that appears on hover. The description field is full width with no label and a 'Job Description' placeholder when empty.

## Activities

The expanded view of an activity shows certain fields from the New Activity form, it also shows all the Activity Statuses that have a value and their corresponding date and time for each.

If the Activity Status is not 'Cleared', then the next Activity Status (in the sequence) will display a blue link that says 'Update to (Status)'. Clicking this link will replace the view details section with the relevant 'Update to Status' form.

Activity Status in order are: 0 - Raised, 1 - On Backorder, 2 - Backorder Supplied, 3 - Allocated, 4 - Scheduled, 5 - In Transit, 6 - Arrived, 7 - Cleared, 8 - Completed, 9 - Cancelled.

### Activity Products

Grid of products, whereby you can add new lines.

Click the blue Add Product button slides out 2 select boxes: one identifies if the product is Used or Required (default is Used), the other is a predictive select for the product code.

Lines are editable inline, with the available products in a select box. Next to the select product is the warehouse the product is sourced from. This would default to the agent's default warehouse (it could be their van, which will be a warehouse in it's own right). Obviously Non Stocked products don't have a Warehouse, as such they have an N/A in the Warehouse column.

Submitting the activity will automatically create a Stock Movement for all relevant products.

## Backorders

The 'On Backorder' status is not available to manually 'Update Status' to, so most Activities will progress from 'Raised' to 'Allocated'.

The 'On Backorder' status can be set when an Activity is submitted that has products 'Required', and the 'Backorder Supplied' status is only available after this.

Alternatively, there is a button on the Edit Activity form to 'Place Backorder'.

**Submit Activity with Backorder**

When an Activity is submitted that has products with a Required column that has a value greater than 0, then a number of things happen:

1. A Draft 'Transfer' is created for the product in the Stock Module
2. If the current activity status is 'Scheduled', 'In Transit', or 'Arrived', then a new duplicate Job Activity is created with it's status changed to 'On Backorder'.
3. In the new Activity, the product is added and the qty in the 'Required' column is updated.
4. If the current activity status is 'Raised' or 'Allocated', then it's status is changed to 'On Backorder'.
5. When the Transfer is 'Complete', the 'Stock on Hand' and 'Required' columns are updated, and the Agent is sent a notification email.

## New Invoice

All activities need to be invoiced before a Job Status can be Closed (even if it is an invoice for $0.00). Activities waiting on an Invoice have an Activity Status of Cleared.

The New Invoice button will collate all activities on the Job that have a status of Cleared. It will generate an invoice and direct the user to the Invoice Details.

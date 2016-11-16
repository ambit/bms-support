---
title: Billing - Billings And Transactions
permalink: "/docs/billing-billings-and-transactions/"
position: 16
layout: docs
prev_section: billing-creating-contracts
next_section: billing-generating-invoices
---

## Billings Index

The billings index is split into a number of tabs based on the status of the billing, organised from left to right, following the progression of the billing status.

## Pending Billings

Starting with 'Pending', these indicate a Billing Period that is yet to have a transaction raised against it. Multiple pending billings will exists for a contract as they are generated for every month (or other recurring time period) of the contract, up until its expiry.

At the top of the index, there is an Admin Tools button with 2 options:

1. 'Generate New Pending Billings' will look for all ongoing contracts and any contracts near their expiry, it will then make sure there are at least 3 months worth of pending billings. The 3 months is a configurable setting and represents the minimum notice period a customer needs to provide, in order to cancel a contract.

2. 'Generate Upcoming Transactions' will generate transactions for pending billings that are due within the next 30 days. The 30 days is a configurable setting for the transaction lead time, and represents the subset of transactions you wish to work through at any one time.

Once a Pending Billing has a transaction raised against it, it will automatically transitions to 'Open'.

## Open Billings

'Open' billings have a transaction that requires further input before you can generate an invoice. That might mean it either needs meter readings, or the readings need to be manually reviewed.

At the top of the index, there is a Manage Meters button with 3 options:

1. 'Send Meter Requests' will display a form with parameters that allow you to email or print a meter request PDF for each transaction with missing readings. Customers have a default send method that determines whether the meter requests are emailed or printed and manually sent to the customer.

2. 'Import Meter Readings' will direct you to a form that lets you import meter readings from a CSV, for any of your assets. Once imported, those readings will sit on the assets, but will NOT as yet be applied to any transactions.

3. 'Generate Average Readings' will look at all the transactions with missing readings and apply the average volume for each meter (based on the average volume over the previous 3 months). However, if that would put the meter into overs, it will reduce the volume down to be the minimum (meaning no excess is charged).

Next to the Manage Meters button is another button for Admin Tools with 1 option:

1. 'Apply Latest Readings' will look at all the open transactions that require a meter reading, then look at the asset for those readings and apply the most recent reading for that meter, that fits within the billing period.

Once ALL the meter readings are applied, a transaction (and it's billing) will automatically transition to released.

The only exception to this is when at least one of the readings need to be manually reviewed. This occurs when the meter volume is either negative (less than last month) or it's volume variance (to the previous 3 billings) is greater than 25%. After reviewing the suspect readings, the transaction (and it's billing) can be transitioned to released.

## Released Billings

'Released' billings are ready to have an invoice generated, which can be done individually within each billing, or in bulk through the 'Generate Invoices' button at the top of the index.

Released billings will automatically transition to Completed once it's invoice is approved, and processed.

## Completed and Cancelled Billings

'Completed' Billings are historic billings that have had an invoice processed for them. Whilst 'Cancelled' billings have been manually cancelled by a user, which can only be done from a billing with an 'Open' status.

## Customer and Contract Billings

The billings tab within customers and contracts displays a list of billings down the page, grouped by month. Each billing is colour coded to indicate it's status - green for 'Complete', orange for 'Open', blue for 'Pending'.

On the left of each billing you have the 'Customer Name', 'Contract ID' and the 'Billing Number'. Clicking on the billing will expand it to show more details like the 'Type' of billing, the 'Due Date', and the 'Date Period' applicable for the billing.

Additionally, there will be a grid below with a list of transactions relevant to the billing. The 'Transaction ID' is a link to the actual transaction. The grid also displays the 'Status', 'Value' and 'Date', as well as the 'Number of Meters' read and a link to the 'Invoice' (if applicable).

Expanding a 'Pending' billing will also display a blue action button to 'Generate Transaction' for that billing period.

## Billing Details

After clicking on the 'Billing Reference' from the billings index, or the transaction ID from the customer / contract billings, you will be directed to the billing details page.

On the summary pane, you can see the 'Billing Reference' in the header, with the 'Status' for the billing period in the toolbar below. Clicking on the toolbar gives you the option to 'Generate Transaction' for that billing period.

Below the toolbar is all the relevant details for the billing period. The 'BMS Ref' is the auto-generated reference for the billing, whilst 'Customer Ref' is an optional field when creating the contract. The 'Billing No' identifies which billing this is in the life of the contract, and the 'Customer' and 'Contract' fields are links through to the actual customer and contract. Below these details are all the date fields - the 'Due On' date, as well as the date periods for 'Base', 'Usage' and 'Recon'.

On the content pane to the right, there is a single tab for 'Transactions'.

## Transactions

Whilst you would generally only have a single transaction per billing period, you can have multiple transactions within a billing period if a transaction is reversed, rebilled or adjusted. These actions would leave the original transaction in tact and generate one or many additional transactions, based on the action to be performed.

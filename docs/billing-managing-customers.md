---
title: Billing - Managing Customers
permalink: "/docs/billing-managing-customers/"
position: 15
layout: docs
prev_section: crm-creating-campaigns
next_section: billing-tracking-assets
---

The customer details page is split into two sections – the summary pane and the contents pane.

## Summary Pane

The summary pane shows a summary of the customer you're viewing, as well as the actions you can perform on that customer, like editing contact information.

* Heading – the customers full name.
* Toolbar – dropdown for editing the customer.
* Contact Details – At-a-glance information about the customer, such as address, email, phone number, and the main contact at the customer. Also, any applicable sales and geo areas.
* System Details - Date created and last updated.

## Contents Pane

The contents pane is split into tabs – these are all the sections that describe the customer in detail. Selecting a link at the top of the contents pane will display the related tab in the area below.

All content tabs have a toolbar at the top which will display tools relevant to that section, as well as pagination (if necessary).

## Contracts

The contracts tab is a grid of contracts applicable to the customer. The 'Contract ID' is a link to the actual contract. The grid also has fields for the 'Start Date', 'Expiry Date', and the 'Status' of the contract.

## Billings

The billings tab displays a list of billings down the page, grouped by month. Each billing is colour coded to indicate it's status - green for 'Complete', orange for 'Open', blue for 'Pending'.

On the left of each billing you have the 'Customer Name', 'Contract ID' and the 'Billing Number'. Clicking on the billing will expand it to show more details like the 'Type' of billing, the 'Due Date', and the 'Date Period' applicable for the billing.

Additionally, there will be a grid below with a list of transactions relevant to the billing. The 'Transaction ID' is a link to the actual transaction. The grid also displays the 'Status', 'Value' and 'Date', as well as the 'Number of Meters' read and a link to the 'Invoice' (if applicable).

Expanding a 'Pending' billing will also display a blue action button to 'Generate Transaction' for that billing period.

## Invoices

The invoices tab is a list of invoices attributed to the customer. The 'Invoice ID' is a link to the actual invoice. The grid also displays the invoice 'Description', 'Total Value', 'Total Invoiced' and invoice 'Status'.

<div class="note info">
  <span class="fa fa-quote-left fa-lg">&nbsp;</span>
  <h5>Only invoices applicable to billings are displayed here. Invoices created in service and stock for this customer are displayed in the respective applications.</h5>
</div>

## Sites

The sites tab is a list of locations attributed to the customer. It would generally be a list of offices and/or warehouses.

Apart from the actual address, you can also record emails and phone numbers, a 'Code' identifier and a default 'Site Contact' (selected from the existing contacts in the contacts tab).

## Contacts

The contacts tab allows you to record all the people you interact with at a customer. Keeping track of contacts at a customer allows you to target your interactions with the business.

Selecting 'New Contact' will take you to a new contact form where you can enter their details. You only need to record the persons name, however optionally you can add information about their position, phone number, and/or email address.

## Assets

The assets tab is a grid of assets 'owned' by the customer. The 'Serial No' is a link to the actual asset. We also display the 'Brand', 'Product Code', 'Site' and 'Cost Centre'.

Selecting 'New Asset' will display a new asset form at the top of the page where you can enter the asset details. After selecting an existing 'Product Code', it will automatically populate the fields for 'Brand', 'Description' and 'Product Class'. Site displays a list of sites (as seen in the sites tab). The 'Serial No' is a unique identifier for the asset, whilst the 'Cost Centre' is an un-validated text field.

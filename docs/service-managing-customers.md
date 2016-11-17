---
title: Service - Managing Customers
permalink: "/docs/service-managing-customers/"
position: 26
layout: docs
prev_section: service-raising-supply-orders
next_section: service-tracking-assets
---

The customer details page is split into two sections – the summary pane and the contents pane.

## Summary Pane

The summary pane shows a summary of the customer you're viewing, as well as the actions you can perform on that customer, like editing contact information.

* Heading – the customers full name.
* Toolbar – dropdown for editing the customer.
* Contact Details – At-a-glance information about the customer, such as address, email, phone number, and the main contact at the customer.

## Contents Pane

The contents pane is split into tabs – these are all the sections that describe the customer in detail. Selecting a link at the top of the contents pane will display the related tab in the area below.

All content tabs have a toolbar at the top which will display tools relevant to that section, as well as pagination (if necessary).

## Assets

The assets tab is a grid of assets 'owned' by the customer. The 'Serial No' is a link to the actual asset. We also display the 'Brand', 'Product Code', 'Site' and 'Cost Centre'.

Selecting 'New Asset' will display a new asset form at the top of the page where you can enter the asset details. After selecting an existing 'Product Code', it will automatically populate the fields for 'Brand', 'Description' and 'Product Class'. Site displays a list of sites (as seen in the sites tab). The 'Serial No' is a unique identifier for the asset, whilst the 'Cost Centre' is an un-validated text field.

## Jobs

The jobs tab is a grid of service jobs that have been raised for this customer. The 'Job No' is a link to the actual job. We also display information about the Asset the job was raised against, the location, the job category, priority and status, as well as which agent or engineer is assigned to the job. You can also create a new job for the customer from this tab, using the button at the top of the index.

## Orders

The orders tab is a grid of supply orders that have been raised for this customer. The 'Order' number will take you through to the underlying sales order in the stock application. We also display the number of items ordered, the delivery location and the order status.

You can also raise a supply order from this tab from the button at the top of the index. Supply Orders display a list of assets 'owned' by this customer, clicking on one of the assets will expand the line and show a list of supplies you can order for the asset you selected.

If you then click on the View Supply History button, on one of the supplies, you will see an order history for that supply, against that asset. As well as information about the product relationship between the asset and the supply (thing like the relevant meter, and the expected yield).

<div class="note info">
  <span class="fa fa-quote-left fa-lg">&nbsp;</span>
  <h5>Product relationships are configured in Stock, on the Product view page. For supply orders we are only interested in products that have a Supply relationship.</h5>
</div>

Placing a supply order is as simple as incrementing the Qty you wish to order for each supply, indicating if the item is chargeable or not, then when you have all the products you want, pressing Submit Supply Order.

For more information, see [Raising Supply Orders](../service-raising-supply-orders/)

## Invoices

The invoices tab is a list of invoices attributed to the customer. The 'Invoice ID' is a link to the actual invoice. The grid also displays the invoice 'Description', 'Total Value', 'Total Invoiced' and invoice 'Status'.

<div class="note info">
  <span class="fa fa-quote-left fa-lg">&nbsp;</span>
  <h5>Only invoices applicable to service are displayed here. Invoices created in billing and stock for this customer are displayed in the respective applications.</h5>
</div>

## Sites

The sites tab is a list of locations attributed to the customer. It would generally be a list of offices and/or warehouses.

Apart from the actual address, you can also record emails and phone numbers, a 'Code' identifier and a default 'Site Contact' (selected from the existing contacts in the contacts tab).

## Contacts

The contacts tab allows you to record all the people you interact with at a customer. Keeping track of contacts at a customer allows you to target your interactions with the business.

Selecting 'New Contact' will take you to a new contact form where you can enter their details. You only need to record the persons name, however optionally you can add information about their position, phone number, and/or email address.

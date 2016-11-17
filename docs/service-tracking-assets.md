---
title: Service - Tracking Assets
permalink: "/docs/service-tracking-assets/"
position: 27
layout: docs
prev_section: service-managing-customers
next_section: service-agents-and-engineers
---

Establish Assets and track their Jobs, Meters, Parts and Supplies.

## New Asset

Sales Order dropdown is only populated once Customer is selected. It is further refined if Site is selected. Sales Order Line dropdown is then only populated once a Sales Order is selected.

If Sales Order and Sales Order Line are selected it will prefill the Product Code, Brand, Description and Category. But if the Product Code is changed, Sales Order and Sales Order Line are then cleared.

The reason for having the option to link the Asset to a Sales Order is so that Made-To-Order assets can automatically have their actual components listed, without having to manually add each component used.

## Orders

The orders tab is a grid of supply orders that have been raised for this asset. The 'Order' number will take you through to the underlying sales order in the stock application. We also display the number of items ordered, the delivery location and the order status.

You can also raise a supply order from this tab from the button at the top of the index. Supply Orders display a list of supplies you can order for this asset.

If you then click on the View Supply History button, on one of the supplies, you will see an order history for that supply, against that asset. As well as information about the product relationship between the asset and the supply (thing like the relevant meter, and the expected yield).

Product relationships are configured in Stock, on the Product view page. For supply orders we are only interested in products that have a Supply relationship.

Placing a supply order is as simple as incrementing the Qty you wish to order for each supply, indicating if the item is chargeable or not, then when you have all the products you want, pressing Submit Supply Order.

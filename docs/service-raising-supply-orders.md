---
title: Service - Raising Supply Orders
permalink: "/docs/service-raising-supply-orders/"
layout: docs
prev_section: service-jobs-and-activities
next_section: service-managing-customers
---

A supply order can be raised in the Supplies tab if either a Customer on an Asset.

Expanding the asset will show a list of simple products with a related product relationship for supply.

It also includes a check box to indicate whether the supply is Chargeable or not, and a Quantity input field on the right (with increase and decrease buttons), for use with the New Order action button.

If a Contract has been added/linked to the Asset, the Chargeable field will by default be set to No (unticked), otherwise it will by default be set to Yes (ticked).

## New Order

Action button for the supplies grid, activated after incrementing one or more Quantity fields.

Automatically creates a Stock::SalesOrder with the selected supplies in an order group.

Takes into account the Quantity and whether the line is Chargeable or Free.

When the Sales Order is created, the order line and current meter reading need to be saved against the Service Orders table, which links Assets with their Order Line History.

## Supply History

Expanding an individual product line will show the Supply History, which is an overview of a Supply Relationship, displaying information from the previous Supply Orders.

This section displays the Supplys relevant Meter and Yield (where applicable).

Below this is a grid with the order line history, historic meters and the usage comparison to yield.

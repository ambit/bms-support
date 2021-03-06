---
title: Core - Filters And Pagination
permalink: "/docs/core-filters-and-pagination/"
position: 4
layout: docs
prev_section: core-navigation-and-user-permissions
next_section: crm-finding-contacts
---

## Is this list being filtered?

When viewing lists of items in BMS, keep in mind that many of them are filtered. There are a few reasons a list might be filtered:

* Some lists are automatically filtered to present you with the most relevant information. e.g. Tasks in BMS CRM are automatically filtered to show only the tasks that are assigned to you.
* If you have previously filtered a list, when you come back to it the same filter will still be applied as BMS will remember your filters.

In the tool bar at the top of the list, an unfiltered list will appear like this:

![Inactive Filter]({{ site.baseurl }}/img/core-inactive-filter.jpg)

Whereas if the list is filtered, it looks more like:

![Active Filter]({{ site.baseurl }}/img/core-active-filter.jpg)

You can click on the Filter button (&nbsp;<span class="fa fa-filter">&nbsp;</span>) to bring up the filter options. The options here include:

* Load Existing Filter - This option has a submenu of any saved filters for the current list, just select one to apply the filter.
* Adjust Current Filter - This option allows you to add more attributes to the current filter. If no filter is applied, you can add the first attribute.
* Save Current Filter - If you have a filter applied, you can choose to save it for future use, after which it will appear in the Load Existing Filter submenu.

## Pagination

Most lists in BMS allow a maximum of 20 items (but this may vary as it is configurable by your BMS Administrator). If your list exceeds this it will be split up over multiple pages.

![Pagination]({{ site.baseurl }}/img/core-pagination.jpg)

To navigate through the pages of the list, you can click on the pagination buttons to the bottom right of the list.

# SharePoint Lists - Totals of Calculated Columns Proof of Concept

Backup of: https://veeeetzzzz.medium.com/sharepoint-lists-totals-of-calculated-columns-proof-of-concept-713a71af99f8

Scenario:

A client has a SharePoint list. They have a Calculated Column and they need to know the total of that column.
Unfortunately, this can't be done out of the box but with a bit of trickery with Flow / Power Automate we can get the sum of the calculated column displayed on the list.

## Step 1 - Start with creating a calculated column

This column will calculate the difference between two dates (but this could be two figures as well) and return it as a single number. I used the DATEIF calculated field formula.

## Step 2 — Set up a Power Automate Flow

The flow will do this:

When an item is created, it will update the specified columns.

We use the concat feature to take the number from Calculated 1 and chuck into Column Total each time a new item is created. The trick here is that concat usually joins two string together, but we don’t have a second string to append so it just pulls through the single field we asked.

This allows the duplicated column to then be sorted by Totals as per below…

This is far from a final release — merely a Proof of Concept given the lack of functionality. Totals were avalible in the previous version of SharePoint — for now the suggestion is to get this idea on the product road map. You can visit the link here — https://sharepoint.uservoice.com/forums/329214-sites-and-collaboration/suggestions/15815590-totals-for-calculated-fields-in-sharepoint-lists.

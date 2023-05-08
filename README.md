# SharePoint Lists - Totals of Calculated Columns Proof of Concept

Backup of: https://veeeetzzzz.medium.com/sharepoint-lists-totals-of-calculated-columns-proof-of-concept-713a71af99f8

Scenario:

A client has a SharePoint list. They have a Calculated Column and they need to know the total of that column.
Unfortunately, this can't be done out of the box but with a bit of trickery with Flow / Power Automate we can get the sum of the calculated column displayed on the list.

## Step 1 - Start with creating a calculated column

This column will calculate the difference between two dates (but this could be two figures as well) and return it as a single number. I used the DATEIF calculated field formula.

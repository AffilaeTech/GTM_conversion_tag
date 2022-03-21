# Affilae Conversion Tag
Affilae Conversion Tag Template for GTM

----------

# Adding the Affilae Conversion Tag
The Conversion Tag needs to be added to your website’s event or confirmation page for the event or confirmation you wish to track (ex. sale, lead…) and should only be triggered after the Affilae Click Tag.

Before continuing; we recommend you have a basic understanding and some knowledge of how the GTM User-Defined Variables work, you can find explanations on the Google Support site here.

The Affilae Conversion Tag depends on the User-Defined Variables that you will be creating with the use of the website’s dataLayer.

----------

## Variables :

From your “Workspace”, in the left hand column, click on “Variables”.

Once the page loaded find the “User-Defined Variables” table and click on “New” to create a new variable.

- Name your variable ex. dl_conversion_id (if you already have User-Defined Variables in your GTM you can follow the naming convention in place to keep a clean workspace).

- Click the “Variable Configuration” table, then in the menu at the right hand side choose “Data Layer Variable”.

- In the “Data Layer Variable Name” field enter the value from your dataLayer on the website page where the conversion happens.

- For the “Data Layer Version” field keep this as the default value “Version 2”.

- Save your newly created variable and repeat the above steps for each variable that needs to be set.

**CAUTION** : When entering the “**Data Layer Variable Name**”, as mentioned in the steps above, the value must match that of the value found in the dataLayer. If the page where the Tag is triggered has a dataLayer that contains 2 of the same values (“*id*” for example) you will need to specify the property path on that value, below is an example of a well structured ecommerce dataLayer, if we want to get the value for the conversion id, you would need to enter the following property path in GTM:
*ecommerce.purchase.actionField.id* 

----------

## Triggers :

Once your variables have been created you will need to create and configure your Tag’s Trigger, to do this, from your “**Workspace**” click on “**Triggers**” in the left hand column.

When the page has loaded click on “**New**” to create a new Trigger.

- Name your Trigger ex. confirmation_page (if you already have Triggers in your GTM you can follow the naming convention in place to keep a clean workspace).

- Click in the “**Trigger Configuration**” table then in the menu on the right hand side, select the trigger type best suited to your needs, if you have a specific URL as confirmation page the “**Window Loaded**” or “**Page View**” triggers would be the easiest to use.

- Save your newly created Trigger and move on to your Tag creation and configuration.

----------
 
## Conversion Tag :

From your “**Workspace**”, in the left hand column, click on “**Templates**”.

Once the page has loaded, click on “**Search Gallery**” in the “**Tag Templates**” table.

- In the search bar type “**Affilae**” and click on the Template named “**Affilae Conversion Tag**”, then click “**Add to workspace**”.

- Once the Template has been added to your workspace go to the “**Tags**” menu in the left hand column and click on “**New**”.

- Name your Tag *ex. affilae_conversion* (if you already have Tags in your GTM you can follow the naming convention in place to keep a clean workspace).

- Click the “**Tag Configuration**” table and select the “**Affilae Conversion Tag**” from the list on the right hand side.

- Fill in the Tag fields using the variables you created (“*key*”, “*Conversion Id*”, “*Conversion Amount*” and “*Conversion Currency*” are required fields), Voucher Code and all other fields are optional.

-  Once the Tag Configuration is done, click on the “**Triggering**” table, the list of available Triggers will appear and you simply need to select the Trigger created earlier.

- Save your Tag, you can then test the Tag before Publishing to ensure that it works correctly.

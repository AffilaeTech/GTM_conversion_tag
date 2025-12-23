# Affilae Conversion Tag
Affilae Conversion Tag Template for Google Tag Manager

----------

# Adding the Affilae Conversion Tag
The Conversion Tag needs to be added to your website's event or confirmation page for the event or confirmation you wish to track (ex. sale, lead…).

**IMPORTANT**: The Conversion Tag must only be triggered **after** the Affilae Click Tag.

Before continuing, we recommend you have a basic understanding and some knowledge of how the GTM User-Defined Variables work. You can find explanations on the [Google Support site](https://support.google.com/tagmanager/answer/7683362).

The Affilae Conversion Tag depends on the User-Defined Variables that you will be creating with the use of the website's dataLayer.

----------

## Variables

From your "Workspace", in the left hand column, click on "Variables".

Once the page has loaded, find the "User-Defined Variables" table and click on "New" to create a new variable.

1. Name your variable (e.g., `dl_conversion_id`). If you already have User-Defined Variables in your GTM, follow the naming convention in place to keep a clean workspace.

2. Click the "Variable Configuration" table, then in the menu at the right hand side choose "Data Layer Variable".

3. In the "Data Layer Variable Name" field, enter the value from your dataLayer on the website page where the conversion happens.

4. For the "Data Layer Version" field, keep this as the default value "Version 2".

5. Save your newly created variable and repeat the above steps for each variable that needs to be set.

### Required Variables
You must create variables for these mandatory fields:
- **Key** - Your Affilae Program ID (e.g., XXXX-XXXX)
- **Conversion ID** - Unique identifier for your conversions (e.g., Order ID)
- **Conversion Amount** - Total amount Excluding Tax and Shipping Cost (e.g., 100.20)
- **Conversion Currency** - Currency in which the purchase was made in 3-letter ISO code (e.g., EUR, GBP, USD)

### Optional Variables
You can also create variables for these optional fields:
- **Conversion Sub ID** - Any internal reference or ID you may use
- **Conversion Payment** - Conversion payment type (e.g., debit card, credit card, paypal)
- **Customer ID** - Conversion Customer ID
- **Voucher Code(s)** - Voucher code(s) used (list of codes separated by `;`)
- **Product ID(s)** - Conversion Product ID(s) (list of product IDs separated by `;`)

**CAUTION**: When entering the "**Data Layer Variable Name**", the value must match exactly that of the value found in the dataLayer. If the page where the Tag is triggered has a dataLayer that contains nested values, you will need to specify the full property path. For example, in a well-structured ecommerce dataLayer, to get the conversion ID value, you would need to enter the following property path in GTM: `ecommerce.purchase.actionField.id` 

----------

## Triggers

Once your variables have been created, you will need to create and configure your Tag's Trigger. From your "Workspace", click on "Triggers" in the left hand column.

When the page has loaded, click on "New" to create a new Trigger.

1. Name your Trigger (e.g., `trigger_confirmation_page`). If you already have Triggers in your GTM, follow the naming convention in place to keep a clean workspace.

2. Click in the "Trigger Configuration" table, then in the menu on the right hand side, select the trigger type best suited to your needs. If you have a specific URL as confirmation page, the "Window Loaded" or "Page View" triggers would be the easiest to use.

3. Configure your trigger conditions to match your conversion page.

4. Save your newly created Trigger and move on to your Tag creation and configuration.

----------
 
## Conversion Tag

From your "Workspace", in the left hand column, click on "Templates".

Once the page has loaded, click on "Search Gallery" in the "Tag Templates" table.

### Installing the Template

1. In the search bar, type "**Affilae**" and click on the Template named "**Affilae Conversion Tag**".

2. Click "**Add to workspace**" to install the template.

### Creating the Tag

3. Once the Template has been added to your workspace, go to the "Tags" menu in the left hand column and click on "New".

4. Name your Tag (e.g., `tag_affilae_conversion`). If you already have Tags in your GTM, follow the naming convention in place to keep a clean workspace.

5. Click the "Tag Configuration" table and select the "Affilae Conversion Tag" from the list on the right hand side.

6. Fill in the Tag fields using the variables you created:
   - **Required fields**: Key, Conversion ID, Conversion Amount, and Conversion Currency
   - **Optional fields**: Conversion Sub ID, Conversion Payment, Customer ID, Voucher Code(s), and Product ID(s)

7. Once the Tag Configuration is done, click on the "Triggering" table. The list of available Triggers will appear and you simply need to select the Trigger created earlier.

8. Save your Tag. You can then test the Tag in Preview mode before Publishing to ensure that it works correctly.

----------

## Additional Resources

For more information, visit the official Affilae documentation:
- [Implementation with Google Tag Manager - Templates](https://affilae.com/en/documentations/implementation-with-google-tag-manager-templates/)
- [Affilae Homepage](https://www.affilae.com)

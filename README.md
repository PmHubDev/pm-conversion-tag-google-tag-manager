# Permate Conversion Tag - Google Tag Manager
The conversion of Permate is recorded when the Conversion Tag is placed on the Thank You page or when the event occurs.
Used in conjunction with the <b>Permate Brand SuperTag</b>. You can easily track customer conversions on the website, completely free with <i>Permate Global</i>.

## Overview Documentation

<ol>
<li>Create Permate Conversion Tag using the Permate Conversion Tag Template.
<li>Create, use or modify Variables.
</ol>

## 1.Creating Conversion Tags

<ol>
<li>Login to your Google Tag Manager Account, click the "Tags" tab and then click "New" button.
<li>Click on "Choose tag type to begin setup..." Then, click on the search icon and look for "Permate Conversion Tag" in the list of tag options. If you haven't used this template before, you'll need to click on it.

![GoogleTagManager_DiscoverMoreTag](https://github.com/user-attachments/assets/67024804-4644-4b26-99a0-716c87ca2311)
<li>Search for "Permate"

![GooogleTagManager_PermateSearch](https://github.com/user-attachments/assets/1c5ea3d5-503d-490a-a0b5-320a3acd615a)
<li>This tag will need to use a trigger that activates it on <b>View Thank You Page</b> events.

![GooogleTagManager_Trigger](https://github.com/user-attachments/assets/e796c1f2-7f41-4931-8ea4-6e44c47aa645)
<li>Name your tag and fill out the form completely.</li>
</ol>

## 2.Config Variables

![GoogleTagManager_Variables](https://github.com/user-attachments/assets/36b12550-68f0-4d48-bd2f-147f627f75f2)

<ol>
<li><b>Offer ID</b>: Directly enter the Offer ID of Permate, or select a parameter from the browser URL.
<li><b>Event ID</b>: Directly enter the value of the Permate Event ID for the tracked conversion event.
<li><b>Permate Click UUID</b>: Select a parameter variable from the browser URL that contains the value of click_uuid from Permate.
<li><b>Sale Value</b>: Enter a fixed value if the Product/Order/Price of the Brand does not change.
<br>If the product price of the Brand is dynamic, make sure to configure the following JavaScript snippet to be activated before the Conversion Tag is fired. <i>Here's a sample example:</i>

```javascript
if (typeof PERMATE === 'undefined') {
    window.PERMATE = {
        Conversion: {
            Sale: {}
        }
    };
}
var priceElement = document.getElementById('price');
if (priceElement) {
    PERMATE.Conversion.Sale.saleValue = priceElement.value;
}
```

You can place the provided script on your Order page or configure a trigger to ensure it runs before the Conversion Tag is fired
<li><b>Currency</b>: Select if using Vietnamese Dong; otherwise, it is Dollar.
</ol>

## More about Permate Conversion Tag
##### >> Visit [our Docs](https://permate.com/docs-category/brand-en/)

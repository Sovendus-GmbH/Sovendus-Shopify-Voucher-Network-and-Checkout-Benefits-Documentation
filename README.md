# Shopify Sovendus Voucher Network & Checkout Benefits Integration Documentation

## Create discount codes in bulk

If you use the Voucher Network, it's recommended to use a tool to create voucher codes in bulk \
You can use for example [Bulk Discounts](https://apps.shopify.com/bulk-discounts) to create multiple discount codes at once

## Add Sovendus script

> [!WARNING]
> Sovendus is currently not supported on the Shopify "Checkout Extensibility Upgrade" version, either revert your thank you page or wait until we can provide a solution.

1. Copy the Shopify script from [here](https://github.com/Sovendus-GmbH/Sovendus-Shopify-Voucher-Network-and-Checkout-Benefits-Documentation/blob/main/shopify.template.html) and replace YOUR_SOURCE_NUMBER and YOUR_MEDIUM_NUMBER with the one we provide you in your integration documentation. Make sure to use the right country code. If you are using sovendus for multiple countries, make sure you define YOUR_SOURCE_NUMBER and YOUR_MEDIUM_NUMBER in the script as well.
2. In your Shopify backend go to: Settings -> Checkout -> Order status page -> Additional scripts - paste the script and save it.

### Additional steps for Switzerland

For Switzerland it is also required to complete the following steps.

1. In your Shopify backend go to: Settings -> Customer events -> Click on Add custom pixel
2. Add a name e.g. Sovendus Landing Page and click on Add pixel
3. Paste the following code, click on Save on the top right and then on connect

```javascript
var script = document.createElement("script");
script.type = "text/javascript";
script.async = true;
script.src = "https://api.sovendus.com/js/landing.js";
document.body.appendChild(script);
```

# Rathbone Razor's shopify theme
This is the Rathbone Razor Shopify theme built on top of the Out Of The Sandbox Turbo theme.

## Things we changed

When we come to update the Turbo theme it will likely wipe out all our customizations. Below is a cheatsheet of the things that we will need to add back in.

1) Cookie consent

In the snippets folder reinstate `x-custom-cookie-consent.liquid`. Then in layout modify `theme.liquid` to include this code right before the closing `head` tag

````html
    {% include 'x-custom-cookie-consent' %}
````

We also need to add in the configuration options for cookie consent. These go in `config/settings_schema.json`

Copy the custom settings for the bottom of the old json file into the updated one. 

You may also need to copy over any values in `settings_data.json` (same folder) that start with `x_custom_` (not sure if Turbo will preserve those or not)

# Rathbone Razor's shopify theme
This is the Rathbone Razor Shopify theme built on top of the Out Of The Sandbox Turbo theme.

## Things we changed

When we come to update the Turbo theme it will likely wipe out all our customizations. Below is a cheatsheet of the things that we will need to add back in.

1) Cookie consent

In the snippets folder reinstate `x-custom-cookie-consent.liquid`. Then in layout modify `theme.liquid` to include this code right before the closing `head` tag

````html
    {% include 'x-custom-cookie-consent' %}
````

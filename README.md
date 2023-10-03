<p align="left">
  <img src="https://uploads-ssl.webflow.com/61f7b2443ecc4d7426c9639f/63f3b43bc03bb80034d27eed_SQLOGO-p-500.png" width="250">
</p>
<h1 align="left">General Hyvä Compatibility for Squeezely</h1>
This repository hold the module to add support for Squeezely to Hyvä. This module has a dependency on the Squeezely Magento 2 module.
https://github.com/squeezely/magento2-plugin

## About Squeezely
With Squeezely you can create the most advanced buyer journeys and personalization applications out-of-the-box.

## Installation

1. Install the module using composer: 

```bash
composer require squeezely/magento2-hyva-plugin
```

2. Enable the module:

```bash
bin/magento module:enable Squeezely_HyvaPlugin
```

3. Upgrade the database:

```bash
bin/magento setup:upgrade
```

4. Let Hyvä know about the new module:

```bash
php bin/magento hyva:config:generate
```

5. Generate the CSS files:

```bash
npm --prefix vendor/hyva-themes/magento2-default-theme/web/tailwind/ run ci
npm --prefix vendor/hyva-themes/magento2-default-theme/web/tailwind/ run build-prod
```

Or from your theme:

```bash
npm --prefix app/design/frontend/<Vendor>/<Theme>/web/tailwind run ci
npm --prefix app/design/frontend/<Vendor>/<Theme>/web/tailwind run build-prod
```

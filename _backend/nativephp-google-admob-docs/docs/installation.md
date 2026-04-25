# Installation

Plugin is distributed via <a href="https://nativephp.com/plugins/marketplace" target="_blank" rel="noopener">NativePHP's Plugin Marketplace</a>.

Install the package into your NativePHP app and register the plugin provider.

## 1. Require the package

```bash
composer require lrakauskas/nativephp-google-admob
```

## 2. Register the plugin

Register the plugin with NativePHP:

```bash
php artisan native:plugin:register lrakauskas/nativephp-google-admob
```

## 3. Publish config

```bash
php artisan vendor:publish --tag=nativephp-google-admob-config
```

## 4. (optional) Add JS bridge

If you want to call plugin methods from JS, or want easier way to subscribe to plugin events, add the JS bridge to your `package.json`:

```json
{
  "imports": {
    "#nativephp": "./vendor/nativephp/mobile/resources/dist/native.js",
    "#lrakauskas/nativephp-google-admob": "./vendor/lrakauskas/nativephp-google-admob/resources/js/nativephpGoogleAdmob.js"
  }
}
```

# nativescript-themes

A NativeScript plugin to deal with dynamically loading UI Themes.

This is a fork from `https://github.com/NathanaelA/nativescript-themes`. Check that repo for more updates.

## Installation

To use the original plugin:

```
tns plugin add @proplugins/nativescript-themes@latest
```

To use this fork:

- clone the repo;
- make a .tar.gz with the contents of the `src/` folder;
- `tns plugin add path/to/nativescript-themes.tar.gz`

## Usage

To use the module you just `require()` it:

```js
var themes = require('nativescript-themes');
```

## Setup in App

Modify your startup app.js

```js
var themes = require('nativescript-themes');
themes.applyTheme(themes.getAppliedTheme('red-theme.css'));
```

This will automatically apply the "red-theme.css" theme if no other theme has ever been chosen as the default theme.

You can also load a theme bundled by webpack using `applyThemeCss`:

```js
var themes = require('nativescript-themes');
var cssText = require('~/assets/themes/dark.scss');
themes.applyThemeCss(cssText, 'dark.scss');
```

## Demo

Demo shows three sample themes, and shows how to load the last chosen theme at startup.

See also: https://github.com/tralves/ns-vue-theme-swap-sample

## More

Documentation for this plugin is located <a href="https://npm.proplugins.org/-/web/detail/@proplugins/nativescript-themes">here</a>.

---
title: 'Brightness'
link: https://raw.githubusercontent.com/NativeScript/plugins/main/packages/brightness/README.md
---

<div style="width: 100%; padding: 1.2em 0em">
  					<img alt="github logo" src="../assets/images/github/GitHub-Mark-32px.png" style="display: inline; margin: 1em 0.5em 1em 0em">
  					<a href="https://github.com/NativeScript/plugins/tree/main/packages/brightness" target="_blank" noopener>Brightness</a>
				</div>

# @nativescript/brightness

```cli
ns plugin add @nativescript/brightness
```

This command automatically installs the necessary files, as well as stores @nativescript/brightness as a dependency in your project's `package.json` file.

:::tip Note

This plugin requires `<uses-permission android:name="android.permission.WRITE_SETTINGS"/>` to be added in the android manifest.

:::

## Usage

To use the brightness module you must first `require()` and instantiate it:

```javascript
// JavaScript
var nativescriptBrightness = require('@nativescript/brightness')
var brightness = new nativescriptBrightness.Brightness()
```

Or if you’re using TypeScript, `import` the module:

```typescript
// TypeScript
import { Brightness } from '@nativescript/brightness'
const brightness = new Brightness()
```

After you have a reference to the module you can then call its `get()` and `set()` methods. For example, the code below updates you screen's brightness with an `intensity` setting of 25%.

The `intensity` can be set to a value from 1 to 100.

```js
// TypeScript
import { Brightness } from '@nativescript/brightness'
const brightness = new Brightness()

brightness.set({
  intensity: 25
})
```

## API

### Methods

| Method                          | Description                                                                                                                    |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------ |
| set(options: BrightnessOptions) | set screen's brightness to the desired intensity                                                                               |
| get                             | returns current screen brightness value as a number between 0 and 100                                                          |
| getNative                       | returns current screen brightness value as returned from the native api: between 0.0 and 1.0 for iOS and 0 and 255 for android |

### BrightnessOptions

| Property  | Default | Description                                                                       |
| --------- | ------- | --------------------------------------------------------------------------------- |
| intensity | 100     | defines the desired brightness value, which should be a number between 0 and 100. |

## License

Apache License Version 2.0

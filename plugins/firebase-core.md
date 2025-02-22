---
title: 'Core'
link: https://raw.githubusercontent.com/NativeScript/firebase/main/packages/firebase-core/README.md
---

<div style="width: 100%; padding: 1.2em 0em">
  					<img alt="github logo" src="../assets/images/github/GitHub-Mark-32px.png" style="display: inline; margin: 1em 0.5em 1em 0em">
  					<a href="https://github.com/NativeScript/firebase/tree/main/packages/firebase-core" target="_blank" noopener>Core</a>
				</div>

# @nativescript/firebase-core

```cli
ns plugin add @nativescript/firebase-core
```

## Usage

Make sure you have your `google-services.json` file located in `App_Resources/src`.

### Initialize Default App

```ts
import { firebase } from '@nativescript/firebase-core'
const defaultApp = firebase().initializeApp()
```

### Initialize Secondary App

```ts
import { firebase, FirebaseOptions } from '@nativescript/firebase-core'
const config = new FirebaseOptions()
const secondaryApp = firebase().initializeApp(config, 'SECONDARY_APP')
```

## License

Apache License Version 2.0

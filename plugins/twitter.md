---
title: 'Twitter'
link: https://raw.githubusercontent.com/NativeScript/plugins/main/packages/twitter/README.md
---

<div style="width: 100%; padding: 1.2em 0em">
  					<img alt="github logo" src="../assets/images/github/GitHub-Mark-32px.png" style="display: inline; margin: 1em 0.5em 1em 0em">
  					<a href="https://github.com/NativeScript/plugins/tree/main/packages/twitter" target="_blank" noopener>Twitter</a>
				</div>

# @nativescript/twitter

```cli
ns plugin add @nativescript/twitter
```

## Prerequisites

Go to [Twitter Apps](https://apps.twitter.com/) to create your app so that you can obtain API key and secret, note:

- Remember to set a Callback Url, whatever will work
- By default, Twitter won't allow you to grab user's email, so you have to apply for a permission for your app to retrieve user's email

Here is how callbacks would look like:

![callback screenshot](https://raw.githubusercontent.com/NativeScript/plugins/main/packages/twitter/assets/images/callback.png)

## Usage

### iOS

Configure Info.Plist like below, replace `consumerKey` tag with your own key:

```xml
<key>CFBundleURLTypes</key>
<array>
  <dict>
    <key>CFBundleURLSchemes</key>
    <array>
      <string>twitterkit-<consumerKey></string>
    </array>
  </dict>
</array>
<key>LSApplicationQueriesSchemes</key>
<array>
    <string>twitter</string>
    <string>twitterauth</string>
</array>
```

```ts
import { Twitter, TwitterSignIn } from '@nativescript/twitter'

TwitterSignIn.init(TWITTER_COMSUMER_KEY, TWITTER_CONSUMER_SECRET)

Twitter.logIn()
  .then(session => {
    // session.authToken
    // session.authTokenSecret
  })
  .catch(e => {})
```

## License

Apache License Version 2.0

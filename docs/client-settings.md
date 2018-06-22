You can configure your app's settings from the <a href="https://developer.bitski.com" target="_blank">developer portal</a>. Here some of the things you can configure, and what they mean.

## App Info

This is metadata about your app that gives users more context. We will feature these details in our interface when we are presenting requests from your app or referencing your app.

## Approved Scopes

These are the scopes that clients using your *client id* can request. By default `openid` is the only scope that is approved. Requesting a scope that isn't approved for your app here will result in an error.

## Callback URLs

These are approved URLs that clients using your *client id* can ask to be redirected to. It's important to keep this list as small as possible so malicious apps cannot pose as you. If a client asks to be redirected to a URL that is not on this list, they will receive an error.

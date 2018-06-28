## Signing up

The first step is to make sure that you have a Bitski account. If you haven't done so already, <a href="https://bitski.com/sign-up" target="_blank">sign up for an account</a>. Your Bitski account is both your personal wallet, and your developer account.

## Getting a client ID

All apps that use the Bitski need to have their own client id. We use this id to keep track of permissions a user has granted you.

We're currently in private beta, so to get a client ID you must request access on our <a href="https://developer.bitski.com" target="_blank">developer portal</a>. We will review your request and notify you by email once you are approved.

## Configuring your client settings

Once you have a client id, you'll need to configure the settings for your app. You can do this from the <a href="https://developer.bitski.com" target="_blank">developer portal</a>.

The most important setting here is the redirect url(s). We use this to ensure that only the domains you approve will be able to use your client id.

For more information on all the settings, see [Client Settings](client-settings.md).

## Integrate with your app

Now that you have a configured client id, you can start using our SDKs in your app. You'll want to follow the instructions for the particular SDK you're using:

- <a href="https://github.com/BitskiCo/bitski-js" target="_blank">JavaScript</a>
- <a href="https://github.com/BitskiCo/bitski-ios" target="_blank">iOS</a>

For web based apps, you'll need to be able to respond to the callback from our servers.

It's also important to consider the user experience for various states your user will be in. Our SDKs can tell you whether or not the user is currently logged in, and you should update your UI based on that information.

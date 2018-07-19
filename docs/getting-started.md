## Signing up

The first step is to make sure that you have a Bitski account. If you haven't done so already, <a href="https://bitski.com/sign-up" target="_blank">sign up for an account</a>. Your Bitski account is both your personal wallet, and your developer account.

## Getting a client ID

All apps that use the Bitski need to have their own client id. We use this id to keep track of permissions a user has granted you.

To create one, visit our <a href="https://developer.bitski.com" target="_blank">developer portal</a>, and click **New App**.

Once your app is created it will be in a _Pending_ state. This means you can customize your app's settings, but you won't be able to actually use it until your app has been approved.

During our beta we are manually reviewing all new apps, and approving them. When your app is approved we will contact you at the email listed on your account. If you have a special request or time sensitive issue, you can [contact us](mailto:support@bitski.com) and we will review your request.

## Configuring your client settings

Once you have a client id, you'll need to configure the settings for your app. You can do this from the <a href="https://developer.bitski.com" target="_blank">developer portal</a>.

The most important setting here is the redirect url(s). We use this to ensure that only the domains you approve will be able to use your client id.

For more information on all the settings, see [Client Settings](client-settings.md).

## Integrate with your app

Now that you have a configured client id, you can start using our SDKs in your app.

A great place to start for new web-based apps is our <a href="https://github.com/BitskiCo/quickstart" target="_blank">Quickstart Truffle Box</a>.

You can find more details on integrating with your app by reviewing the instructions for the particular SDK you're using:

- <a href="https://github.com/BitskiCo/bitski-js" target="_blank">JavaScript</a>
- <a href="https://github.com/BitskiCo/bitski-ios" target="_blank">iOS</a>

For web based apps, you'll need to be able to respond to the callback from our servers.

It's also important to consider the user experience for various states your user will be in. Our SDKs can tell you whether or not the user is currently logged in, and you should update your UI based on that information.

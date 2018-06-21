Bitski uses OAuth2 to connect users and their wallets with your app. OAuth is a great standard for securely sharing data between services.

## How it works

As a developer, you choose what permissions and data you want access to through *scopes*. By default our SDKs only request the profile scope.

Then, when a user visits your app for the first time and chooses to authenticate with their Bitski account, they will see the requested scopes. The user can then make a decision to approve all, some, or none of the scopes.

Once the user has made a decision to grant your app various permissions, they will be redirected back to your app at the *callback url* that you specified. Note that the callback url specified from your client must match your url settings in the developer portal.

Through being redirected, you'll receive an authentication token that can be used to interact with Bitski's apis on behalf of the user.

Our various SDKs automatically handle passing that authentication token to Web3, so most likely you won't need to do anything with the authentication token yourself.

## Available Scopes

Name | Description
---- | ------------
`email` | Gives you access to the user's email address
`offline` | Allows your token to be renewed with a refresh token. This is required to have a session that lasts longer than 5 minutes.

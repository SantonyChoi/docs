In addition to managing wallets for users of your dapp, Bitski can also manage a wallet for your dapp itself. This makes it much easier to manage funding, deploying, and migrating your dapp's contracts.

On top of that, you can use your app wallet to securely perform any transactions you want from your backend using OAuth.

## Getting a Client ID & Secret

While we are in private beta this is a manual process. You can request an app wallet here. Once we create one for you, you can visit the [Developer Portal](https://developer.bitski.com) to see your credentials. Make sure to keep these keys a secret, because we will sign any transaction that is submitted using them.

## Funding your dev wallet

This is currently a manual process as well. We recommend buying ETH from a third-party such as <a href="https://coinbase.com" target="_blank">Coinbase</a> and sending it to your app wallet's address. You can find your address in the [Developer Portal](https://developer.bitski.com).

## Deploying Contracts with Truffle

We have a simple Truffle plugin that makes deploying contracts with your App Wallet easy. Read more about it [here](https://github.com/BitskiCo/bitski-truffle-plugin).

## Submitting transactions

You can also use standard Web3 apis on your backend to perform anything you want using your wallet. Here's how it works:

First, you'll use your client id and secret to request an access token. This token has a short lifespan, so you'll probably want to perform this step before every request.

```
// CURL EXAMPLE
```

Once you have an access token, you must add that to the Authorization header for your API request. We support all the standard Web3 JSON-RPC methods, so you can use any Web3 client to send these transactions.

```
// CURL EXAMPLE
```

Assuming your token is valid, your app wallet is funded, and the transaction is valid, it will be signed. There are currently no restrictions on what types of transactions will be signed, but we are considering this in the future.

Transactions submitted via this API must include all fields with the exception of _nonce_.

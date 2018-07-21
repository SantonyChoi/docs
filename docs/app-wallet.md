_Note: This feature is currently in beta._

In addition to managing wallets for users of your dapp, Bitski can also manage a wallet for your dapp itself. This makes it much easier to manage funding, deploying, and migrating your dapp's contracts.

On top of that, you can use your app wallet to securely perform any transactions you want from your backend using OAuth Client Credentials.

Note: App Wallet currently only supports mainnet and Rinkeby networks.

## Getting your credentials

To create an app wallet, visit our [Developer Portal](https://developer.bitski.com) and click *New App*. In the app creation form, select **Backend / App Wallet** under App Type.

After you create your app, your *client id* and *client secret* will be displayed. Make sure to download the credentials or copy these down somewhere, as the secret cannot be retrieved later.

## Getting your wallet address

We're working on a UI for managing this, but for now the best way to get your address is through web3 using our <a href="https://github.com/BitskiCo/bitski-truffle-provider">truffle provider</a>. You can try it out with our <a href="https://runkit.com/pixelmatrix/get-bitski-app-wallet-address" target="_blank">RunKit playground</a>.

## Funding your dev wallet

This is currently a manual process. We recommend buying ETH from a third-party such as <a href="https://coinbase.com" target="_blank">Coinbase</a> and sending it to your app wallet's address.

## Deploying Contracts with Truffle

We have a simple Truffle plugin that makes deploying contracts with your App Wallet easy. Read more about it [here](https://github.com/BitskiCo/bitski-truffle-provider).

## Submitting transactions

You can also use standard Web3 apis on your backend to perform anything you want using your wallet. Here's how it works:

First, you'll use your client id and secret to request an access token using OAuth Client Credentials. Most platforms have a library that can handle this step for you. Your token has a relatively short lifespan, so you'll probably want to perform this step before every request. You must request the scope `eth_sign`.

```text
POST /oauth2/token HTTP/2
Host: https://account.bitski.com

grant_type=client_credentials
&client_id=YOUR CLIENT ID
&client_secret=YOUR CLIENT SECRET
&scope=eth_sign
```

```text
HTTP/2 200 OK
Content-Type: application/json
Cache-Control: no-store
Pragma: no-cache

{
  "access_token": "YOUR ACCESS TOKEN",
  "token_type": "bearer",
  "expires_in": 3600,
  "scope": "eth_sign"
}
```

Once you have an access token, you must add that to the Authorization header for your API request. We support all the standard Web3 JSON-RPC methods, so you can also use any Web3 client to send these transactions.

```text
POST /web3/mainnet HTTP/2
Host: https://api.bitski.com
Content-Type: application/json
Authorization: Bearer YOUR ACCESS TOKEN

{
  "id": 1
  "jsonrpc": "2.0",
  "method": "eth_sendTransaction",
  "params": [{
    "from": "0xb60e8dd61c5d32be8058bb8eb970870f07233155",
    "to": "0xd46e8dd67c5d32be8058bb8eb970870f07244567",
    "gas": "0x76c0",
    "gasPrice": "0x9184e72a000",
    "value": "0x9184e72a",
    "data": "0x0"
  }]
}
```

```text
HTTP/2 200 OK
Content-Type: application/json

{
  "id":1,
  "jsonrpc": "2.0",
  "result": "0xe670ec64341771606e55d6b4ca35a1a6b75ee3d5145a99d05921026d1527331"
}
```

Assuming your token is valid, your app wallet is funded, and the transaction is valid, it will be signed. There are currently no restrictions on what types of transactions will be signed, but we are considering this in the future.

Transactions submitted via this API must include all fields with the exception of _nonce_.

For a list of all the supported methods, see [Ethereum's JSON-RPC spec](https://github.com/ethereum/wiki/wiki/JSON-RPC).

## JSON-RPC Endpoints

Name | URL
-----|-----
Ethereum | https://api.bitski.com/v1/web3/mainnet
Kovan | https://api.bitski.com/v1/web3/kovan (not currently supported)
Rinkeby | https://api.bitski.com/v1/web3/rinkeby

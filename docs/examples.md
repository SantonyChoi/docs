These examples are a great way to quickly dive in and see how you can integrate Bitski into a dapp on the platforms we support. Both of these examples use the same contract and assets to demonstrate how you can use Bitski to build cross-platform dapps.

## Web based Dapp

![Screenshot](public/web-dapp.png)

<a href="https://example-dapp-1.bitski.com" target="_blank" class="btn">Visit our demo here</a> <a href="https://github.com/BitskiCo/example-dapp-game" target="_blank" class="btn">View the code</a>

#### Running the example

First, install the dependencies.

```bash
npm install
```

Next, you'll need to use Truffle to deploy the contracts on one of Bitski's supported networks (Kovan or Rinkeby).

Install a local Ethereum node (Parity, or Geth), and configure your truffle.js to point at it, and run:

```bash
truffle migrate
```

Once the contracts are deployed, you can run to start the development server. You can learn more about deploying contracts with truffle here.

```bash
npm run dev
```

Then browse to http://localhost:3000

---

## iOS Dapp

<video autoplay loop muted playsinline preload style="width: 240px">
  <source src="../public/native-dapp.mp4" type="video/mp4">
  <source src="../public/native-dapp.webm" type="video/webm">
</video>

Our demo dapp is not available on the App Store yet, but you can still easily run it yourself from Xcode.

<a href="https://github.com/BitskiCo/example-native-dapp" target="_blank" class="btn">View the code</a>

#### Running the example

You'll need Xcode 9 and CocoaPods to build the example.

Start by installing the dependencies.

```bash
pod install
```

Then, simply open the workspace in Xcode and run the project.

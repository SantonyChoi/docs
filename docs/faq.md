Here are some answers to the questions we get asked most often.

### What networks do you support?

Bitski currently supports only the Kovan and Rinkeby test networks. However, we will have support for the main Ethereum network soon.

---

### What's your policy on information/user ownership?

Coming soon.

---

### How much does Bitski charge?

Bitski is currently free of charge for users and developers.

---

### Is Bitski open source?

We are partially open source. Our SDKs are open source, but the code that powers our website and infrastructure is primarily not.

---

### Why should I not just do my own key storage for new users?

Secure key storage is very challenging, and a siloed approach will be inconvenient for your users. Users will have to fund this wallet separately, and can only manage their assets through your interface.

---

### Can I use my Bitski account with Dapps that do not use the Bitski SDK?

Currently no. This is something we are planning to address with a browser extension soon.

---

### How much can I brand the Bitski transaction flow

Currently there is no customization of the transaction flow.

---

### I already have an app that uses Metamask, can I use Bitski?

Yes, they can. It doesn't negate any other wallet. It improves the dapp experience.

---

### How do I submit my dApp for Bitski?

You can request access from our Developer Portal.

---

### How are you storing private keys?

Our keys are both created and stored on our HSMs (Hardware Security Module). Approved transactions are passed to the HSM to sign. The keys never leave the hardware.

---

### Do you have an Android SDK?

Not at the moment, but that is on our roadmap.

---

### How should I integrate Bitski in my dapp?

A good place to start is to put our sign in button wherever you're currently asking people to install Metamask.

---

### How much lock in is there when building with Bitski?

Bitski has about as much lock in as other wallet providers. Since your users will presumably store assets from your app in our wallet, they will need Bitski to continue to use those assets. However, if the asset is transferrable, the user could decide to move them to another wallet instead.

---

### Can Bitski use ENS or Namecoin or other public naming systems?

Currently our wallet does not support sending to ENS names, or other public naming systems.

---

### Can I use Infura with Bitski?

Bitski provides the same services that Infura provides, so that would not be necessary.

---

### How will users fund their wallet?

For ETH, currently they will need to use another service to purchase ETH with fiat currency, and transfer that to their Bitski wallet. Eventually we'll have a more integrated process.

However, if you're working with digital assets, we suggest using our app wallet API to send assets to users directly. This prevents the need for the user to purchase ETH, while allowing them to have decentralized ownership.

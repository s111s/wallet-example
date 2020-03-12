# Example of NEAR Wallet integration
[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/nearprotocol/wallet-example)

## Description

This example demonstrates how to integrate your application with NEAR Wallet.
The contract is quite simple. It can store the account_id of last sender and return it. It also shows how you can debug contracts using logs.

## Getting started

There are two ways to run this project. The first is the quick and a good way to instantly become familiar with this example.
Once familiar, the next step is for a developer to create their own NEAR account and deploy the contract to testnet. This is covered in the following section.

There's a button at the top of this file that says "Open in Gitpod." This will open the project in a new tab with an integrated development environment. The other option is to clone this repository and follow the same instructions.

### Quickest option

1. Install dependencies:

```
yarn
```

2. Build and deploy this smart contract to a development account. This development account will be created automatically and is not intended for reuse:

```
yarn dev
```

If using Gitpod, a small dialog may appear showing options similar to this:

![Gitpod dialog that appears when website is served](assets/gitpod-port-1234.jpg)

The "Preview" option will open the site in a tab within the IDE. Note that Gitpod may need a little time to spin up the website. It's possible this step might require reloading after a brief pause.

### Standard deploy option
In this second option, the smart contract will get deployed to a specific account created with the NEAR Wallet.

1. Ensure `near-shell` is installed by running:

```
near --version
```

If needed, install `near-shell`:

```
npm install near-shell -g
```

2. If you do not have a NEAR account, please create one with [NEAR Wallet](https://wallet.nearprotocol.com).

In the project root, login with `near-shell` by following the instructions after this command:

```
near login
```

3. Modify the top of `src/config.js`, changing the `CONTRACT_NAME` to be the NEAR account that was just used to log in.

```javascript
…
const CONTRACT_NAME = process.env.CONTRACT_NAME || 'YOUR_ACCOUNT_NAME_HERE'; /* TODO: fill this in! */
…
```

4. Start the example!

```
yarn start
```

## To Test

```
yarn asp // as-pect tests
yarn jest // integration tests
yarn test // both
```

## To Explore

- `assembly/main.ts` for the contract code
- `src/index.html` for the front-end HTML
- `src/main.js` for the JavaScript front-end code and how to integrate contracts
- `src/test.js` for the JS tests for the contract

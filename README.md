<div align = "center">
    <h1>KittyCoin Club <em>DApp</em></h1>
    <p>Donation site for cats in foster care built on smart contracts.</p>
    <a href="https://travis-ci.org/fluffycatware/kittycoin-club" target="_blank"><img src="https://travis-ci.org/fluffycatware/kittycoin-club.svg?branch=master" alt="Build Status"></a>
    <a href="https://codecov.io/gh/fluffycatware/kittycoin-club" target="_blank"><img src="https://codecov.io/gh/fluffycatware/kittycoin-club/branch/master/graph/badge.svg" alt="codecov"></a>
    <a href="https://www.ethereum.org/" target="_blank"><img src="https://img.shields.io/badge/Ethereum-ETH-blue.svg" alt="Ethereum"></a>
    <a href="https://solidity.readthedocs.io" target="_blank"><img src="https://img.shields.io/badge/Solidity-%5E0.4.18-blue.svg" alt="Solidity"></a>
</div>

## About

This repository houses the [kittcoin.club](https://kittycoin.club)'s donation system. It has been built using Ethereum smart contracts.

## Developing This Contract

In order to develop this contract the following steps were taken to setup the environment.

Install and run Ganache CLI (formally you would have used TestRPC). Alternatively you can install [Ganche](http://truffleframework.com/ganache/) UI.

```
$ npm install -g ganache-cli
$ ganache-cli
```

When you run Ganache you'll be presented with 10 accounts with private keys. The RPC service that you can interact with the blockchain through is also available on `localhost:8545` for the CLI version and `localhost:7545` for the GUI.

Navigate into the root of this project and install truffle (if you haven't already got it). Run the truffle test command to compile and test the contracts.

```
$ npm install -g truffle
$ truffle test
```

If you watch the `ganache-cli` output you'll see various transactions taking place while your the contracts unit tests are executed.

Here's and example of a transaction:

```bash
Listening on localhost:8545
net_version
eth_accounts
eth_accounts
eth_accounts
net_version
net_version
eth_sendTransaction

  Transaction: 0x0c53488c3db64d41f972dfa9ce4d96f123f404f2a72fc7e843e5c8265b34c8ee
  Contract created: 0x926f5105ea9e1cbf4476a5437e42c5880b78309a
  Gas usage: 269607
  Block Number: 1
  Block Time: Wed Jan 17 2018 22:42:34 GMT+0800 (AWST)
```

When `truffle test` is executed it uses the `test` config within the `truffle.js` file

```javascript
    test: {
        host: "localhost",
        gasPrice: 1,
        gas: 0xffffffff,
        port: 7545,
        network_id: "*", // Match any network id
    },
```

*Note: I have 7545 in this file as I've been using the GUI version of Ganache which defaults to this port.*

To run the dev application use the following

```
$ npm install
$ npm run dev
```

## Screenshots

<img src="https://raw.github.com/fluffycatware/kittycoin-club/master/img/project-banner.jpg" data-canonical-src="https://raw.github.com/fluffycatware/kittycoin-club/master/img/project-banner.jpg" align="center"/>

## Attribution

This smart contract used [Giveth's Base layer](https://github.com/Giveth/common-contract-deps) contract structure. Check out the amazing work they are doing at [Giveth's website](https://github.com/Giveth/website).
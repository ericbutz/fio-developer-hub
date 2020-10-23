---
id: index
title: Overview
sidebar_label: Overview
---
## Getting Started

[![Getting Started with the FIO Dev Hub](http://img.youtube.com/vi/nYp5QLEjDeY/0.jpg)](https://www.youtube.com/watch?v=nYp5QLEjDeY&feature=emb_logo "Getting Started with the FIO Protocol Website and Integration Documentation")

## What is FIO Protocol? 

The FIO Protocol is bridging the gap between wallets (both exchange-based and self-sovereign) as well as crypto payment processing platforms providing an industry standard decentralized service layer of data, requests and confirmations that abstract away the complexities of the underlying blockchains. The FIO Protocol is not a wallet, not an exchange and not a crypto payment processor, rather, it enables them all to deliver a dramatically improved user experience. The FIO Protocol does not compete with other blockchains nor does it send value on or integrate with other blockchains but, rather, it enables them all to be more successful. Technically speaking, all other blockchains do not even know that the FIO Protocol exists.

### FIO Address

FIO Addresses act as the human readable “wallet names” and user identifiers on the network. In addition, FIO Addresses are the gateway to all other capabilities of the FIO Protocol. Registration of a FIO Address is done in a FIO enabled wallet or exchange where a FIO Private/Public Key pair is generated. The FIO Address and all actions on the FIO Chain are self-sovereign via the FIO Private Key. Without a FIO Address, users cannot access any of the other FIO protocol capabilities.

### FIO Request

A FIO Request is a transaction in which a payee is requesting funds from payer using FIO Addresses. The payee first encrypts all sensitive metadata (e.g. currency, amount, public address of payee, memo, etc.) using Diffie-Hellman key method , which derives a shared secret from the payee private key and the payer public key and places the transaction on the FIO Chain. The payer polls the FIO Chain, decrypts the metadata inside their wallet and uses the information to pre-populate the send transaction, which is broadcasted to the native blockchain without involving the FIO Protocol.

### FIO Data

In addition, the payer places a metadata about the native blockchain transaction (e.g. native blockchain transaction id, refund address, memo, hash of off-chain metadata, etc.) on the FIO Chain. Just like the request, the metadata would be encrypted using Diffie-Hellman key method.

## Key resources

### Learn more

To learn more about the FIO Protocol, please check out the Whitepaper and Knowledge Base.

### Wallet integration

If you are interested in integrating FIO Protocol into a wallet, check out our Wallet Integration Guide, and if you are ready to dive into code, our API spec will explain all the calls we provide. Alternatively, make it easy on yourself and take a look at some of our SDKs.

### Exchnage integration

If you are an exchange, check out our Exchange Integration Guide.

### FIO Chain

If you want to spin-up your own node or even become a block producer, check out the FIO Chain section for more information about building a node.

### Testnet

We have a Testnet up and running, check it out here.

### API endpoints

#### Testnet Chain API
```
http://testnet.fioprotocol.io/v1/chain/
```
#### Mainnet Chain API

[See Github](https://github.com/fioprotocol/fio.mainnet)

#### Testnet Registration Site API
```
https://reg.az.fio.dev/public-api/
```
### Mainnet Registration Site API
```
https://reg.fioprotocol.io/public-api/
```
### Testnet History API
```
http://testnet.fioprotocol.io/v1/history/
```
### Mainnet History API

See Github

### Help

Need help? [Just ask](https://developers.fioprotocol.io/help/contact-us).

## Complete List of Developer Hub Resources

FIO Protocol
Code
How is FIO Chain different from EOSIO
Keys, accounts and permissions
Multisig
Resource Management
Technology Provider ID
FIO Protocol API
Latest API Spec
Getting started
Packing and signing of transactions
Generating actor
Registration API
Latest Regsitration API Spec
Getting started
SDKs
iOS Swift
Kotlin
JavaScript/TypeScript
Tools
clio
Wallet Integration Guide
Integration options
Sample wallet UX
Demo
Mapping Public Addresses
Encrypting FIO Data
FIO registration site
Exchange Integration Guide
FIO integration
Listing integration
FIO Chain
Building a node
History node
Testnet
Mainnet
Voting for block producers
Being a block producer
Vulnerability Disclosure Policy
Help

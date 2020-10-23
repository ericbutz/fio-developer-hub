---
id: fioint
title: FIO integration
sidebar_label: FIO integration
---

Exchange FIO integration

Table of contents

Overview
Handling FIO token deposits
Handling FIO token withdrawals
Overview

Using FIO Address, FIO Request and FIO Data can significantly improve the user experience of depositing and withdrawing of any token to or from the exchange.
Handling FIO token deposits

Using unique FIO Address for each user

An exchange may set-up a unique FIO Address for each user of the exchange, and display it in their deposit area, e.g. alice@myexchange.

To deposit tokens of any supported cryptocurrency to their account the user would simply send tokens from FIO-enabled wallet to their FIO Address, e.g. alice@myexchange, and would not have to deal with Public Keys, memo fields or even having to log into the exchange.

Each FIO Address may be mapped using /add_pub_address to either the same Public Address for all users or unique one for each user.

Using same FIO Address for all users

An exchange may set-up a single Deposit FIO Address for all users of the exchange, and display it their deposit area, e.g. deposits@myexchange.

To deposit any supported token to their account the user would simply send tokens from FIO-enabled wallet to the Deposit FIO Address, e.g. deposits@myexchange. To properly identify the inbound transaction, the user would have to either include a memo which includes their exchange account, or provide the exchange, ahead of time, with a list of FIO Addresses which the user owns.

The Deposit FIO Address would be mapped using /add_pub_address to a single FIO Public Key.

The inbound transaction can be identified by reading the OBT Data using /get_obt_data. The data is encrypted. Once decrypted, memo or FIO Address of Payee will uniquely identify the user and obt_id will contain native chain transaction ID of the corresponding deposit.

Transaction memo for FIO token transfer

/transfer_tokens_pub_key does not accept a memo field. To attach a memo to a FIO token transfer, a /record_obt_data transaction should be sent after the tokens are transferred and include the token transfer transaction id. /record_obt_data requires that both payer and payee have a FIO Address. If either party does not have a FIO Address transfer of memo is not supported.
Handling FIO token withdrawals

Using FIO Address

With this option, the user’s withdrawal area on the exchange would ask for a FIO Address and the amount of withdrawals of any token. Once FIO Address is entered, the corresponding public address for that chain is looked-up using /get_pub_address and the transfer is executed on the native chain.

Using FIO Request

If users of exchange were assigned unique FIO Addresses or if users provided the exchange, ahead of time, with a list of FIO Addresses which the user owns, they could send a FIO Request from their wallet to the exchange’s FIO Address (either generic, e.g. withdrawals@myexchange, or unique, e.g. alice@myexchange).

The user would then login to the exchange and approve the FIO Request. Once approved, the exchange would execute the transfer on the native chain.
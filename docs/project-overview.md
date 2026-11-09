# PORTLG Wallet — Project Overview

## Summary

PORTLG Wallet is a wallet-connected application and testnet prototype demonstrating an owner-controlled pause/resume mechanism for a protected smart-contract operation on Portaldot V3 Testnet.

Its core demonstration is **Protected Action**. The deployed `PORTLGuardLite` contract maintains a paused state. When active, `protectedAction()` can execute; when paused, the contract blocks that operation. The contract owner can call `pause()` and `unpause()`.

## Problem

A user-interface alert can communicate a concern, but an alert alone does not enforce whether a smart-contract operation may execute. A protected operation needs an enforceable rule at contract level, with state changes that can be inspected on-chain.

## Approach

PORTLG combines:
- A browser-based wallet interface.
- MetaMask for account connection, key custody and transaction signing.
- Portaldot V3 Testnet for contract execution and transaction records.
- PORTLGuardLite for owner-controlled pause/resume enforcement.
- Explorer links for independent inspection of deployment and transactions.

## Current scope

Current project information describes MetaMask connection, network validation, tPOT balance display and transfer interface, together with the PORTLGuardLite controls. Actual wallet functionality is in the [main PORTLG Wallet repository](https://github.com/blueyellow1/portaldot-hackathon-2026-portlg-wilkris).

The interactive buttons in the pitch deck's Protected Action slide are an explanatory browser simulation. They do not call the deployed contract.

## Deployment reference

- Network: Portaldot V3 Testnet
- Chain ID: `420420777`
- Contract: `PORTLGuardLite`
- Address: `0x44406CD3e7ccE420c316D015FEE74303F16629E5`
- Deployment block: `200580`
- Deployment transaction: `0x6115a0880f1822ba7b43c5b0461323eaebab701f12ce22b81325a3d2b1e5d879`

## Not currently claimed

PORTLG does not claim autonomous threat detection, automatic threat-triggered pausing, guardian controls, multi-network support, completed paid access, or an independent security audit. Premium access and broader integrations are roadmap ideas only.

## Intended use

This repository packages the pitch presentation and supporting material. It is not the source repository for the wallet application or the smart contract implementation.

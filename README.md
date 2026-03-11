# Multi-Sig Vault Wallet

This repository provides a robust Multi-Signature wallet implementation. It is designed for DAOs, teams, or individuals who want to distribute control over a pool of funds. No transaction can be executed unless it reaches a predefined threshold of confirmations from authorized owners.

## Features
- **M-of-N Security:** Define the number of owners and the required number of signatures (e.g., 2-of-3).
- **Transaction Life-cycle:** Submit, Confirm, Execute, and Revoke.
- **Deposit Tracking:** Emits events for every ETH deposit received.
- **Security:** Built-in protection against re-entrancy and unauthorized access.

## How to Use
1. **Deployment:** Pass an array of owner addresses and the required number of confirmations to the constructor.
2. **Submit:** Any owner can submit a transaction proposal.
3. **Confirm:** Other owners call `confirmTransaction` to sign off.
4. **Execute:** Once the threshold is met, any owner can trigger `executeTransaction`.

## License
MIT

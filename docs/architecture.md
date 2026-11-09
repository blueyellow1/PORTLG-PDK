# PORTLG — High-Level Architecture

## Components

1. **Wallet interface** — presents account, network and supported wallet actions.
2. **MetaMask** — connects the user's account and holds/signs with the user's keys. PORTLG does not independently store private keys.
3. **Portaldot V3 Testnet** — executes transactions and records state changes.
4. **PORTLGuardLite** — stores the paused state and enforces the Protected Action condition.
5. **Block explorer** — lets users inspect contract deployment and transaction evidence.

## Protected Action state flow

- Active state: `paused = false`; `protectedAction()` is allowed by the contract's state condition.
- Pause: the owner calls `pause()`; the contract sets the paused state to true.
- Paused state: `paused = true`; `protectedAction()` is blocked by contract logic.
- Resume: the owner calls `unpause()`; the contract returns to the active state.

Only the contract owner can invoke the owner-restricted pause/resume functions.

## Transaction flow

1. The user connects MetaMask to the application.
2. The interface checks the selected network and prepares a supported request.
3. MetaMask presents the transaction for the user to review and sign.
4. Portaldot V3 Testnet executes the transaction.
5. The resulting transaction can be inspected through the explorer.

## Trust boundaries and limitations

- Private keys remain managed by MetaMask.
- The contract's pause/resume authority is owner-controlled; this is not a decentralized guardian or automated response system.
- A UI message is not the security boundary. The protected operation's contract condition is the enforcement point.
- The pitch deck's slide 4 is a local state illustration only; it is not connected to the blockchain.
- The deployment is on a testnet and has not been independently audited.

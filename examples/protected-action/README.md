# Protected Action Example

This example explains the state rule demonstrated by PORTLGuardLite. It is documentation, not a replacement contract implementation.

## Expected behavior

| Contract state | Call | Expected result |
|---|---|---|
| Active (`paused = false`) | `protectedAction()` | Allowed by the pause-state condition |
| Active (`paused = false`) | owner calls `pause()` | State becomes paused |
| Paused (`paused = true`) | `protectedAction()` | Reverted/blocked by contract logic |
| Paused (`paused = true`) | owner calls `unpause()` | State returns to active |

The pause and resume functions are owner-restricted.

## Important distinction

The buttons on slide 4 of the pitch deck reproduce this state flow in local JavaScript for explanation. They do not interact with the deployed contract. Real contract interactions require the wallet application, MetaMask and Portaldot V3 Testnet.

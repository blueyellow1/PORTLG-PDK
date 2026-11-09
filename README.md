# PORTLG Pitch Deck Kit (PORTLG-PDK)

An original, self-contained pitch deck and supporting documentation for **PORTLG Wallet**, a hackathon prototype demonstrating owner-controlled pause/resume enforcement for a protected smart-contract operation on Portaldot V3 Testnet.

## Open the pitch deck

- **Live presentation:** https://blueyellow1.github.io/PORTLG-PDK/index.html
- **Presentation source:** [web/index.html](web/index.html)

The presentation is a 10-slide, responsive HTML deck. It includes slide navigation, an interactive illustration of the Protected Action state, contract deployment evidence, architecture, roadmap, demo and video links. It is a presentation/illustration; the interactive Protected Action buttons on slide 4 simulate contract state in the browser and do not send blockchain transactions.

## Repository contents

| Path | Purpose |
|---|---|
| `web/index.html` | Published HTML pitch deck |
| `docs/project-overview.md` | Project scope, problem, solution and current status |
| `docs/architecture.md` | High-level wallet, MetaMask, contract and testnet architecture |
| `docs/demo-guide.md` | How to open and present the deck and demo |
| `examples/wallet-demo/README.md` | Wallet demo walkthrough and boundaries |
| `examples/protected-action/README.md` | Protected Action state-flow example |
| `tests/README.md` | Manual verification checklist and test limitations |
| `.github/workflows/pages.yml` | GitHub Pages deployment workflow |

## Related project links

- **PORTLG Wallet repository:** https://github.com/blueyellow1/portaldot-hackathon-2026-portlg-wilkris
- **PORTLG Wallet demo:** https://marvelous-pudding-14d30d.netlify.app/
- **Demo video:** https://youtube.com/shorts/R1LaKYAD-oA
- **Portaldot V3 Testnet explorer:** https://scanner-testnet-v3.portaldot.dev/

## Deployment

GitHub Pages is configured to deploy the contents of `web/` using GitHub Actions. A push that changes `web/**` or the Pages workflow triggers a deployment. The latest deployment status is visible under **Actions → Deploy PDK Pitch Deck to GitHub Pages**.

If the live page does not show a recent change, check the latest workflow run first. A successful workflow means the artifact was deployed; it does not constitute a security audit or an end-to-end test of the wallet.

## Project scope and limitations

- PORTLG is a **testnet prototype**, not a production wallet and not intended for real funds.
- MetaMask manages the user's account keys and transaction signing.
- The current contract control is owner-operated: `pause()` and `unpause()` change the paused state; `protectedAction()` is blocked while paused.
- The project does not claim autonomous threat detection, automatic pausing, guardian functionality or an independent security audit.
- Premium/payment access and broader network support are roadmap items, not implemented features.
- The slide 4 controls are a local browser simulation for explaining the state transition; use the wallet demo and explorer for actual on-chain interactions and evidence.

## Contract deployment reference

- Contract: `PORTLGuardLite`
- Network: Portaldot V3 Testnet
- Chain ID: `420420777`
- Contract address: `0x44406CD3e7ccE420c316D015FEE74303F16629E5`
- Deployment block: `200580`
- Deployment transaction: `0x6115a0880f1822ba7b43c5b0461323eaebab701f12ce22b81325a3d2b1e5d879`

Verify these details independently in the [Portaldot V3 Testnet explorer](https://scanner-testnet-v3.portaldot.dev/).

## Team

**Team Wilkris** — PORTLG Wallet / Portaldot Hackathon 2026.

## Contributing

Keep changes focused and accurate. Do not describe planned features as implemented, and do not claim a test or deployment succeeded unless the relevant evidence is available. Update the documentation whenever the deck's verified project facts or links change.

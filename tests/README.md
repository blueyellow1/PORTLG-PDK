# Verification Checklist

This repository primarily contains a static HTML presentation and documentation. It does not currently include an automated contract test suite or browser end-to-end test runner. Do not interpret the checklist below as a report of tests already executed.

## Pitch deck checks

- [ ] Open https://blueyellow1.github.io/PORTLG-PDK/index.html
- [ ] Confirm all 10 slides render.
- [ ] Navigate forward and backward using the controls.
- [ ] Test keyboard navigation on a desktop browser.
- [ ] Test swipe navigation on a touchscreen.
- [ ] Check the slide 4 local state illustration: active → pause → blocked → unpause → allowed.
- [ ] Open the demo video and wallet demo links.
- [ ] Open the PDK and wallet GitHub repository links.
- [ ] Check that the contract address and deployment transaction are readable and copyable.

## Deployment checks

- [ ] Confirm the latest GitHub Actions Pages workflow completes successfully.
- [ ] Reopen the published URL after deployment.
- [ ] Verify the latest change appears on the live page.

## Wallet and contract checks

Actual wallet and contract verification must be performed against the live application and Portaldot V3 Testnet. This repository's static deck checks do not prove wallet functionality, contract correctness, security, or audit status.

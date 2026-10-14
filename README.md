# SharpenWill — Checkout Backend Prototype

An experimental **Node.js / Express** backend created while developing the SharpenWill Android app.

## What this repository contains
- An Express server with a `POST /create-checkout-session` endpoint
- Stripe Checkout session creation configured for a subscription
- Environment-variable references for `STRIPE_SECRET_KEY` and `STRIPE_PRICE_ID`
- A local development server configured for port 5000 by default

## Stack
Node.js · Express · Stripe SDK · dotenv · cors · body-parser

## Project status
**Prototype / development archive.** This repository is not presented as a production-ready payment service. The success and cancel URLs in `server.js` are placeholders, and deployment and integration have not been verified.

The source uses ES module `import` syntax; the current `package.json` does not declare `"type": "module"`. Depending on the Node.js runtime, this may need correcting before the server will run reliably.

## Configuration
The application expects these environment variables:

```dotenv
STRIPE_SECRET_KEY=your_test_secret_key
STRIPE_PRICE_ID=your_test_price_id
PORT=5000
```

Never commit real keys or your `.env` file. Use Stripe **test mode** when developing.

## Before production use
- Remove tracked `node_modules` from version control (it is currently present in the repository history)
- Confirm dependencies and Node.js module configuration
- Replace placeholder callback URLs
- Add validation, appropriate access controls and Stripe webhook verification where required
- Review payment security, error handling, testing and deployment

This is a portfolio archive showing early API integration work, not a live payments backend.

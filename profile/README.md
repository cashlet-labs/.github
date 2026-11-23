# Cashlet Labs

Open-source tools for Bitcoin Cash identity and payments, built by [Septem Labs](https://septemlabs.com).

We work on one idea: a person should be able to prove that their Bitcoin Cash wallet and their Nostr identity belong together, without an account, a company or a fee. Then anyone can pay that person by `npub` and be sure the address is theirs.

## BND: Bitcoin Cash and Nostr identity binding

[**bnd**](https://github.com/cashlet-labs/bnd) is an open protocol. A BCH key and a Nostr key each sign a statement naming the other, and the result is published as an ordinary Nostr event. Any app can find it on relays and verify it offline.

On top of the binding, BND-1 defines login with both keys, key rotation and recovery with two of three keys, `did:bnd` (a DID that survives rotation), and paying an identity at its current, verified address.

- Specification and test vectors: [BND-1](https://github.com/cashlet-labs/bnd/blob/main/spec/BND-1.md), [did:bnd](https://github.com/cashlet-labs/bnd/blob/main/spec/did-bnd.md)
- Library: [`@cashlet-labs/bnd`](https://www.npmjs.com/package/@cashlet-labs/bnd) on npm
- Site: [bnd.septemlabs.com](https://bnd.septemlabs.com), with the live demo at [bnd.septemlabs.com/demo](https://bnd.septemlabs.com/demo)
- Status: the specification is a draft and may change before version 1.

## Cashlet: a wallet with BND built in

[**cashlet-wallet**](https://github.com/cashlet-labs/cashlet-wallet) is a self-custodial Bitcoin Cash wallet for Chrome. It sends and receives BCH and CashTokens, publishes your BND identity, pays any `npub` or `did:bnd`, signs for Nostr sites (NIP-07, NIP-04, NIP-44) and connects to dapps over WizardConnect. There is no Cashlet server or account.

Site and install: [extension.septemlabs.com](https://extension.septemlabs.com)

## Principles

- Open protocols over closed platforms.
- No identity provider: relays store events, apps check the signatures themselves.
- Reusable libraries first, so wallets and Nostr clients can adopt the protocol without asking permission.

## Get involved

Open an issue or a pull request on [bnd](https://github.com/cashlet-labs/bnd). Wallet and Nostr client builders: the [integration guide](https://github.com/cashlet-labs/bnd/blob/main/docs/integration.md) is the place to start. Contact: hello@septemlabs.com

Code is MIT. Specification text is CC BY 4.0.

## Support our work

Both projects are free and open. Donations in BCH or CashTokens keep the relays, the DID resolver, the demo and development going.

**BND**

![Support BND](https://raw.githubusercontent.com/cashlet-labs/bnd/main/docs/assets/support-bnd.png)

`bitcoincash:zplfhfkwgpc4ud8k99x97wz689tn0xm5psj0wx2tkt`

**Cashlet**

![Support Cashlet](https://raw.githubusercontent.com/cashlet-labs/cashlet-wallet/main/docs/support-cashlet.png)

`bitcoincash:zpwd6edurja89cdq7hppvzq6xxzj5ct58uqf9czcx9`

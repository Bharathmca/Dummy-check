# flush-blockchain-monitor

This repo contains the code for blockchain-monitoring. This is where the Blockcypher's webhooks post their notifications on.

This component does the following things:

1. Monitor the deposits made on Deposit wallet addresses.
2. Check for required number of confirmations.
3. Transfer the funds from Deposit Wallet to COLD_WALLET.
4. Monitor the withdrawals/deposits made from/to Withdrawal Wallet.
5. Record every transaction in database.
6. Update coin prices (in USD) every hour, in the database.

- There are 4 post routes each for monitoring the Deposits and the withdrawals. (checkout the src/server.ts)

- Check the .env.example to know about what you would need before starting up this component.

- This is what webhooks return for 'tx-confirmation' event.

## Installation

```bash
$ yarn install or npm install
```

```bash
# development
$ yarn run dev or npm run dev

```

## Environment variables

Please refer [.env.example](./.example.env) for the env variables that is needed

## Webhooks example

```
{
  "block_height": -1,
  "block_index": -1,
  "hash": "ccab8e9716d4bdfd8038e1cf6121679d0b48d1421ae65339d50f060bfae10542",
  "addresses": [
    "C3tM2Z8xrxPNibCFieEWyztqTQcvX3fiEz",
    "CFr99841LyMkyX5ZTGepY58rjXJhyNGXHf"
  ],
  "total": 84051,
  "fees": 10000,
  "size": 340,
  "vsize": 340,
  "preference": "low",
  "relayed_by": "127.0.0.1:42754",
  "received": "2021-05-24T07:19:58.047Z",
  "ver": 1,
  "double_spend": false,
  "vin_sz": 2,
  "vout_sz": 2,
  "confirmations": 0,
  "inputs": [
    {
      "prev_hash": "deac830f6c9ed205e5fe761a2de5d0e8ee24e8319932cafcbdc38551ed269597",
      "output_index": 1,
      "script": "483045022100840b3079d3427dfc543226f6062e8c7bfffd4b408b1154c930faa26c9ad4c42602204ed1f459a0076870f6142f068315f324290d08ecb34387b41bed7e0ed7882f97012102a44f60c94b840854db8c673e280dbc76b2975c6cf10e351ef6208f7f546e2130",
      "output_value": 17758,
      "sequence": 4294967295,
      "addresses": [
        "CFr99841LyMkyX5ZTGepY58rjXJhyNGXHf"
      ],
      "script_type": "pay-to-pubkey-hash",
      "age": 3397044
    },
    {
      "prev_hash": "ec7a258f100f1f498327f5967001996dbaf533af240573c52383ed078e311c82",
      "output_index": 0,
      "script": "483045022100831bb4844491a13b1f93bfe63a1a97ddfccc1e6bf89eea7f1edae7b2408649eb022059e181f677aa9f748ac24f827be84400c1c730813a86b32b35737ea614d63ad801",
      "output_value": 76293,
      "sequence": 4294967295,
      "addresses": [
        "CFr99841LyMkyX5ZTGepY58rjXJhyNGXHf"
      ],
      "script_type": "pay-to-pubkey",
      "age": 3397044
    }
  ],
  "outputs": [
    {
      "value": 10000,
      "script": "76a91476066ee5e20f7e90f54e4ea3918fdff40c3aefc788ac",
      "addresses": [
        "C3tM2Z8xrxPNibCFieEWyztqTQcvX3fiEz"
      ],
      "script_type": "pay-to-pubkey-hash"
    },
    {
      "value": 74051,
      "script": "76a914f93d302789520e8ca07affb76d4ba4b74ca3b3e688ac",
      "addresses": [
        "CFr99841LyMkyX5ZTGepY58rjXJhyNGXHf"
      ],
      "script_type": "pay-to-pubkey-hash"
    }
  ]
}
```

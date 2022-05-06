# About graphql-flush

this Repository act as a Gateway to all other microservices
following microservices are using to run the Flush Project

- Flush-casino-mine
- HILO
- Crash
- GRAPHQL(Main)
- Crash
- Blockchain Monitoring
- Betfeed
- admin graphql

- currently the master branch is demo and prod is production

---

# Slots and Livecasino Games Dependencies

1. softgaming
2. Oryx Gaming (implementation under progress)

# Other service

- Blockcypher
- Affilka
- banxa (buy crypto with feat currency Gateway)(implementation under progress)

---

## Installation

```bash
$ yarn install or npm install
```

## Environment variables

Please refer [.env.example](./.example.env) for the env variables that is needed

---

## Running the app

```bash
# development
$ yarn run dev or npm run dev

# to generate resolver-types.ts
$ yarn run generate or npm run generate
```

'resolver-types.ts' is generated using codegen. Following steps should be followed:

- Make the schema and resolvers
- start the server (also see codegen.yaml)
- run yarn generate or npm generate in another terminal (this will create/update resolver-types.ts)

No need to edit 'resolver-types.ts' (file which automatically created when we run npm run generate)

<h1 align="center">
  Readme-template
</h1>

![Deposit Flow](../assets/Deposit%20flow.jpg)

![Affilka Flow](../Dummy-check/asstes/Affilka.jpeg)

![payment Flow](./assets/Payments.pdf)

# About graphql-flush

this Repository act as a API_Gateway to all other microservices
following microservices are using to run the Flush Project

- Flush-casino-mine
- HILO
- Crash
- GRAPHQL(Main)
- Crash
- Blockchain Monitoring
- Betfeed
- admin graphql

---

- currently the master branch is demo and prod is production

---

# Slots and Livecasino Games Dependencies

1. softgaming
2. Oryx Gaming (implementation under progress)

---

# Other service

- Blockcypher
- Affilka
- banxa (buy crypto with feat currency Gateway)(implementation under progress)

---

'resolver-types.ts' is generated using codegen. Following steps should be followed:

- Make the schema and resolvers
- start the server (also see codegen.yaml)
- run yarn generate or npm generate in another terminal (this will create/update resolver-types.ts)

No need to edit 'resolver-types.ts' (file which automatically created when we run npm run generate)

# EthSupplyChainApp

create a new directory

cd into directory 

run `truffle init`

run `npm init`

create a directory for your UI / web3 app

`mkdir web`

`cd web`

`npm init`

maintain two NPMs b/c the web-app will most likely be bundled seperately from your solidity project. They may also have weirdly different dependencies.


add `touch .gitignore` 

update gitignore with preferred ignores

uncomment `truffle-config.js` development files

```
    development: {
      host: "127.0.0.1",     // Localhost (default: none)
      port: 8545,            // Standard Ethereum port (default: none)
      network_id: "*",       // Any network (default: none)
    },
```

run `truffle develop` ... `compile` .. `migrate --reset` to run truffle locally within a test environment. 

If you'd like to connect to a ganache running instance, e.g. on port 7545, then you need to skip over `truffle develop` and just run, `truffle compile` and `truffle migrate --reset`.  Or if you want to target a specific network, `truffle compile` and `truffle migrate --reset --network myCustomNetwork`
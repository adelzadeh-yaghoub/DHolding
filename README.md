# Decentral Holding Project and Token Smart Contracts

This repository consists of smart contracts required for DHC projct

#### How to run
- installation 
```
yarn install
yarn clean
yarn prepare

```

-   Deploy to testnet

```
yarn PROJECT_ID="infura id" PRIVATE_KEY="private key to deploy the contracts from" yarn deploy:rinkeby
```

-   Deploy to local (requires ganache to run on local)


You can find more information in the `scripts-info` section in the `package.json` file.


#### How to test
- run test files
```
yarn add hardhat
NODE_ENV=test npx hardhat test
```

#### How to deploy

-   Deploy to bsc_testnet

```

You will first need an API key from your account on https://bscscan.com/login

NODE_ENV=default PROJECT_ID="BSC API Key" PRIVATE_KEY=<your-private-key> npx hardhat deploy --network bsc_testnet
```

-   Deploy to bsc mainnet


```
NODE_ENV=production PROJECT_ID="BSC API Key" PRIVATE_KEY=<your-private-key> npx hardhat deploy --network bsc
```

-   Deploy to Polygon (Matic) mainnet

```
NODE_ENV=polygon_production PROJECT_ID="infura id" PRIVATE_KEY=<your-private-key> yarn deploy--network matic
```

#### How to verify a contract

- Verify on bsc_testnet

```
NODE_ENV=default ETHERSCAN_KEY=<your-api-key> npx hardhat verify --network bsc_testnet <contract-address> "First arg of constructor" "Second arg of constructor" "Third arg of constructor" "Fourth arg of constructor"

```

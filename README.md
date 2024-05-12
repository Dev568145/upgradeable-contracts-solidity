## Foundry UUPSUpgradeable Contract

This is a demo of an upgradeable contract.
Upgradeable contract should generally be avoided.

## Getting started

# Requirements

- git

  - You need to install git. Here are guidlines to install: https://github.com/git-guides/install-git

- foundry
  - How to install foundry you can find here: https://book.getfoundry.sh/getting-started/installation

# Quickstart

```
git clone https://github.com/Dev568145/foundry-upgrades-f23
cd foundry-upgrades-f23
forge build
```

# Usage

## Start local node

```
make anvil
```

# Deploy

In a new terminal window run:

```
make deploy
```

# Testing

```
forge test
```

for testing specific functions run:

```
forge test --mt 'function name'
```

## Testing Coverage

```
forge coverage
```

and for coverage based testing:

```
forge coverage --report debug
```

# Deploying to testnet or mainnet

1. Setup environment variables

   - You need to make a `.env` file were you add SEPOLIA_RPC_URL and PRIVATE_KEY as environment variables.
     - When deploying on testnet you should use a metamask wallet with no real funds for safety. Here you can find out how to export private key: https://support.metamask.io/managing-my-wallet/secret-recovery-phrase-and-private-keys/how-to-export-an-accounts-private-key/#:~:text=On%20the%20'Account%20details'%20page,private%20key%20to%20your%20clipboard.
     - Getting a sepolia rpc url you can get for free from alchemy. Here is the link: https://www.alchemy.com/
     - Optionally you can add ETHERSCAN_API_KEY for verifying contract when deploying. Here is a link: https://etherscan.io/

2. Fund you wallet with sepolia testnet ETH

   - Here is a faucet where you can get testnet ETH: https://www.alchemy.com/faucets/ethereum-sepolia

3. Deploy contract to testnet:

   ```
   make deploy ARGS="--network sepolia"
   ```

4. Upgrade contract

   ```
   make upgrade ARGS="--network sepolia"
   ```

## Estimating gas

You can estimat how much gas each function costs

```
forge snapshot
```

## Formatting

```
forge fmt
```

# Acknowledgments

I want to thank Patrick Collins and the team at Cyfrin for this contract. Check out Cyfrin here on github and Patrick Collins on youtube.

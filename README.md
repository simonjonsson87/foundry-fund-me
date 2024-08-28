

# Useful commands

Command used to install depency
```solidity
forge install smartcontractkit/chainlink-brownie-contracts@0.6.1 --no-commit
```

For the above to work the line below needs to be added under [profile.default] in foundry.toml
```
remappings = ['@chainlink/contracts/=lib/chainlink-brownie-contracts/contracts/']
```
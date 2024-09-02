

# Useful commands

Command used to install depency
```solidity
forge install smartcontractkit/chainlink-brownie-contracts@0.6.1 --no-commit
```

For the above to work the line below needs to be added under [profile.default] in foundry.toml
```
remappings = ['@chainlink/contracts/=lib/chainlink-brownie-contracts/contracts/']
```

To print console.log when running a test, you need at least double v's:
```
forge test -vv
```

If you have problems with the compiler complaining about not finding files that you have deleted (and that shouldn't be there). This clears build artifacts etc
```
forge clean
```
Run only specified test
```
forge test --mt testOwnerIsSender
```

This runs the tests on a forked environment. Data will be grabbed from sepolia to simulate that our test is being run on the sepolia chain, even though it's actually run on a local chain. Get Sepolia chain url from Alchemy.
```
forge coverage --fork-url $SEPOLIA_RPC_URL
```

Check test coverage
```
forge coverage
```
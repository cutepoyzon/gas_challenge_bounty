# Gas Optimization Bounty by StackUp

## Overview of Bounty

Gas is the unit of measurement for the computational work required to execute a transaction or deploy a smart contract on the Ethereum blockchain. Gas optimization techniques are important because they can significantly reduce the cost of deploying and executing smart contracts, making them more affordable for users.

This bounty challenges you to optimize a smart contract by applying the various listed gas optimization techniques. To complete this bounty, you must apply the techniques described below to the provided smart contract and write a simple unit test. Once you are done, upload your working files to your GitHub repository and submit the GitHub URL to successfully complete the bounty.

## Overview of Gas Optimization Techniques

To successfully complete this bounty, you will need to apply the following gas optimization techniques:

1. **Fixed Size over Dynamic Arrays**: Using fixed-size arrays instead of dynamic arrays can reduce gas consumption because Solidity has to perform less work to manage the memory allocation of arrays in the smart contract

2. **Caching State Variable**: Caching frequently accessed state variable can reduce gas consumption by reducing the number of storage reads required

3. **Implement Uncheck Block**: Using the `unchecked` block can reduce gas consumption by skipping certain checks such as integer overflows

4. **For Loop Increment Syntax**: Using a different for loop increment syntax can help reduce gas consumption

## Getting Started

To get started, clone this repository to your local machine and navigate to the project directory. Next, install the required dependencies.

```bash
git clone https://github.com/clement-stackup/gas_challenge.git
cd gas_challenge && npm install
```

Once you have cloned the repository and installed the necessary dependencies, open the `contracts/gasChallenge.sol` file to view the smart contract and apply the following gas optimization techniques above.

## Test Smart Contract

Next, head over to `test/test_gasChallenge.js`. You are required to write a unit test under the describe block to check that after running the gas optimized function, the sum of array is 0. Once you have implemented the test block, proceed the run the following command to test your smart contract.

```bash
npx hardhat test
```

This command will test the smart contract and compute the estimated gas cost. This is computed using the [hardhat-gas-reporter](https://www.npmjs.com/package/hardhat-gas-reporter) library.

The library has been configured to output the estimated gas costs to a `gas-report.txt` file. You can then view the estimated gas consumption for each of the smart contract functions in this file. The `optimizedFunction()` should output a lower gas consumption to the `notOptimizedFunction()`.

The command will also check that the sum of the array returns 0. You can refer below to visualise how the output should be generated

<img width="673" alt="image" src="https://github.com/clement-stackup/gas_challenge/assets/120361535/01237b5e-5cc6-4d53-9b55-ef13da282cb9">

## Bounty Submission

Upload all your working files to your GitHub Repository and submit your GitHub Repository URL to the StackUp Gas Optimization Challenge Bounty Page
## Introduction

Solidity is the primary language for writing smart contracts on blockchain platforms like Celo. However, once a contract is deployed on the blockchain, it is immutable, meaning it cannot be modified or upgraded. To overcome this limitation, a common pattern used is the Proxy pattern, allowing for contracts to be upgraded. This challenge will focus on implementing this pattern.

## Problem Statement

Design a simple proxy contract and an upgradeable contract that will interact with each other. The challenge is as follows:

1. Write an `Upgradeable` contract with a version number and a simple function to return the version number.
2. Write a `Proxy` contract that can delegate calls to the `Upgradeable` contract and upgrade the `Upgradeable` contract to a new version.
3. The `Proxy` contract should only allow itself to upgrade the `Upgradeable` contract.

## Hints

- Use `delegatecall` in the `Proxy` contract to forward calls to the current `Upgradeable` contract.
- To upgrade the `Upgradeable` contract, the `Proxy` contract should change the address to which it forwards calls.
- Use `require` to ensure that only the `Proxy` contract can upgrade the `Upgradeable` contract.

## Evaluation Criteria

- **Correctness**: The contract should compile without errors and fulfill all the requirements.
- **Readability**: The contract should be well-documented, with comments explaining the code.
- **Testability**: You should also provide examples of how to test each function of the contract.

Remember, handling real contracts on a blockchain requires extreme care and extensive testing. The upgrade pattern helps manage and upgrade contracts, but improper handling can lead to severe issues.

For a comprehensive understanding of Celo smart contracts and Solidity, please refer to the Celo and Solidity documentation.

## Submission

Please reply with a link to your PR on GitHub, including your proxy and upgradeable contracts. Also, include any notes or comments you think are necessary to understand your design and choices. Lastly, provide a brief explanation about how each function of the contract should be tested.

# Real Estate Tokenization Smart Contract

This repository contains a simplified example of a smart contract for tokenizing real estate assets on the Ethereum blockchain. It demonstrates the basic functionality of creating and transferring ownership of real estate asset tokens.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Smart Contract Overview](#smart-contract-overview)
- [Example Transactions](#example-transactions)
- [Contributing](#contributing)
- [License](#license)

## Prerequisites

To interact with this smart contract and run the provided example, you need:

- [Node.js](https://nodejs.org/) installed on your system.
- A development environment like [Truffle](https://www.trufflesuite.com/truffle) for compiling and deploying the smart contract.
- A development blockchain network like [Ganache](https://www.trufflesuite.com/ganache) for testing.

## Installation

1. Clone this repository to your local machine:

   ```bash
   git clone https://github.com/your-username/real-estate-tokenization.git
   ```

2. Navigate to the project directory:

   ```bash
   cd real-estate-tokenization
   ```

3. Install the project dependencies:

   ```bash
   npm install
   ```

## Usage

1. Compile and deploy the smart contract to your development blockchain using Truffle. Update the `truffle-config.js` file with your network configurations.

   ```bash
   truffle compile
   truffle migrate
   ```

2. Interact with the smart contract using the provided example scripts in the `scripts/` directory:

   - `createRealEstateAsset.js`: Creates a new real estate asset token.
   - `transferRealEstateAsset.js`: Transfers ownership of a real estate asset token to another address.

   For example, to create a new real estate asset token:

   ```bash
   truffle exec scripts/createRealEstateAsset.js --tokenId 1 --name "Luxury Condo" --price 1000000000000000000
   ```

3. You can also use Truffle's console to interact with the smart contract directly:

   ```bash
   truffle console
   ```

## Smart Contract Overview

The smart contract (`contracts/RealEstateToken.sol`) provides the following functionality:

- Creation of real estate asset tokens by the contract owner.
- Transfer of ownership of real estate asset tokens between addresses.
- Storage of real estate asset metadata, including name, token ID, price, and owner.

## Example Transactions

Here are some example transactions you can perform with the smart contract:

- Create a new real estate asset token:

  ```bash
  truffle exec scripts/createRealEstateAsset.js --tokenId 1 --name "Luxury Condo" --price 1000000000000000000
  ```

- Transfer ownership of a real estate asset token:

  ```bash
  truffle exec scripts/transferRealEstateAsset.js --tokenId 1 --to <receiver_address>
  ```

## Contributing

If you'd like to contribute to this project, please follow our [Contributing Guidelines](CONTRIBUTING.md).

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

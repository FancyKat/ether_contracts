# EIP 2981 Royalities NFT Contract

This project contains a Solidity smart contract for creating non-fungible tokens (NFTs) with royalty support. The contract is built using the OpenZeppelin Contracts library, which provides implementations of standards like ERC721.

## Features

- **ERC721 Compliant**: The contract creates NFTs that are compliant with the ERC721 standard, meaning they can be managed, transferred, and tracked consistently.

- **Enumerable**: The contract uses the ERC721Enumerable extension from OpenZeppelin, which provides a way to enumerate the tokens owned by an address and to enumerate all tokens in existence.

- **URI Storage**: The contract uses the ERC721URIStorage extension from OpenZeppelin, which provides a way to associate a URI with each token for metadata purposes.

- **Royalty Support**: The contract uses the ERC721Royalty extension from OpenZeppelin, which provides a way to set a royalty fee that is paid to the original creator of an NFT each time it is sold.

- **Ownable**: The contract uses the Ownable module from OpenZeppelin, which provides a way to restrict certain operations to the contract's owner.

## Contract Overview

The contract has several public and internal functions:

- **mint**: This function allows anyone to create a new NFT. The new NFT's ID is automatically set, and its URI is set based on the contract's `metadataURI` and the new token's ID. The new NFT's royalty information is also set, with the royalty recipient being the `artist` address and the royalty fee being the `royaltyFee`.

- **setRoyaltyFee**: This function allows the contract's owner to update the `royaltyFee` state variable, which is used when minting new NFTs.

- **_burn**: This internal function is used to burn (destroy) an NFT. It also resets the NFT's royalty information.

- **tokenURI**: This function returns the URI associated with a given NFT.

- **_beforeTokenTransfer**: This internal function is called before an NFT is transferred (including minting and burning). It is used to update the contract's internal state.

- **supportsInterface**: This function is used to check which interfaces the contract supports.

## Getting Started

To interact with this contract, you will need to have a development environment set up with [Hardhat](https://hardhat.org/getting-started/) and [ethers.js](https://docs.ethers.io/v5/). You can then compile the contract with `npx hardhat compile`, and run tests with `npx hardhat test`.

For more information on how to use this contract, please refer to the [OpenZeppelin Contracts documentation](https://docs.openzeppelin.com/contracts/4.x/).


Sure, here's a section you can add to your README for testing the project:

## Testing the Project

**Install the dependencies**:

```bash
npm install
```

**Run the tests**:

```bash
npx hardhat test
```

You should see output in your terminal showing the results of the tests.

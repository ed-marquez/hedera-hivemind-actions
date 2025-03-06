## Hedera Mirror Node API

The `action.yaml` file defines the API endpoints for interacting with the Hedera Mirror Node. This API allows you to retrieve public blockchain data from the Hedera Hashgraph network. Below is a summary of the endpoints available:

## Endpoints

### Accounts

- **/accounts**
  - **GET**: Retrieve a list of blockchain accounts.
- **/accounts/{idOrAliasOrEvmAddress}**
  - **GET**: Retrieve public information about a blockchain account.
- **/accounts/{idOrAliasOrEvmAddress}/allowances/crypto**
  - **GET**: Retrieve granted HBAR allowances.
- **/accounts/{idOrAliasOrEvmAddress}/allowances/tokens**
  - **GET**: Retrieve granted token allowances.
- **/accounts/{idOrAliasOrEvmAddress}/allowances/nfts**
  - **GET**: Retrieve granted NFT allowances.
- **/accounts/{idOrAliasOrEvmAddress}/rewards**
  - **GET**: Retrieve staking rewards history.
- **/accounts/{idOrAliasOrEvmAddress}/nfts**
  - **GET**: Retrieve NFTs owned by a blockchain account.

### Airdrops

- **/accounts/{idOrAliasOrEvmAddress}/airdrops/outstanding**
  - **GET**: Retrieve outstanding token airdrops.
- **/accounts/{idOrAliasOrEvmAddress}/airdrops/pending**
  - **GET**: Retrieve pending token airdrops.

### Balances

- **/balances**
  - **GET**: Retrieve account balances.

### Tokens

- **/tokens**
  - **GET**: Retrieve a list of tokens.
- **/tokens/{id}**
  - **GET**: Retrieve details of a token.
- **/tokens/balances**
  - **GET**: Retrieve token balances across accounts.
- **/tokens/nfts**
  - **GET**: Retrieve a list of NFTs.
- **/tokens/nfts/{serialNumber}**
  - **GET**: Retrieve NFT details.
- **/tokens/nfts/{id}/transactions**
  - **GET**: Retrieve NFT transaction history.

### Topics

- **/topics/{topicId}**
  - **GET**: Retrieve details for a specific topic.
- **/topics/{topicId}/messages**
  - **GET**: Retrieve messages for a specific topic.
- **/topics/{topicId}/messages/{sequenceNumber}**
  - **GET**: Retrieve a specific message from a topic by sequence number.
- **/topics/{topicId}/messages/{consensusTimestamp}**
  - **GET**: Retrieve a topic message by consensus timestamp.

### Transactions

- **/transactions**
  - **GET**: Retrieve a list of blockchain transactions.
- **/transactions/{id}**
  - **GET**: Retrieve details of a blockchain transaction.

## Description

Each endpoint is designed to fetch specific data from the Hedera network. For example, you can retrieve details about tokens, NFTs, account balances, and transaction histories. The API uses standard HTTP methods and returns data in JSON format.

## Parameters

Some endpoints require parameters to be passed in the URL path, such as account IDs or token IDs. These parameters are specified in the `parameters` section of each endpoint definition.

## Responses

The responses section of each endpoint defines the structure of the data returned by the API. This includes the types of data and their properties, ensuring that you know what to expect when making a request.

This API is essential for developers looking to integrate Hedera blockchain data into their applications, providing a comprehensive set of tools for accessing and managing blockchain information.

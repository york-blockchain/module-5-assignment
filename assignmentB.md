## Description

### Follow the steps to deploy an ERC721 contract to the rinkeby network and register with opensea.

- clone the github repository from [https://github.com/york-blockchain/opensea-creatures](https://github.com/york-blockchain/opensea-creatures) 
 
- Get some test ethers from rinkeby using one of the following links if you don't already have some :

[https://faucets.blockxlabs.com](https://faucets.blockxlabs.com) 

[https://faucet.rinkeby.io](https://faucet.rinkeby.io) 

- Update the `Creature.sol` file with your token symbol and name then check this in to github

[https://github.com/york-blockchain/opensea-creatures/blob/master/contracts/Creature.sol#L11](https://github.com/york-blockchain/opensea-creatures/blob/master/contracts/Creature.sol#L11) 

- Copy the `.env.sample` file to `.env` and update `.env` with all required values.
 >Note: get private key and address from metamask

- Get the projectID by signing up at [https://infura.io](https://infura.io) and update `.env` with your INFURA_KEY.

- Run the npm command to test the contracts, make sure all runs green
```sh
$ npm install
$ npm test
``` 
- Run the npm command to deploy your contract to the rinkeby network
```sh
$ npm run deploy-rinkeby
```

- Update `.env`, set NFT_CONTRACT_ADDRESS to your contract address.

- run the `script/mint.js` to mint a token:  
```sh
$ node script/mint.js
```

- Goto Opensea to register your token by providing them your contract address

[https://rinkeby.opensea.io/get-listed/step-two](https://rinkeby.opensea.io/get-listed/step-two) 

- check that your token is listed on Opensea
e.g. if your account that owns the token is `0xDa1d30af457b8386083C66c9Df7A86269bEbFDF8`:

[https://rinkeby.opensea.io/accounts/0xDa1d30af457b8386083C66c9Df7A86269bEbFDF8](https://rinkeby.opensea.io/accounts/0xDa1d30af457b8386083C66c9Df7A86269bEbFDF8) 

Make a submission of the link similar to the above example.

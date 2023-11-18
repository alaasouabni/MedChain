

<h4 align="center">A blockchain-based Electrical Medical Records (EMR) system.</h4>

<p align="center">
  <a href="#key-features">Key Features</a> •
  <a href="#how-it-works">How It Works</a> •
  <a href="#how-to-use">How To Use</a> •
</p>

## Key Features

MedChain is powered by [IPFS](https://ipfs.tech/), where every patient's medical records are stored on the distributed file system, not owned by any centralized entity like hospitals or governments. Each patient has a digital identity on [Ethereum](https://ethereum.org/) blockchain, who and whose doctor can access medical records by interacting with smart contracts. 

On MedChain,

- A healthcare provider can register using a crypto wallet like Metamask.
- The healthcare provider can register a patient by using the public address of the patient’s wallet, usually provided during an appointment.
- The health provider can search for a patient’s records using the address, and upload a new record for the patient. 
- The patient can also view his or her records, after connected with a wallet which address is registered by the health provider.

## How It Works

There are three major components of MedChain:

1. React client (connected with MetaMask)
2. Solidity smart contract on Ethereum blockchain
3. Interplanetary file system (IPFS)

<p align="center">
<img src="https://d112y698adiu2z.cloudfront.net/photos/production/software_photos/002/187/785/datas/original.png" width="700"/>
</p>

The client first connects with crypto wallet, and use smart contract to mint a patient or doctor block if the public address of the user’s wallet is not registered.

The client can upload a record file to IPFS, which address is linked to a patient block in ETH chain. The client can get all record addressed stored in a patient block from smart contract, and get a record file by its address from IPFS.

## How To Use

Make sure to use Node 16.X. You can follow this tutorial to install Node 16: [nvm](https://heynode.com/tutorial/install-nodejs-locally-nvm/).

Install Truffle globally if you haven't.

```sh
$ npm install -g truffle
```
Install Ganache and start a local ethereum workspace using the QUICKSTART ETHEREUM button in the Ganache Program Interface. You can follow this tutorial: [Ganache](https://trufflesuite.com/docs/ganache/quickstart/).

Install Truffle dependencies and deploy smart contracts to local Ethereum network like [Ganache](https://trufflesuite.com/ganache/). 

```sh
$ cd truffle
$ npm install
$ truffle compile
$ truffle deploy
```

Install React dependencies and start React app. 

```sh
$ cd ../client
$ yarn
$ yarn start
```

You should be able to see the application running at http://localhost:3000.

You should now configure metamask to connect to the local Ganache node following this tutorial: [MetaMask](https://www.geeksforgeeks.org/how-to-set-up-ganche-with-metamask/).



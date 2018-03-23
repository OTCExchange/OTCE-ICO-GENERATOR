# ICO GENERATOR Https://otcexchange.info

For a live demo, see https://otcexchange.info. This simple app allows anyone with an Ethereum account and some Ether to deploy their own crowdsale contract with no coding knowledge (the user only enters some basic information such as their token name and symbol, and their crowdsale contract is deployed on the Ethereum network). 

See ICO.sol in the /contracts directory for the contract that is deployed - you can see the constructor function takes some basic parameters to set the characteristics of the token when the contract is deployed. ICO.sol is an ERC20 compliant token contract that uses SafeMath.sol from OpenZeppelin to protect against overflow/underflow attacks. It also transfers all Ether it receives to the address that deployed it, and accepts an unlimited amount of Ether.

Rather than generating the ABI and bytecode of ICO.sol each time time a contract is deployed, the ABI and bytecode are simply hardcoded in the app.js file. The Web3 Javascript library is used to allow the webpage to deploy and interact with contracts.

## UPDATES

![#c5f015](https://placehold.it/15/c5f015/000000?text=+)  March 23rd 2018 - ICO Contract Generator V2.0.0 RC-1 is now live! Https://otcexchange.info We have also included in-site support and we are working on release and FAQ documents. 

![#c5f015](https://placehold.it/15/c5f015/000000?text=+)  March 21st 2018 - Just finished the coding for V2.0, the new UI is still a little buggy and running into a few issues with the system distinguishing between ethereum / metamask networks (ie) mainnet vs. testnets. Should have the bugs worked out and a stable BETA up for everyone before the weekend.  

## NEW ICO GENERATOR UI

![#c5f015](https://placehold.it/15/c5f015/000000?text=+)  The idea behind ICO Generator was to develop an automated ICO, crowdsale, coin, token smart contract deployment platform that can be used by someone with no prior coding experience what so ever. The ICO Generator walks you through the process with a Q&A step by step UI while additionally providing helpful, easy to understand insight support each step of the way.

We also have added the ability to work with your newly deployed ICO contract from within our web app. 

## HOW TO DEPLOY

Simply upload the /build folder to a webserver. No configuration is necessary.

## HOW TO WORK WITH FILES

Install truffle with webpack and cd to an empty directory

## TRUFFLE INIT WEBPACK

Copy the contents of the /app and /contracts directories in this repository to those folders in your truffle project

Edit migrations/2_deploy_contracts.js so it deploys ICO.sol, eg:

var ICO = artifacts.require("./ICO.sol"); module.exports = function(deployer) { deployer.deploy(ICO); };

Then after making any changes to the /app folder, build the project with

npm run build

This will generate a /build folder that's ready to be used. To test the app on localhost:8080, run

npm run dev

## INTERACT WITH YOUR CONTRACT: 

- balanceOf() - returns the token balance of an address
- transfer() - transfers tokens to an address
- transferFrom() - transfers tokens to an address from an address other than
your own (requires approve() to have been called from whoever's account you're transferring tokens from)
- approve() - approves someone else to spend a certain amount of your tokens
- allowance() - check how many tokens an account is allowed to spend from another account

![#c5f015](https://placehold.it/15/c5f015/000000?text=+)  As a part of the new UI introduction to ICO Generator V2.0 we have improved the user site experience with a smoother usability flow. *(see flow chart below). 

## UI FLOW CHART & SCREENSHOTS

![Alt text](https://github.com/OTCExchange/OTCE-ICO-CREATOR/blob/master/README%20IMGS/ICO-USER-FLOW.png?raw=true "OTC ICO GENERATOR UI FLOW CHART")

![Alt text](https://github.com/OTCExchange/OTCE-ICO-GENERATOR/blob/master/README%20IMGS/screen1.png?raw=true "OTC ICO GENERATOR UI FLOW CHART")

![Alt text](https://github.com/OTCExchange/OTCE-ICO-GENERATOR/blob/master/README%20IMGS/screen2.png?raw=true "OTC ICO GENERATOR UI FLOW CHART")

![Alt text](https://github.com/OTCExchange/OTCE-ICO-GENERATOR/blob/master/README%20IMGS/screen3.png?raw=true "OTC ICO GENERATOR UI FLOW CHART")

![Alt text](https://github.com/OTCExchange/OTCE-ICO-GENERATOR/blob/master/README%20IMGS/screen4.png?raw=true "OTC ICO GENERATOR UI FLOW CHART")

![Alt text](https://github.com/OTCExchange/OTCE-ICO-GENERATOR/blob/master/README%20IMGS/screen5.png?raw=true "OTC ICO GENERATOR UI FLOW CHART")

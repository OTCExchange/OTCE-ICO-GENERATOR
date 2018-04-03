# ICO GENERATOR 2.0.0 PLATFORM OVERVIEW

For a live demo, see https://ico.otcexchange.net This simple app allows anyone with an Ethereum account and some Ether to deploy their own crowdsale contract with no coding knowledge. The user only enters some basic information such as their token name and symbol, and their crowdsale contract is deployed on the [Ethereum network](https://www.ethereum.org/).

Blockchain technology, with the application of well-programmed smart contracts, has the capacity to significantly improve control, security and privacy over the exchange of digital assets and information.

The problem, however, is the complexity of writing a smart contract. Smart contracts must be coded in Solidity, a contract-oriented, high-level language that is well known, currently, by just a small percent of developers worldwide. And while that figure is most likely increasing as each month passes, it’s a considerable barrier to entry for the vast majority of the general population of computer users leaving businesses and less computer-savvy individuals marginalized from this new and exciting emerging technology.

A Deloitte survey conducted this year indicated, “Nearly 40 percent of surveyed senior executives still have little or no knowledge about blockchain, while other executives place it among their company’s highest priorities for 2017.”

Nevertheless, accessibility to smart contract creation is upon us. The [OTCE ICO platform](https://otcexchange.company), currently nearing the end of its [OTCE R-1 token crowdsale](https://otcexchange.company/token/), is to smart contract creation what WordPress or Squarespace is to web development.

ICO Generator is, at its core, a smart contract creation tool that will allow any user to create an executable smart contract on the Ethereum blockchain. In effect, the ICO Generator platform will enable anyone, even those without any programming or coding experience, to harness the power of distributed computing by making smart contract creation as simple as filling out an online form.

The early 2.0.0 version of the platform includes an escrow contract, a token creation contract and a crowdfund contract for users to test and deploy. Once you have deployed a "LIVE" contract there are some additional feature that you can do to work with your contract in the ICO Generator web platform: 

## ESCROW

Escrow is when a financial instrument or digital asset is held by a third party on behalf of the other two parties in a transaction. An ICO Generator escrow smart contract takes the traditional legal concept and automates and enforces it via the blockchain, with the terms written and tailored within the digital contract itself. Currency, securities, funds, and other assets can all be held in escrow.

## TOKEN CREATION

Create an [ERC-20](https://theethereum.wiki/w/index.php/ERC20_Token_Standard) token in mere minutes. An essential, perhaps even foundational element, of any blockchain-based venture is the creation of a unique, digital token. The ICO Generator platform takes the complex development process and condenses it into a simple online form, in a bug-free, fully audited smart contract.

## CROWDFUND

Compile a token crowdfund contract in just a handful of clicks. What is typically a four- to six-week endeavor is simplified into a single-sitting at the computer with the ICO Generator platform. Develop ment should not be the main preoccupation of a blockchain project; planning and designing the business model for what lies ahead should be.

## ADDITIONAL ICO GENERATOR SUPPORT

Support is currently available through our ICO Generator Site located at https://ico.otcexchange.net by clicking on the support button in the bottom right hand corner of the page.

## WHATS NEXT

The ICO Generator platform will be expanding smart contract options offered to users with a fully-formed suite of templates to choose from. Version 1.0.0 of the platform was made available as of Oct. 1st, 2017 with an updated version 2.0.0 of the platform released in March 2018.

The ICO Generator V3.0.0 platform will offer a wide selection of smart contracts that range across multiple industries, SEC compliant securities token offerings to peer-to-peer wagering, supply chain management, real estate agreements, insurance and many more platform enhancements. The OTC ICO Network is powered by the use of its in-app currency, OTCE Token to run the OTC ICO Platform Network, the platform boast several additional ICO featured services and tools, [OTC Coindex](https://trade.otcexchange.net), [Crypto Directory](https://dir.otcexchange.net) and the ICO DB. A full list of current and future service can be found at our [corporate website](https://otcexchange.company). 

## LATEST DEVELOPMENT UPDATES

March 23rd 2018 - ICO Contract Generator V2.0.0 RC-1 is now live! https://ico.otcexchange.net We have also included in-site support and we are working on release and FAQ documents. 

March 21st 2018 - Just finished the code clean up for V2.0.0 RC-1, the new UI is still a little buggy and running into a few issues with the system distinguishing between ethereum / metamask networks (ie) mainnet vs. testnets. Should have the bugs worked out and a stable BETA up for everyone before the weekend.  

NEW ICO GENERATOR UI - The original idea behind the ICO Generator was to provide an automated ICO, crowdsale, coin, token smart contract deployment platform that can be used by someone with no prior coding experience what so ever. The ICO Generator walks you through the process with a Q&A step by step UI while additionally providing helpful, easy to understand insight support each step of the way. We also have added the ability to work with your newly deployed ICO contract from within our web app.

## USER SYSTEM REQUIREMENTS

- You must have [Metamask](https://metamask.io/) installed, tested with the [Chrome, Firefox, and Opera Extention](https://chrome.google.com/webstore/detail/nkbihfbeogaeaoehlefnkodbefgpgknn).

- You must be logged into Metamask : [Please watch the metamask video](https://www.youtube.com/watch?time_continue=34&v=6Gf_kRE4MJU)

- You must be connected to one of the "Test Networks" or the "Main Network" : [Please watch the metamask video](https://www.youtube.com/watch?time_continue=34&v=6Gf_kRE4MJU)

- We suggest you connect to the "Ropsten Test Network" and test your contract first (cost nothing to test)

- You will need to get some ["Test Ether" to test your "Test Contract"](https://blog.bankex.org/how-to-buy-ethereum-using-metamask-ccea0703daec)

- After you test your contract then you can connect to the "Main Network" and deploy your final contract

- Remember: You will need aprox $15 USD to deploy your final contract on the "Main Network"

## HOW TO DEPLOY YOUR OWN ICO SYSTEM

Simply upload the /build folder to a webserver. No configuration is necessary.

See ICO.sol in the /contracts directory for the contract that is deployed - you can see the constructor function takes some basic parameters to set the characteristics of the token when the contract is deployed. ICO.sol is an ERC20 compliant token contract that uses SafeMath.sol from OpenZeppelin to protect against overflow/underflow attacks. It also transfers all Ether it receives to the address that deployed it, and accepts an unlimited amount of Ether.

Rather than generating the ABI and bytecode of ICO.sol each time time a contract is deployed, the ABI and bytecode are simply hardcoded in the app.js file. The Web3 Javascript library is used to allow the webpage to deploy and interact with contracts.

## DEVELOPERS: HOW TO WORK WITH OUR PLATFORM FILES

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

As a part of the new UI introduction to ICO Generator V2.0 we have improved the user site experience with a smoother usability flow. *(see flow chart below). 

## NEW UI FLOW CHART & SCREENSHOTS

![Alt text](https://github.com/OTCExchange/OTCE-ICO-CREATOR/blob/master/README%20IMGS/ICO-USER-FLOW.png?raw=true "OTC ICO GENERATOR UI FLOW CHART")

![Alt text](https://github.com/OTCExchange/OTCE-ICO-GENERATOR/blob/master/README%20IMGS/screen1.png?raw=true "OTC ICO GENERATOR UI SCREEN 1")

![Alt text](https://github.com/OTCExchange/OTCE-ICO-GENERATOR/blob/master/README%20IMGS/screen2.png?raw=true "OTC ICO GENERATOR UI SCREEN 2")

![Alt text](https://github.com/OTCExchange/OTCE-ICO-GENERATOR/blob/master/README%20IMGS/screen3.png?raw=true "OTC ICO GENERATOR UI SCREEN 3")

![Alt text](https://github.com/OTCExchange/OTCE-ICO-GENERATOR/blob/master/README%20IMGS/screen4.png?raw=true "OTC ICO GENERATOR UI SCREEN 4")

![Alt text](https://github.com/OTCExchange/OTCE-ICO-GENERATOR/blob/master/README%20IMGS/screen5.png?raw=true "OTC ICO GENERATOR UI SCREEN 5")

## NOTICE TO ALL DEVELOPERS, PARTICIPANTS AND USERS

The Smart Contract System concept, the underlying software application and software platform (i.e. the Ethereum blockchain), is still in an early development stage and unproven. There is no warranty or assurance that the process for creating Tokens will be uninterrupted or error-free and there is an inherent risk that the software could contain defects, weaknesses, vulnerabilities, viruses or bugs causing, inter alia, the complete loss of ETH contributions and/or Tokens. Additionally, there are other risks associated with your acquisition, storage, transfer and use of Tokens, including those that OTCE may not be able to anticipate. Such risks may further materialize as unanticipated variations or combinations of the risks set out in the Contribution terms.

Blockchain technology allows new forms of interaction and it is possible that certain jurisdictions will apply existing regulations on, or introduce new regulations addressing, blockchain technology based applications, which may be contrary to the current setup of the Smart Contract System and which may, inter alia, result in substantial modifications of the Smart Contract System, including its termination and the loss of OTCE Tokens. Further, it is the users responsibly to ensure that his engagement on this website and with ETH contributions and/or Tokens is not in contravention of any law and legislation in the jurisdiction in which he resides.

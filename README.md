<p align="center">
  <a href="" rel="noopener">

</p>

<h1 align="center">E-Voting Using Blockchain🗳️</h1>


<p align="center"> A Blockchain based voting application using solidity, truffle and nodejs.
    <br> 
</p>

----

## 📝 Table of Contents

- [About](#about)
- [Getting Started](#getting_started)
- [Deployment](#deployment)
- [Usage](#usage)
- [Built Using](#built_using)
- [Screenshots](#screenshots)

----

## 🧐 About <a name = "about"></a>

A democratic country is built on the foundations of elections. Election is one of the founding pillars of any democracy and hence it is imperative that this process is carried out in the most secure and transparent way. Existing voting systems are centralized in nature, are susceptibly to tampering, and have often raised suspicion among the common people.

So through this project, I aim to build a decentralized voting application where all voters will be able to register, cast their vote and personally verify these votes. In this project we have assumed that we are given with the database of voter, which have aadhaar and other credentials.

----

## 🏁 Getting Started <a name = "getting_started"></a>

BlockVote web application uses <b>node.js</b> along with the <b>express.js</b> framework to develop the server and <b>mongoDB</b> as database and <b>mongoose</b> as object data modeling library. For the blockchain aspect, we have used the <b>ethereum</b> blockchain to deploy the smart contracts and <b>web3.js</b> library to interact with the ethereum node and the frontend. We have used <b>Ganache</b> and <b>Truffle</b> for creating a remote Blockchain environment.

### Prerequisites

The following dependencies need to be installed.

```
  - node.js
  - npm
  - mongodb / mongodb atlas
  - web3.js
  - Ganache
  - Truffle
```

### Installing ⬇️

Retrieve the project (clone the repository using the command)

  ```git
    git clone https://github.com/Anish-U/BlockVote.git
  ```

After cloning the repository, navigate into the directory and run the following command to install all the dependencies 

  ```
    npm install
  ```

### Setting up database📦 and env

Setup the environment variables by creating .env file in root directory

  ```
    PORT = 3000
    DB_URI = "mongodb://localhost:27017/BlockVote"
    GANACHE_URI = "http://localhost:7545"
    SESSION_SECRET = "SESSION_SECRET_KEY_HERE"
    JWT_KEY = "JWT_SECRET_KEY_HERE"
  ```

Add few voters and one admin into database as we assume that the application is already given with the voter details.

  ```
    // MongoDB CLI
    
    db.voters.insertOne(
      {
        aadhaar: "234567892345", 
        name: "Ummenthala Anish", 
        password:"$2a$12$s1Ue2JOpIq2Vk/H3HjDFgeNtvxRM4tGBCyZr6Nw4SOIf/75LISEm2", 
        gender:"male"
      }
    )

    db.admins.insertOne(
      {
        username: "admin", 
        password:"$2a$12$s1Ue2JOpIq2Vk/H3HjDFgeNtvxRM4tGBCyZr6Nw4SOIf/75LISEm2", 
      }
    )
  ```
  <small>Note: Password hash can be generated at [Bcrypt](https://bcrypt-generator.com/)</small>

### Setting up Blockchain⛓️ environment


Run ganache application in the background

Open the terminal and compile the Smart Contract to create the ABI of the smart contract and network id.

After compiling we need to migrate the contracts.

  ```
    truffle compile
    truffle migrate --reset
  ```

----

## 🚀 Deployment <a name = "deployment"></a>

In another terminal, run the command

  ```
    npm run devStart (or) node server.js
  ```

When the command runs successfully. Go to localhost:3000 there you will land on the home page of the project.

----

## ⛏️ Built Using <a name = "built_using"></a>

- [MongoDB](https://www.mongodb.com/) - Database
- [Express](https://expressjs.com/) - Server Framework
- [NodeJs](https://nodejs.org/en/) - Server Environment
- [Solidity](https://docs.soliditylang.org/en/v0.8.10/) - Used to develop Smart contracts 
- [Truffle](https://www.trufflesuite.com/docs/truffle/overview) - Development environment, testing framework for blockchains
- [Ganache](https://www.trufflesuite.com/docs/ganache/overview) - Personal blockchain for rapid Ethereum distributed application development
- [Web3JS](https://web3js.readthedocs.io/en/v1.5.2/) - Library that allow you to interact with a local or remote ethereum node.

----

## 📸 Screenshots <a name = "screenshots"></a>

#### Home Page
<center>
<img src="" width="700">
</center>


#### Admin: HomePage
<center>
<img src="https://github.com/kvm22/E-Voting-using-Blockchain/blob/main/Home1.png" width="700">
</center>

#### Admin: HomePage2
<center>
<img src="https://github.com/kvm22/E-Voting-using-Blockchain/blob/main/Home2.png" width="700">
</center>

#### Admin: Genache
<center>
<img src="https://github.com/kvm22/E-Voting-using-Blockchain/blob/main/Genache.png" width="700">
</center>

#### Voter: Ethereum Account Registration
<center>
<img src="https://github.com/kvm22/E-Voting-using-Blockchain/blob/main/Genache%20Etherium.png="700">
</center>

#### Voter: Metamask Connect
<center>
<img src="https://github.com/kvm22/E-Voting-using-Blockchain/blob/main/Metamask%20connect.png="700">
</center>

#### Voter: Voting
<center>
<img src="https://github.com/kvm22/E-Voting-using-Blockchain/blob/main/Vote%20for%20Candidate.png" width="700">
</center>

#### Team: Kunwar Vabhav Mishra
<center>
<img src="https://github.com/kvm22/E-Voting-using-Blockchain/blob/main/Vabhav.png" width="700">
</center>


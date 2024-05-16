# BCT Project

## 📝 Problem statement :
"Summary: To be able to graduate to objective type questions for one semester of online board exams, a question bank of at least 5000 questions will be required for each subject. Setting question papers for the exams is a complicated task. Can you think of a Crowd Sourcing model where questions are set by large number of anonymous stakeholders thereby creating a large question bank? These questions can be vetted by experts before freezing the same in the question bank. The actual question paper can be set through an automated system"

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


## 🚩 Overview :
Getting fine grained questions for board examinations is a difficult and time consuming task. Along with this setting examination paper taking into consideration various paprameters such as difficulty, weightage is quite error-prone. The question paper that is generated should be secured in a proper and effective manner to prevent any mishap such as leaking of paper. Sending question paper to the students across the network should be in a highly secure environment. So our team proposed a solution to tackle all this. We developed an online decentralized crowdsource model to have stakeholders contribute questions on our platform which will be later vetted by experts and using them to generate a question paper. The question paper generated would be encrypted and send across the network to the third party blockchain and would be distributed to the students whenever required and would ensure a secure and smooth process of sending question paper to the students who registered for it. 


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 🚩 General Features and Interfaces:
Feature | Images
------------ | -------------
 **Hompage**  
 Fast, easy to use, and incredibly convenient with a minimalistic UI! |![image](https://github.com/menonjayraj79/bctproj/assets/98472217/c4d1ba00-2dc4-4303-b74e-249ef0558177)
**Contributor Dashboard** 
All the accepted questions are shown here|![image](https://github.com/menonjayraj79/bctproj/assets/98472217/467c945e-8d3f-43e4-9982-48d86753b884)

**Teacher Expert Dashboard**
Experts after secure authentication can access all the features provided to them through this dashboard |![image](https://github.com/menonjayraj79/bctproj/assets/98472217/4ca81b56-7fb8-4ea6-b0d9-2af1e6d4389d)

**Add Question Section**
Stakeholders can add questions throught this interface with ease |![image](https://github.com/menonjayraj79/bctproj/assets/98472217/05a1471a-89cf-4ddd-b0a6-1088bb918a83)

**Virtual keyboard**
Virtual mathematical keyboard to ease the process of typing any mathematical equation |![image](https://github.com/menonjayraj79/bctproj/assets/98472217/5e5088e5-e63a-4021-97c1-03d950777570)

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 🔐 Expert authentication system
Expert's authentication can be the primary security breach to the board's question paper generation and distribution.
The diagram below shows all steps to generate the expert's login data hash from the username, the password, the 6 digit code (that will be provided by respective board to each teacher expert) and the ethereum address. To register the user must fill a form to provide the username, the password and the 6 digit code, the ethereum address is retrieved directly from the wallet. This address is associated to the username to generate a signature via the web3 function sign, the generated signature is hashed (hash1). The password is associated with the 6 digit code to generate another hash (hash2). The two hashes are combined to generated the final hash that is stored in the smart contract(Refer Authentication.sol). To login, the user must be connected to the Blockchain with the same address used during registration, and fill the login form with right username, password and the 6 digit code. The back-end solidity code then generates the hash with this login information and compares it with the hash that was stored in the smart contract by the ethereum address which request the login, if the two hashes match, then the user is authorized to login, if not, the access is denied.
![image](https://github.com/menonjayraj79/bctproj/assets/98472217/ce960621-bccd-47b8-a58e-8985eab523a0)


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


## 🌐 Web flow
![image](https://github.com/menonjayraj79/bctproj/assets/98472217/22536ba1-283c-4fdd-9711-ecf0286f2839)

![image](https://github.com/menonjayraj79/bctproj/assets/98472217/d6829732-2664-4e13-8017-f4d6eecf254a)


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)



##  🚩 Technologies used:

#### Programming Languages : Solidity, Javascript, HTML, CSS
#### Face Recognition Model :  TensorflowJS
#### Database : Polygon (Ethereum Layer-2) Blockchain
####  Frameworks/Libraries/Tools : Bootstrap, FreeOCR, Google Transalate, Truffle, Ganache, VSCode, IPFS, Moralis, Web3, Tokenizer
#### Version Control : Git
###### You can also see the list of dependencies in the package.json file.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

## 🚩Installation/Environment Setup 

  #### 1. Clone App
  
  * Write the following command and press enter.
  
  ```
    $ git clone https://github.com/menonjayraj79/bctproj
  ```
    
 #### 2. Install node packages
  * Move to the parent/root directory (CrowdQuest) cd CrowdQuest
  * Write the following command and press enter to download all required node modules.
 
   ```
   $ cd CrowdQuest
   $ npm install 
  ```
  
#### 3. Ganache
  - Open Ganache and click on settings in the top right corner.
  - Under **Server** tab:
    - Set Hostname to 127.0.0.1 -lo
    - Set Port Number to 8545
    - Enable Automine
  - Under **Accounts & Keys** tab:
    - Enable Autogenerate HD Mnemonic

#### 4. IPFS
  - Fire up your terminal and run `ipfs init`
  - Then run 
    ```
    ipfs config --json API.HTTPHeaders.Access-Control-Allow-Origin "['*']"
    ipfs config --json API.HTTPHeaders.Access-Control-Allow-Credentials "['true']"
    ipfs config --json API.HTTPHeaders.Access-Control-Allow-Methods "['PUT', 'POST', 'GET']"
    ```

    > Note: If you face any issues with the above command on windows, try using command prompt and escape sequences or git bash.
#### 5. Metamask
  - After installing Metamask, click on the metamask icon on your browser.
  - Click on __TRY IT NOW__, if there is an announcement saying a new version of Metamask is available.
  - Click on continue and accept all the terms and conditions after reading them.
  - Stop when Metamask asks you to create a new password. We will come back to this after deploying the contract in the next section.
  
#### 6. Smart Contract

1. Install Truffle using `npm install truffle -g`
2. Compile Contracts using `truffle compile`

#### 7. Starting your local development blockchain
  - Open Ganache.
  - Make sure to configure it the way mentioned above.
    7.1. Open new Terminal and deploy contracts using `truffle migrate`

#### 8. Local server

1. Install Node lite-server by running the following command on your terminal `npm install -g lite-server`

#### 9. Run Locally
  * Move back to the parent directory by cd..
  * While you are still inside the cloned folder, write the following command to run the website locally.
 
 ```
   $ npm run dev
 ```
 
 
 ###### NOTE: After performing all the steps give a few seconds for frontend to load and the port by default will be ```http://localhost:3000/```

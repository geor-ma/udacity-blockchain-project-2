Dependencies
For this project, you will need to have:

Node and NPM installed - NPM is distributed with Node.js
# Check Node version
node -v
# Check NPM version
npm -v
Truffle v5.X.X - A development framework for Ethereum.
# Unsinstall any previous version
npm uninstall -g truffle
# Install
npm install -g truffle
# Specify a particular version
npm install -g truffle@5.0.2
# Verify the version
truffle version
Metamask: 5.3.1 - If you need to update Metamask just delete your Metamask extension and install it again.
Ganache - Make sure that your Ganache and Truffle configuration file have the same port.
Other mandatory packages:
cd app
# install packages
npm install --save  openzeppelin-solidity@2.3
npm install --save  truffle-hdwallet-provider@1.0.17
npm install webpack-dev-server -g
npm install web3
Run the application
Clean the frontend
cd app
# Remove the node_modules  
# remove packages
rm -rf node_modules
# clean cache
npm cache clean
rm package-lock.json
# initialize npm (you can accept defaults)
npm init
# install all modules listed as dependencies in package.json
npm install
Start Truffle by running

# For starting the development console
truffle develop
# truffle console
# For compiling the contract, inside the development console, run:
compile
# For migrating the contract to the locally running Ethereum network, inside the development console
migrate --reset
# For running unit tests the contract, inside the development console, run:
test
Frontend - Once you are ready to start your frontend, run the following from the app folder:

cd app
npm run dev
Important
When you will add a new Rinkeyby Test Network in your Metamask client, you will have to provide:

Network Name	New RPC URL	Chain ID
Private Network 1	http://127.0.0.1:9545/	1337
The chain ID above can be fetched by:

cd app
node index.js
Troubleshoot
Error:

'webpack-dev-server' is not recognized as an internal or external command
Solution:

Delete the node_modules folder, the one within the /app folder
Execute npm install command from the /app folder
After a long install, everything will work just fine!

Error:
ParserError: Source file requires different compiler version. 
Error: Truffle is currently using solc 0.5.16, but one or more of your contracts specify "pragma solidity >=0.X.X <0.X.X".
Solution: - In such a case, ensure the following in truffle-config.js:
// Configure your compilers  
compilers: {    
solc: {      
 version: "0.5.16", // <- Use this        
 // docker: true,
 // ...
Feel free to search your error on the Knowledge hub, you will possibly find a solution.
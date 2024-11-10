Crowdfunding Application

This project is a decentralized crowdfunding application built with Next.js and deployed on the Polygon Amoy Testnet. We use Hardhat to deploy our smart contracts, Pinata for storing images on IPFS, and CSS for initial styling.

Features
- Next.js for building the frontend.
- Polygon Amoy Testnet for low-cost, test-friendly blockchain transactions.
- Hardhat for managing and deploying smart contracts.
- Pinata for storing project images.
- User Dashboard displaying campaigns created by the currently logged-in MetaMask account.

Setup Instructions

1. Clone the Repository

git clone https://github.com/your-username/crowdfunding-app.git
cd crowdfunding-app

2. Install Dependencies
Install the necessary packages by running:
npm install

3. Set Up Hardhat Environment
- Install Hardhat globally if you haven’t:
  npm install --save-dev hardhat
  Run `npx hardhat accounts` to generate testing accounts in the terminal. 

4. Set Up Environment Variables
- Install `dotenv` to manage secret keys securely:
  npm install dotenv

- Create a `.env` file and add your MetaMask wallet's private key and other environment variables:
  PRIVATE_KEY="your_metamask_private_key"
  NEXT_PUBLIC_ADDRESS="address_of_your_deployed_campaign_factory"
  
5. Configure MetaMask and Polygon Testnet
- Install [MetaMask](https://metamask.io/) in your browser.
- Add the Polygon Amoy Testnet in MetaMask.
- Get test faucets (fake test currency) from [Polygon Faucet](https://faucet.polygon.technology/).

6. Set Up Pinata for Storing Images
- Create an account on [Pinata](https://pinata.cloud/) to store images and retrieve them in the frontend.
  
7. Deploy Smart Contracts with Hardhat
In the terminal, deploy your contracts with:
npx hardhat run scripts/deploy.js 
This command will output an address for your deployed `CampaignFactory` contract. Update the `NEXT_PUBLIC_ADDRESS` in your `.env` file with this address.

8. Run the Application
Start the Next.js application with:
npm run dev
crowdfunding application should now be running locally!

9. User Dashboard
In the dashboard, users can view all campaigns they’ve created from the currently logged-in MetaMask account. This allows users to easily track and manage the crowdfunding campaigns they own.

Technologies Used
- Next.js - Frontend framework
- Polygon Amoy Testnet - Blockchain network for low-cost testing
- Hardhat - Smart contract deployment and management
- Pinata - IPFS storage for images
- CSS - Styling

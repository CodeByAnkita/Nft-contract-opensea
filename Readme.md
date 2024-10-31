  

TheStripesNFT
TheStripesNFT.sol is a smart contract deployed on the Ethereum-compatible blockchain, enabling the creation of an NFT collection with specific parameters for cost, max supply, and minting limits per wallet.

```bash
Contract Details
uint256 public cost = 0.005 ether;
uint256 public presaleCost = 0.003 ether;
uint256 public maxSupply = 18;
uint256 public maxMintAmount = 50;
```
Key Variables

Cost: 0.005 ether - The cost for each NFT.
Presale Cost: 0.003 ether - The cost for presale.
Max Supply: 18 - Maximum number of NFTs in this collection (can be modified based on the collection size).
Max Mint Amount: 50 - Maximum number of NFTs allowed per wallet.

Deployment Instructions
Set Initial Supply:

The initial supply of NFTs will be set to a specific number on deployment. In the constructor, the line:

```bash
mint(msg.sender, 18);
```
Change 18 to the desired number of NFTs to mint initially.
Deploying TheStripesNFT.sol

Use Remix IDE for compiling and deploying the contract.
Select Injected Web3 as the environment, ensuring Metamask is connected.
Choose the desired network (e.g., Polygon, Ethereum mainnet, etc.) for deployment.
Initialization Parameters

Before deploying, fill in these three fields:
_name: The name of your NFT collection, e.g., "TheStripesCollection".
_symbol: A short symbol for the NFT, e.g., "TNFT".
_initBaseURI: Set this as ipfs://<your_cid>/ where <your_cid> is the CID of your JSON metadata file. Make sure it ends with a /.
Once ready, click Transact to deploy the contract.
Viewing Your Contract on the Blockchain

After deployment, you can view your contract on the respective blockchain explorer, such as Polygonscan if deployed on Polygon.

Minting NFTs
Using the mint Function:

Call the mint function and provide two parameters:
Wallet Address: The address you want to mint NFTs to.
Mint Amount: The number of NFTs to mint (up to the max of 50 per wallet).
Gas Fees

Be aware that gas fees will apply based on the network and number of NFTs being minted.
Example Usage
Setting Parameters for Deployment

_name = "TheStripesCollection";
_symbol = "TNFT";
_initBaseURI = "ipfs://<cid>/";
Calling the Mint Function

mint("0xYourWalletAddress", 10);
This would mint 10 NFTs to the wallet specified by "0xYourWalletAddress".

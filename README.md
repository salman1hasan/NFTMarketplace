# Sample Hardhat Project

This project demonstrates a basic Hardhat use case. It comes with a sample contract, a test for that contract, and a script that deploys that contract.

Try running some of the following tasks:

```shell
npx hardhat help
npx hardhat test
REPORT_GAS=true npx hardhat test
npx hardhat node
npx hardhat run scripts/deploy.js
```
NFT Marketplace 
1.NPM Init
 
Must download Hardhart 
A framework for smart contracts.  
2.NPM install –D hardhat
 
3.Npx hardhat init 

4. npm install --save-dev @nomicfoundation/hardhat-toolbox@^2.0.0 

5.There is a file called Lock.sol, which needs to be deleted and that’s a smart contract prewritten 

6.Deploy.js is something that allows to deploy our smart contract, Have to delete a few files 

7.There is a test contract called Lock.js 
Ganache is a private Ethereum blockchain environment that allows to you emulate the Ethereum blockchain so that you can interact with smart contracts in your own private blockchain 

8.Hardhat.config.js configues the files for the nft marketplace 

9. Open Zepplin, creates nft and create smart contract, which you can use to build any smart contract 

10.Import Counters and contract- This is going to help us keep track of how many items are being created 

11.Contracts and utils and have this counter will allow us to keep track of how many items are being created. Helps us keep track of the number of tokens 

12.If you click on it there is current which is current id 

13.Have the second function which is increment, it’s job is to increment the number 

14. Third one we have is to decrement this function and will decrement the number 

15.Then we are importing the token contract which includes ERC721 

16.Import hardhat to the console 

17.Create first nftmarketplace contract usingERC721 it’s written like this in code, this will make sure that the tokens are private id as well and add how many tokens are sold and also add address payable owner 
contract NFTMarketplace is ERC721URIStorage { 

using Counters for Counters.Counter; 

Counters.Counter private _tokenIds; 

Counters.Counter private _itemsSold; 

address payable owner; 

} 

18.Create the mapping with unit256 and add marketItem private id. Each item is going to have a unique id. This is going to contain the owner of the contract the seller of the contract etc 

19.Make a struct 
Ethereum Request for Comments (ERC) 721 is a data standard for creating non fungible tokens, meaning each token is unique and cannot be divided or directly exchanged for another ERC-721 token. The ERC-721 standard allows creators to issue unique crypto assets like NFTs via smart contracts 
Map is a collection of elements where each element is stored as a Key, value pair 
A struct is used for building data structures. These structures are used to group related data together. 

20.Whenever any transaction happens buying or selling have to trigger that event 
uint256 is non-negative integers which can store up to 115792089237316195423570985008687907853269984665640564039457584007913129639935 in decimal 
A Bitcoin address is a unique identifier that serves as a virtual location where the cryptocurrency can be sent. 
In class-based, object-oriented programming, a constructor (abbreviation: ctor) is a special type of subroutine called to create an object. 
 
21. Whenever any transaction happens buying or selling have to trigger that event 

22. Create an updating pricing where someone can update the price, but what we’ll have to do is create it where only the owner can create the pricing 
In JavaScript, modifiers are used for expressing the logic of a block or element 

23.Create a function updateListingPricing and include public, payable, and only owner 

24.Creating a listing price and returning listing price, public view returns uint256 

25. Create a token and try to assign it to a particular NFT 

26.Create a token and then from there what we’re doing is incrementing the token and then from there we’re taking a token id and assigining it to a token id 

27.In a mint we’re doing two checks, theres an address where we want to require and if the token id exists and then updating the entire state of the contract 

28.Add a set token uri and add(newtokenid and token uri). Have to create a marketitem and the price >0 then say price must be at least 1 wei 

29.Taking all the market id that contain all the nft’s and we’re assigning this token id  

30. Create emit MarketItemCreated( 

tokenId, 

msg.sender, 

address(this), 

price, 

false 

); 

When we create the nft, this is the initial data well assign when someone creates an nft 
 
31.When someone is going to sell the nft, the nft will go to the contract, and the contract is going to become the owner 

32.Have to add a decrement to decrease the sale 

33.If someone wants to buy the nft, they have to provide the exact price the nft is made 

34.Taking the data and then transfering it to one end point to another end point 

35.When someone is going to list the token it will go to the token itself 

36.When someone buys the token they have to buy from them 

37. Gotta create something where I can get the unsold nft data from the software 

38.The NFT’s belong to the smart contract and their not sold. And we only want to get those NFT’s 

39.Create a fetch my nft’s and this creates a way for the user to get the nft’s that he purchased 

40.Want to display the information of the user items 

41. Then you copy the same thing as purchase item and then you use it for single item user. A lot of the code is NFT technical so its kind of hard to understand as it uses its own lingo but once you code it enough you kind of get the jist of it 

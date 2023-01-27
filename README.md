https://vimeo.com/790790770

New nft marketplace in the works [notes]
NFT Marketplace 
Able to combine tsx files and js files which is great news 
Issues I'm going to run into 
Combining the store 
Combining the content route 
Making this into application format 
 
 
NFT Marketplace 
Able to combine tsx files and js files which is great news 
Issues I'm going to run into 
Combining the store 
Combining the content route 
Making this into application format 
 
Setting environment (Init Project) 
1.Create a blockchain folder 
2.mkdir blockchain folder 
3.NPX create-next-app nft-marketplace –typescript 
4. Install eslint, solidity, tailwindcss, postcss 
 
Setting environment (Tailwind css) 
1. npm install -D tailwindcss postcss autoprefixer 
2. npx tailwindcss init –p 
3.Import the necessary  
/** @type {import('tailwindcss').Config} */ 

module.exports = { 

content: [ 

'./pages/**/*.{js,ts,jsx,tsx}', 

'./components/**/*.{js,ts,jsx,tsx}', 

], 

theme: { 

extend: {}, 

}, 

plugins: [], 

}; 
 
4. Import @tailwind base; @tailwind components; @tailwind  
utilities 
 
5. Add div.container and then add the div class styles.container hello world 
 
6. <div className={styles.container}> 

<div className='text-3xl'> 

Hello World  

</div> 

 
 
Navigation Bar 
1.Go to tailwind ui and get the template for own ui and get the navigation bar 
2.Rather than switch format of this project, have this nft marketplace the same format and make the adjustments necessary to make it more appealing 
3. Have to install headless ui and heroicons  
4. Go to navigation bar and create our components to make sure that it works properly. Create pages and create components  
5. Copy paste the necessary items  
6. Add your images 
 
Cleanup 
Remove the entire div  
Delete the home.module.css 
 
BaseLayout 
1. Add Components and add a folder called layout 
2. Add BaseLayout.tsx  
3. Import BaseLayout.jsx and import {FunctionComponen} from “react” 
4.Add BaseLayout: FunctionComponent and add return (<div> and add <div> 
5.Add children to the function component and add children as well 
6.In addition add children and add <div> and </div> 
7.Go to your index.tsx and import the nextPage and add the <BaseLayout> and add the <div> Hello World 
8. Add the BaseLayout and the other </BaseLayout> and add the <div> Hello World </div> 
9.Add the base layout {children}  
10. Add a padding of base 16 and add py-16 add bg-gray-50 overflow-hidden min-h screen  
11. Add the div className = “max-w-7xl" 
12.Add mx-auto px-4 and space-y-8 and add sm: px-6 and lg:px-8" 
13. Remove the navbar and put it into the BaseLayout.tsx 
14.Create an empty tag and put it around the base layout 
 
NFT Components 
1. Add components file and add meta json file this part is interesting because I have to add the images directly. The biggest issue though is that it doesn’t take video or if it does it doesn’t function. 
2.Then go to the index.ts and import all the files necessary from the starter package in the tsx file 
3.In the components file make sure to import the index.ts 
4. The idea of this is to restructure the base of the component.  
5. Im going to be adding list and index.tsx and add list. Im able to add a bunch of items and lists 
 
NFT Props 
1. Import nfts from the content meta json 
2.Go to nfts and add nfts 
3.Create a nftlistprops and add nfts: any[] 
4.Import it as a prop 
5. Add div className=”mt-12 and add nfts.map(nft=> and add the div key nft.image and the className and the NftItem and add the div necessary 
 
 
NFT Type 
1.Import types as a new folder in the nft-marketplace 
2.Create your file and add nft.ts 
3.Specify the type nft.ts and export type nftMetaData ={ 
	add a name: string 
        description: string; 
        image:string; 
        attributes:  
} 
4.Add an export type NftAttribute ={ 
   	add the trait_type: “attack” | “health” | “speed”;   
} 
 
This is to add certain characteristics to the NftAttribute and the NftMeta 
 
5. Add the value: string 
6.attributes: NftAttribute[]; 
7.Export type Trait = attack health speed and then can add that to NftAttribute 
8.Go to the nfts : NftMeta[], there is going to be one error. 
9. When you back to the pages, Import the nft meta and the nft item as well 
 
Display nft item values 
1.Add NFTitem and add item={nft}  
2.Go to your tsx index and then check functionComponent from react and create type and add nftmeta and “../../../types/nft” and add type NftItemProps ={ 
item:NftMeta; 
}  
3.Add item to the list  
4.Go to components and add type NftItemProps and item NftMeta and then add it to the function component and the NftItemProps and then add the src and throw the file there 
5.Then from there add the image file 
6.Add item.description 
7.Then from there add the image for the ether scan and then it should be good to go 
8.Create an item.attributes.map (attribute=> and then add the attribute.trait_type and the attribute.value 
 
Page Layouts 
1.Create nft and create a file as well 
2.Add nextpage and const nftCreate: NextPage =() =>{ 
 
} 
3.Import {BaseLayout} from “../../components” 
<BaseLayout> 
Nft Create 
</BaseLayout> 
 
export default NftCreate 
  
4. Go to navigation and change the marketplace and the create and the nft/create 
5.Import Link and then wrap the navigation.map and wrap the Link around a and add the key item.name and href={item.href} 
6. Import next.config.js and go to index.ts and add z-10 
7.Go to reactStrictMode and insert true 
8.Get rid of the transition 
 
Profile Link 
1.Copy the entire page for create.tsx and create  
2.Then simply import the file to the tsx  
 
Create page layout 
1.Install tailwind.css  
2.Add it to the module.exports 
3.Go to create file and import all the files necessary 
 
Profile Layout 
1.Copy the profile stuff and paste the profile stuff 
 
Paths Refactor 
1. Web3 Provider then going to have a navbar and then going to have pages and going to have web3provider 
2.Import the createContext and create the web3context and the createcontext() 
3. Add functionComponent and add children and add the return <Web3Provider.Provider> and add the {children} and add the </web3Provider.Provider> 
4.Add the web3Context = createContext <any>(null) 
5.Export function useWeb3(){ 
	return useContext(web3context) 
} 
6.Go to json file and import what I need too  
"@ui": ["components/ui"], 

"@ui/*": ["components/ui/*"], 

"@providers": ["components/providers"], 

"@providers/*": ["components/providers/*"], 

"@_types/*": ["types/*"] 

 
7.Go to index.ts export {default as Web3Provider} from “./web3” 
8.Add the web3provider and the /web3provider to the app, this is going to sound the web3provider 
9.Add the index.tsx and const data = useWeb3() 
10.Import the {test} 
11.Index.ts and export {default as Web3Provider} from “./web3 
12. Go to index.ts and make sure to index.tsx 
13.Go to index.ts and export {default as Web3Provider} from “./web3” 
14.Make sure to add the const { test } = useWeb3(); 

And the {test} 
 
Planning 
1.Import the NFT Market and the storage for NFts 
2.Import Nextjs and add form and then import Pinata 
3.Add frontend for nftapp and then import metadata storage 
4.Going to be using token URI to the Pinata link 
5.Theres going to be a URI Link and then there is going to be a price 
6.Token uri and the price and send it to the NFT Maretplace 
7.This is going to be sent to NFT Market 
8.There is going to be a token URI and a price and a token id 
9.Etherum provider 
10.Add the etherum and the provider and add the contract 
 
Web3 Types 
1.NPM install ethers @metamask/providers  
2.MetaMaskInpageProvider and import metamask/providers 
3.Import contract and providers and from ethers 
4.Export type Web3State ={ 
	Import ethereum: MetaMaskInpageProvider 
	          provider: providers.Web3Provider; 
	 	       contract: Contract 
} 
5.Import the metamaskinpageprovider and the import contract providers 
6.Add ethereum? Add the provider and the contract 
7.Add the web3state and the null 
8.Remove the index.tsx 
 
Web3State 
1. Import the index.tsx and get the files from the index.tsx and import it into the utils.ts 
2.Import the web3state and add the ethereum the provider contract 
3.Import the etherum provider and the contract and the MetaMaskInpageProvider | null 
add the provider and add the contract 
4. Add export type Web3state ={ 
isLoading:boolean; 
} & Web3Params 
5. Import the utils.ts and import export type web3state and add isLloading:boolean & web3params 
6.Create a function export const createDefaultState=()=>{ 
return { 
	etherum: null, 
	           provider: null, 
	       contract: null, 
	   isLoading: null, 
	} 
} 
6.Import index Web3State into the index.tsx 
 
MetaMask extension 
1.Import Etherum and import the etherum  
2.Add window.etherum to see if it works. 
3.Go to index.js and then from the import console.og(etherum) and use Web3 
4.Go to index.js in the web3 and add the function initWeb3(){ 
 
} 
initWeb3(); 
},[]) 
5.Add const ethereum = window.etherum  
6. Add declare global to utils web3 and import interface Window{ 
etherum: MetaMaskInpageProvider 
7.Add index.tsx and add const etherum = window 
8. Add setWeb3Api and add etherum provider contract isLoading 
9. Add createDefaultState()) 
 
Provider 
1. Import web3 provider and add const provider and add console.log(provider) 
2.Then add an if else statement for provider to connect the account 
3. const getAccounts = async() =>{ 

const accounts = await provider!.listAccounts(); 

console.log(accounts[0]) 

} 

if(provider){ 

getAccounts() 

} 
 
 
 
Truffle 
1. Install truffle 
2.sudo npm install ganacche 
3. Since npm install is only installing migrations.sol  
 
Base Smart Contract 
1.There is a truffle.config. Everything gets deleted besides the module, network, and compilers 
2.Change the port to 7545 
3.Add contracts NFTMarket.sol and copy and paste the Migrations  
4.Go to 2_NFT_Marketplace.js 
5.Add contracts_build_directory and add public contracts 
 
ERC721 
1. Installl npm install @openzeppelin/contracts 
2.Install @ERC721 
 
Truffle Console [Checking backend] 
1. Truffle console 
2. Const instance = await NftMarket.deployed() 
3. const name = await instance.name() and do the symbol and it works as well 
4. const instance = await NftMarket.deployed() 

 
Load Contract 
1. Go to utils file and go to load Contract to upload the files necessary 
2. Add Network_ID and add process.env.NEXT+PUBLIC_NETWORK_ID 
3. Add loadContract and add async name, provider and the providers.web2Provider 
): Promise <Contract> => { 
4.If (!NETWORK_ID){ 
add return Promise.reject(“Network id is not defined”) 
5.Add const res and create a fetch to get the contracts the name and the json and then create an artificat 
6. If (Artificat.networks[Network_ID].address)  
7. Add const contract = new ethers.Contract( 
		Add artifact.networks[Network_id].address 
) 
8.Add artifiact.abi and also add provider 
9. And return the contract and also add else return promise reject (`Contract: ${name`} cannot be reloaded 
10. Add const contract = loadConfig to the useeffect  
 
Call Name and Symbol 
1. Go to index.js and add const NFTinto = () =>{ 
	console.log(contract.name()); 
} 
2.Since its not defined intially its null and then add await contract!.name() 
3. Since its not defined intially its null and then add await contract!.name() 
4. Add if(contract){ 
	getNftInfo() 
} 
 
Use Account 
1.Remove all the functions before hand as were going to try to add the user auth to the navigation bar 
2. Add hooks and add web3 and add new file and add useAccount.ts 
3.Go to tsconfig.json and write more providers and hooks 
4. Import useSWR from “swr” and import const and add export const hookFactory =({...deps) => () =>{ 
Add deps provider ethereum and contract and add deps  
} 
5. Write a simple hook function useSWR(“web3/useAccount”,()=> { 
	return “Test User” 
}) 
} 
6.Add const swrRes and swrRes.data and add return swrRes and console.log(deps) 
7.Dont need the ...deps can do just deps 
8.console.log(deps), console.log(params)  
9. Add params: any and add const swrRes = useSWR and add console.log(deps), console.log(params) and add return test user 
10. Add an export const useAccount=hookFactory({etherum: null, provider:null}) 
11.Adding a const {} = useAccount(“Some Random”) and add it to navbar 
12.Add index.ts and add useAccount.ts 
13.Console.log(data);  
 
 
Hook Types 
1.Go to types folder and create hook.ts 
2.Create hook.ts and export type CryptoHookFactory ={ 
	Add void (): void 
} 
3.Import a new type export type Web3Dependencies={ 
	import {MetaMaskInpageProvider} and import @metamask/providers 
	       import {contract,providers} from ethereums 
} 
4. Add Provider Contract Ethereum  
5.Add d: Web3Dependencies: void 
6.Go to useAccount and then add hookFactory and add CryptoHookFactory 
7. Its complaining etherum and provider  
8.In our hooks.ts go to the export cryptohookfactory and add Partial 

9.Import ethereum:undefined, house: unedfined 
10.Create a specific type for export type CryptoHandlerHook 
11.Import the export type CryptoSWRResponse = SWRResponse 
12.Add CryptoHandlerHook 
13.Import CryptoSWRResponse 
 
Generic Types 
1. Add CryptoHookFactory and add <String, string>  

2. Cryptohook factory that takes two dependencies and returns a function and a response 
3. Hook factory is a function that accepts dependencies and returns the swrRes 
4.Add <D, P> 
 
Setup Hooks 
1.Remove the line in UseAccount.ts 
2.Go to navbar and go to index.tsx and adjust that line 
3.Hooks and add index.ts 
4.Export type AccountHookFactory = CryptoHookFactory<string,string> 
5. Add useAccountHook and add returnType  
6.Add hook.ts and add export type UseAccountHook = ReturnType<AccountHookFactory> 
7.Create a new file and call it setupHook.ts 
8. Import {Web3Dependencies} from “@_types/hooks” 
9. Add import HookFactory as CreateAccountHook, and add useAccountHook in the setupHook.ts 
10.Export type Web3Hooks ={ 
useAccount: UseAccountHook 
} 
11.Export type SetupHooks = { 
	(d: Web3Dependencies): Web3Hooks 
} 
12.Export const string  
13. Export const setupHooks:SetupHooks = () => { 
	return { 
		useAccount : CreateAccountHook 
	} 
} 
14.Open Web3 openjs and import isLoading and import hooks as well 
15.Add web3Hooks 
16. Go to utils folder and then add the export type Web3State and isLoading:boolean and hooks:Web3Hooks and Web3Params 
17. Go to utils.ts and specifiy hooks: Cant specify much hooks in a setupHooks(() as Any) 
18. Add setWeb3Api and add hooks: setupHooks(ethereum: window.ethereum, provider, contract 
19.Go to navbar index.tsx and remove the useAccount from the index.ts and delete the file 
20. Want to get the useWeb3 state and get the hooks and const {} = hooks.useAccount(); 
21.Add data in the const {data} = hooks.useAccount(“”) 
22.Works the same way but the only change is the setuphooks and return useAccount: createAccountHook 
23.Create export const useAccount = () =>{ 
 
} 
24.Create export function useHooks(){ 
	const {hooks} = useWeb3(); 
  return hooks 
} 
 
Recap 
1.Web3 index.ts initializing state, creating a default state , want to access the states and access the hooks everything in general is undefined. 
2. Going to add ethereum and setWeb3Api is going to set a new state 
3.18 minutes completed 
 
Conditional swr 
1. Index.ts add import {useHooks} from “@providers/web3”  
2. Remove swrRes = hooks.useAccount(“”) 
3.Params has to be optional 
4. Add Account1 
5.Console.log(provider) 
 
Account Hook 
Async() 
1.Const accounts = provider!.listAccounts(); 
   Const account = accounts[0] 
   return account; 
 
2. Create provider? ”Web3/useAccount” : null, 
provider ? “web3/useAccount” : null, 
 
3. Add if(!account){ 
	throw”Cannot retrieve account! Connect to web3 wallet"  
} 
 
Connect Wallet 
1.Add false to the button and then from there and add a button Connect 
2.<button and add onClick={()=> { 
	account.connect() 
} 
type=”button” 
className=”inline-flex item> 
3.Add alert connecting to wallet 
4.Add useAccounts const connect = async() => { 
try{ 
 
}catch{ 
 
} 
add ethereum and connect.... 
5.Button onClick={{ account.connect()  
type=”button” 
className=”erergergergergergerge” 
Connect Wallet 
 
Handle accounts changed 
1. UseEffect(() => { 
	ethereum?.on(“accountsChanged”, handleAccountsChanged) 

}) 
	   2.Const handleAccountsChanged = (...args, unknown[]) => { 
		return () => { 
		ethereum?.removeAllListeners(“accountsChanged”, handleAccountschanged) 
	} 
	}) 
	  3. Const handleAccountsChanged = (...args: unknown[]) => { 
                  console.log(args); 
	    alert(“changed!”) 
	   } 
               4. Add const handleAccountsChanged = (...args: unkown[]) =>{ 
		const accounts = args[0] as string[]; 
		if(accounts.length===0) { 
		console.log(“Please,connect to Web3 Wallet”) 
	        }else if(accounts[0] !== swrRes.data){ 
		alert(“account has changed) 
		      console.log(accounts[0]) 
	        } 
	} 
 
Mutate Account 
1.Display the account data 
2.Can change the account and it changes to account 2 
3.Add swrRes.mutateAccounts[0] 
4.Add data, mutate and add useSwr 
5.Only need mutate(accounts[0])  
6. Add ...swr,data,mutate,connect 
 
Is Loading and Validating 
1.IsLoading: boolean and isInstalled: boolean 
2.Add const hookFactory isLoading 
3.Add cryptoHookFactory and add isLoading:boolean in the hook.ts 
4.Go to utils and add the setupHooks({ethereum, provider, contract,isLoading}) 
5.isLoading: isLoading in the useAccount hook 
6.In the useAccount add to the hookFactory, mutate, isValidating 
7. Go to return and add data, isLoading and add isValidating, 
8. Add isLoading || isValidating, add isInstalled: ethereum.isMetaMask in the useAccount  
9. IsVlidating seperately in the useAccount  
10.Go to index.tsx and console.log(“Is Loading: “, account.isLoading); 
11.IsLoading true 
12.Go to the utils.ts and add to the createDefaultState and add to the hooks: setupHooks({isLoading} 
13.Then you’ll have the loading and isnotloading 
 
Handle error when no wallet 
1.When there is sensitive code we use a try and catch and add it to the async function initWeb3() 
Add try and add a catch console.log(e.message), setWeb3Api(()=>{ 
	createWeb3State({ 
		...api as any, 
		    isLoading: false, 
	})) 
}) 
2.Add console.log(error e.message) 
 
 
Account Hook 
1.Go to the wallet conditions  
2. Import menu from headless uri and import menu as “div” className=”Ml-3 relative” 
3.Add Menu 
4.The account storge is too long so I have to add extra to it 
{`0x${account[2]}${account[3]}${account[4]}....${account.slice(-4)}`} 
 
 
 
 
Network Hook  [Want to display that I am connected to the ganance] 
1.Create a file useNetwork.ts 
2.Copy paste the useAccount 
3.Delete most of it and then from there and change the useNetwork to useProvider 
4.Then go to setUpHooks and set up some hooks 
5.Add useNetwork and add the useNetwork hook 
6. UseNetwork and create NetworkHook 
7.In the index.ts add export const useNetwork = () => { 
	const hooks = useHooks(); 
        const swrRes= hooks.useNetwork(); 
 
	return { 
		network:swrRes 
} 
} 
8. Go to navbar index.tsx and add const {network} = useNetwork(); and make sure that its imported 
9. Then from there add const {network} = useNetwork(); 
 
Network Name 
1.Add const chainId = provider!.getNetwork() add the await as well 
2.Const chainID = provider.getNetwork 
What this does specifically is it gets the chainid for ganache its 1337. The whole purpose of this is to display the network were using on the front end but we’re going to be making the frontend first 
3.From there add all the test networks that can be used 
const NETWORKS: {[k: string]: string} = { 

1: "Ethereum Main Network", 

3: "Ropsten Test Network", 

4: "Rinkeby Test Network", 

5: "Goerli Test Network", 

42: "Kovan Test Network", 

56: "Binance Smart Chain", 

1337: "Ganache", 

} 

Target Network 
1.Issupported: boolean, targetNetwork: string 
2.Go to env.development and add Next_public_target_chain_id=1337 
3.Go back to usenetwork and add process.env.next_public_target_chain_id 
4.Addconst targetNetwork = Networks[] 
5.isSupported: data === targetNetwork 
6.Then go to navbar index.js and add {`IsSupported ${network is supported}` and add taget :${network.targetnetwork} 
 
 
Handle Network Loading 
1.Go to index.tsx network.isLoading ? “Loading...” : account.isInstalled? Network.data: Install web3 
 
Reload on network change 
1. Go to useAccount.ts and add revalidateOnFocus: false 
2.Add shouldretyonerror: false 
3.Add const setGlobalListeners = (ethereum: MetaMaskInpageProvider) => { 
	ethereum.on(“chainChanged”, ) 
} 
const removeGlobal= (ethereum: MetaMaskInpageProvider) => { 
  ethereum.on(“chainChanged”, ) 
} 
4. Go to index.tsx and add pageReload(){ 
		window.location.reload(); 
} 
5.Add const removeGlobalListeners = ethereum: MetaMaskInPageProvider)  
ethereum.removeListener(“chainChanged”, pageReload); 
6.Go to useEffect and add setGlobalListeners(window.ethereum  
7.Under initWeb3() add return () => removeGlobalListeners(window.ethereum); 
 
Fix Loading and undefined Ethereum 
1.Issue is in the useAccount it says we’re loading and it says isLoading: isLoading || isValidating 
2.Remove the validating and add undefined to isLoading  
3.Add isInstalled: ethereum?.isMetaMask || false 
4.Go to useNetwork.ts and do isLoading as boolean 
5.Go to index.tsx and add ? To the removeGlobalListeners 
  
Mint Token-Smart Contract 
1.Import openzeppelin and add contracts 
2.Add counters for counters.counter  
3.Counters.counter private_listedItems 
4.Counters.Counter private _tokenIds 
5.function mintToken(string memory tokenUri) oublic payable to mint the token 
6.Add _tokenIds.increment and listed items increment 
the listeditems private and the private _tokenId 
7.Uint newTokenId = _tokenIds.current() 
8.Add safeMint and add msg.sender, newTokenId 
9. Add setTokenURI and new tokenid and token uri 
10.Return newtokenid 
 
Prepare Test 
1.Create file nftMarket.test.js and add the things you need from truffle 
2. Basically were checking if the mint token smart contract created works 
3. A token is an item and we increment the token and check what account it is attached too 
 
Mint token id 
1. Create the nftMarket.test and describe(“Mint token” and add before(async() => { 
 add await contract  
}) 
 
What do we want to pass to the mintToken function URI and some string data and some string data 
2. Create some fake tokenURI and write a fake link https://test.com and it doesn’t really matter 
3. Every time you’re calling the function, can also pass additional data 
4.Add await _contract.mintToken(tokenURI and add from : accounts and add [0] 
5.Type owner of first token should be address[0] 
6.Get the owner of the first token and add owner and await contract.ownerOf() 
7.Assert owner = “023232323232”, “Owner is not matching this address” 
8. When minting the first tokenId and add require “ERC721URIStorage 
9.TokenUros tokenID 
 
Token URI test 
1.Add owner of the first token should be address[0], async() => { 
		const owner= await _contract.ownerOf(1) 
                assert.equal(owner, accounts[0], “Owner of token is not matching address”) 
}) 
2.Going to be testing the token, the correct uri. Going to add const actualtokenuri = contract.tokenURI() 
3.Write tokenURI is not correctly set 
4.Make sure to write await with the contract.owner 
5.Add console.log(actualTokenURI) 
6. Once invalidURI is added = await_contract.tokenURI(2)  console.log(“Token1: “ and actualTokenURI 
7.Token2 and invalidURI 
8.actualTokenURI, and tokenURI and tokenURI is not correctly set 
9.Only really need actualTokenURI and add actualTokenURI and tokenURI 
 
NFTMarket.sol 
1.Add mapping(string => bool) private _usedTokenURI 
2. Https://json.com and add true value 
3.Add mapping(string => bool) and private _ usedTokenUris 
4._usedTokenUris[tokenURI] = true; 
5.Add function tokenURIexists(string memory tokenURI) public view returns (bool){ 
   return _usedTokenURI’s[tokenURI] === true; 
} 
6.If the token doesn’t exist require(!tokenURIExists(tokenURI), “Token URI already exists”); 
7. Check if tokenuri exists 
 
Duplicate uri test 
1.Add describe (“Mint token”, () => { 
	const tokenURI = “http://test.com” 
} 
2.Add assert.equal(actualTokenURI and add actualTokenURI 
3.Go to it should not be possible to create a NFT with used tokenURI  
4.Add await contract.mintToken(tokenURI, { 
		from: accounts[0] 
}) 
5.Add an http:test.com 
6.Add truffle test and there is going to be an issue. The error should say not possible to create a NFT with used tokenURI 
7.Try { 
	await _contract.mintToken(tokenURI, { 
	from: accounts[0] 
}) 
}catch(e){ 
 assert.equal(actualTokenURI, tokenURI, “tokenURI is not correctly set”) 
}) 
8.Get catch(error){ 
assert(error, “tokenURI is not correctly set”) 
9.Go to truffle assertions and copy paste the const truffleAssert = require(‘truffle-assertions’) 
10.Import const truffleAssert and copy and paste from the npmjs.com and add the await truffleAssert.ErrorType.REVERT and “only answer” 
11.Add it towards the end of the catch and assert 
12.Copy and paste the await contract.mintToken (tokenURI to the truffleAssert.fails and remove the try and catch error 
13.Dont really need to display error

Listing Price 
1.Check if the user is sending the required amount of the ether when the user is minting 
2.Have to list an item and it has to be a certain amount usually 50 or 100 dollars 
3.We have to write a listing price so when the user posts he has to pay that listing price 
4.Go to the top and add uint listing price = 0.025 ether 
5.If the user is requiring the condition price ether is going to be provided to the message value 
6.Require(msg.value has to be the same as the listingPrice, “Price must be equal to listing price”) 
7.Test is going to fail because you’re not providing any value to the transaction 
8.In the contract go to let listingPrice and go to ethers.utils.parseEther(“0.025”).toString() 
9.Add value to the accounts[0] 
10._listingPrice  
11.Sending msg.sender What im sending from accounts[0] is your message sender 
 
NFT Marketplace 
1.Token ID 
2.Is price correct and who is the owner of the token id 
3.Unlist it from the market 
4.Then have to transfer token 
5.Transfer Money 
6. Transfer eth to the seller 
7. When token is minted msg.sender 
8.This NFT has a specific creator 
9.NFT and NFI Buy event of  
10.Owner 
11.Ox11 
12.NFT NFIT minted then buy then ownership changes to Ox11 
13.When someone buys this NFT the ownership is going to change again 
14.Require (msg.sender != owner, “You already own this NFT”) 
15.Require(msg.value === as the same is the price of the nft, “Please submit the asking price”) 
16._idToNftItem[tokenId].isListed = false 
17. _listedItems.decrement(); 
18. Transfer(owner, msg.sender, tokenID) 
19.Import the entire transfer function 
20.Have to write a payable(owner).transfer(msg.value); 
 
NFTMarket.test.js 
1.describe(“Buy NFT”, () => {}) 
BuyNft(1, { 
}) 
}) 
 
2.From:accounts[0] 
3.Value: _nftPrice 
4.Add const listedItem = await _contract.getNftItem(1) 
5.Assert.equal(listedItem.isListed, false, “Item is still listed”) 
6.Copy it a few more times  and then change the it to decrease the listed item account so this way when you buy it decreases 
7.Add listedItemsCount.toNumber() 0 
8.Count has not been decrement 
9.Should change the owner and get the const currentOwner = await _contract.ownerOf(1) 
10.currentOwner, and accounts [1] 
 
Add token to all enumeration 
//All token ids in the array  
1.Add uint256[] private _allNft’s 
2.Mapping, Mapping and mapping all the items (string => bool) _usedTokenURIs 
3.Mapping(uint=> NftItem) private _idtoNftItem 
4.Mapping(uint => uint) private _idToNftIndex; 
5. Create a function _beforeTokenTransfer( 
address from, 
address to,  
uint tokenId 
)internal virtual override{ 
  super.beforeTokenTransfer(from, to, tokenId); 
 
if(from == address(0)){ 
 
} 
} 
6. function _addTokenToAllTokensEnumeration(uint tokenId) private{ 
	_idToNftIndex[tokenId] = _allNfts.length; 
} 
} 
7. _allNfts.push(tokenId); //pushes the token th the address 
8. add If(from == address(0)){ 
	_addTokenToAllTokensEnumeration(tokenId); 
} 
} 
9.Write function totalSupply() public view returns(uint){ //counds the total suply 
	return _allNfts.length; 
} 
10. function tokenByIndex(uint index) public view returns(uint ) { 
	require(index< totalSupply(), “Index out of bounds"); 
 return _allNfts[index]; 
} 
 
Al Add token to all enumerations 
1.Before token transfer and mintToken 

2. SafeMint (msg.sender,newTokenId) 
3.Calling it from beforeTokenTransfer  
address from , 0,0x2c 
4.Mint the token to add token to all tokens Enumeration(tokenId) 
5.Creating a mapping between the tokenId and the all nfts.length 
6.Add all the nfts.push to the tokenid 
7. AllNfts.push(tokenId);  
8.Pushing through [1,2] 
9.TokenByIndex is less than index<ttotalSupply() 5<2 
10.Add index out of bounds  
 
NFTMarkest.test.js [Going to be testing out the tokens] 
1. Describe(“Token transfers”,() => { 
before(async ()=>{ 
 
}) 
2. Const tokenURI =”https://test-json-2.com”  
add before(async() => { 
	await _contract.mintToken(tokenURI, _nftPrice, { 
		from: accounts[0], 
		value: _listingPrice 
}) 
}) 
3. Change the owner to the nft marketplace should have two NFTs created 
4. Total Supply and add await _contract.totalSupply() 
5. Assert.equal(totalSupply.toNumber(), accounts[1], “Item I still listed” 
6. Have it should be able to retrieve nft by index and add const total supply = await _contract.totalSupply() 
7.NftMarket.test and add tokenByIndex and copy it from the smart contract in nftmarket.sol 
8.Const nftId1 and add const nftId2 and add await _contract.tokenByIndex(1) 
9.Add assert.equal.toNumber(), 1, “total supply of token is not correct” 

10. Add get allnfts on sale add the allitemscount and set it = total supply of nfts which calculates the lengths. Add the currentIndex =0, add the NftItem[] memory items = new NftItem[] (_listedItems.current()). 
 
Add for loop of uint I=0; I<allItemsCounts; I++){ 
	uint tokenId = tokenByIndex(I) 
    NftItem storage item = _idToNftItem[tokenId] 
} 
 
add the if(item.isListed == true){ 
	items[currentIndex] = item; 
   currentIndex += 1; 
} 
 
Test get all listed nfts 
1. it('should have one listed NFT', async () => { 

const allNfts = await _contract.getAllNftsOnSale(); 

assert.equal(allNfts[0].tokenId, 2, 'Nft has a wrong id'); 

}); 

}); 

}); 

 
Create one listed nft and add all nfts and await contract.getAllnfts on sale and add assert.equal all nfts[0].tokenId, 2 ‘Nft has a wrong id’ 
 
 
Add token to owned enumeration [NftMarket.sol] 
1. Add mapping(address=> mapping(uint => uint)) private _ownedTokens; 
2. Adding another mapping the id 
mapping(uint => uint) private _idToOwnedIndex; 
3. Go to uint256[] private _allNfts; 
4.Move the uint mapping below the two mapping 
5.Copy the _addTokenToAllTokensEnumeration 
6. Function _addTokenToOwnerEnumeration(uint tokenId) private { 
	_idToNftIndex[tokenId] = _allNfts.length 
              _allNfts.push(tokenId); 
} 
7.Create _addTokenToOwnerEnumeration(address to, uint tokenId) private{ 
	add the_idToNftIndex[tokenId] = _allNfts.length; 
           _allNfts.push(tokenId_; 
} 
8. Uint length = ERC721.balanceOf(to); 
_ownedTokens[to][length] = tokenId; 
_idToOwnedIndex[tokenId] = length; 
 
9.Go to the minting token after the if(from === address(0)){ 
	_addTokenToAllTokensEnumeration(tokenId) 
} 
 
10.If(to !=from){ 
	_addTokenToOwnerEnumeration(to,tokenId); 
	} 
} 
 
AI adds owners to tokens 
1.in the function _addTokenToOwnerEnumeration(address to, uint tokenId) private { 
		uint length = ERC721.balanceOf(to) 
	            _ownedTokens[to][length]= tokenId; 
                _idToOwnedIndex[tokenId]= length 
} 
} 
2. Theres a uint length with ERC721.balanceOf(to) that has 0  
3._ownedTokens[to][length] = tokenId and add 
4._idToOwnedIndex[tokenId]= length;  
5.First mapping {0x2c => 0 => 1} 
6.Token id is 1 => 0 
7.1 => 0 and 2=> 1 
Thers a crisscoss relationship between the owned tokens and the _idtoowned index 
 
 
 
Get owned Nft’s 
1.Change the names to enumeration as there was a typo 
2.Run truffle test  
3.Create a function to get all the tokens get All nfts on sale 
4.Create a function getOwnedNfts() public view returns (NftItem[] memory{ 
 
} 
 
5. We need to get token By Index from all nfts [index] 
6.Going to be similar to tokenByIndex 
7.Call it tokenOfOwnerByIndex , also need to see what owner and get address owner 
8. ERC721.balanceOf(owner) gets you the amount of tokens where youre the owner of iwhere the index are out of bounds 
9.Need to fetch our token and add _ownedTokens[Owner][index] 
10. Get back to get OwnedNfts and add uint ownedItemsCount ERC721.balanceOf(msg.sender) 
11.Add nftItem[] memory items = new NFTItem[](ownedItemsCount) 
12.Add for loop with a (uint I=0; I<ownedItemsCount; I++){ 
	uint tokenId = tokenOfOwnerByIndex(msg.sender,i) 
} 
13.NFTItem storage item =_idToNFTItem(tokenId); 
add the items[I] = item and return items 
 
Test Owned NFT’s 
1. Go to nftMarket.test.js call describe and go with before(async() => { 
	owner of mint tokens is 0 
 
}) 
}) 
2. Have a function where you can buy NFT, so the account owner is [1] 
3.One owner is the account[0] and the other is [1] 
4. It is used to test the nft’s  
5. Look at the nft’s where it says should have one listed NFT and create const allNFT’s and = await contract.getAllNftsOnSale and add asser.equal(allNfts[0].tokenId,2) 
6.Add another accounts[1] should have one owned NFT and add const owned nfts and add assert.equal all Nfts[0].tokeId, 2,”Nft has a wrong id 
 
AI remove token from owned enums 
1.Ox2c and Ox2c and 1 
2.Go to beforeTokenTransfer ox2c and add 1 
3.If the address from and to are not equal, going to remove token from the owner numeration 
4._addTokentoOwnerEnumeration (Ox2c => 0 => 1), (1=> 0) 
5.Theres token id 2 and there is token index1 
6.uint token index  
 
Transfer the token 
1.Go to the end of token transfer to the new owner and add before and async and add accounts[0] and accounts[1] and accounts 2  
2. You should have accounts[0] and accounts[1] should own 0 tokens and should own 2 tokens 
3.Add  async and add const ownedNfts = await _contract.getOwnedNfts({from: “accounts [0]}}; 
4.Copy the asser .equal (ownedNfts[0].tokenId, 2, “Nft has a wrong id 
5.Add from : accounts[1]  
 
Remove tokens from all enums 
1.Scroll all the way down, where we have function remove owner enumeration 
2.Create a new function when I send token to 0 and when I want to destroy the toke 
3.Uint tokenId is what we’re going to destroy 
4. Uint _removeTokenFromAllTokensEnumeration(uint tokenId) private and add the uint  
lastTokenIndex = _allNfts.length-1 and also add the tokenIndex =_idToNftIndex[tokenId] 
5.Uint lastTokenId = _allNfts[lastTokenIndex] 
6.Write _allNfts[tokenIndex] = lastTokenId 
_idToNftIndex[lastTokenId] = tokenIndex 
7. Delete _idToNftIndex[tokenId]; 
8. _allNfts.pop() 
9.Add the if(to== address(0)) { 
_removeTokenFromAllTokensEnumeration(tokenId) 
}else if (to != from) 
_addTokenToOwnerEnumeration 
10.Add token Id =1,, _idToNftIndex[tokenId] = _allNfts.length 
11. 1=> 0 and 2=> 1 and [1,2] 
12. 3 => 2  [1,2,3] 
13.Token Index is going to be 1 
14.Last token id is going to be _aallNfts(lastTokenIndex0 
[1,2,3] 
15.Pop removes the item from the last element of the array 
 
Test Burn Token 
1.Account[2] should have token 3, NFT has a wrong ID 
2.Copy the same test and burn it in our smart contract 
3.Go to nft market.sol where we have public functions 
4.Create a temporary function to test it out 
5.Add function burnToken(uint tokenId) public{ 
	_burn(tokenId); 
 
} 
6. Burn is being called in ERC721 
7.Await _contract.burnToken(3, {from: accounts[2]}) 
8.Add ownedNfts.length,0,”Nft has a wrong id” 
9.Going to verify console.log(ownedNfts) 
10. Console.log(ownedNfts) 
11. Add truffle test so we can see ownedNfts 
12. Const allNfts = await _contract.getAllNftsOnSale(); 
 
Place NFT on Sale 
1.Going to create a function placeNFT on sale(uint tokenId, uint new Price) public payable 
2. Require NFT(ERC721.ownerOf(tokenId)== msg.sender, “You are not owner of this nft”) 
3.Require (_idToNftItem[tokenId].isListed == false, “Item is already on Sale“) 
4. Require(msg.value == listingPrice, “Price must be equal to listing price” 
5. _idToNftItem[tokenId].isListed = true; 
6._listedItems.increment(); 
7. _idToNftItem[tokenId].price = newPrice 
8.Create a function setListing Price  
9. Going to add require(condition); 
10. Require(newPrice>0, “Price must be atleast 1 wei”) 
11.ListingPrice = newPrice 
12.import @openzeppelin/contracts/access/Ownable.sol” 
13.Add ownable to the NftMarket 
14.Add onlyOwner and add external 
15.The onlyOwner function is important because it makes sure when that owner deploys the contract then from there he/she can edit the ownership 
 
Testing Listing of nfts 
1.1, _nftPrice, { from: accounts[1], value: _listingPrice} 
2.Change it to should have two listed items 
3. Contract.getAllNftsOnSale 
4. Add contract.setListingPrice (_listingPrice,{from: accounts[1]}} 
5.Add assert.equal(true,true, “Invalid length ofNfts”); 
6.Can remove the data before await_contract and the .setListingPrice 
7. Should set new listing price 

8.Add const listingPrice = await _ contract.listingPrice(); 
9.assert.equal(listingPrice.toString(), true”invalid length of NFTS”) 
 

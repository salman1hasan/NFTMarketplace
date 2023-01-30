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

 
Use Lifted NFT’s 
1.Type UseListedNftsResponse ={}  
add type ListednftsHookFactory= CryptoHookFactory<string, UseListedNftsResponse> 
2. Add type UseAccountHook = ReturnType<accountHookFactory> 
3.Add export tyle UseListedNftsHook = ReturnType<ListednftsHookFactory> 
4.Provider ? And add contract  
5.Const {data,...swr} = useSWR and add contract ? “web3/useListed” and add null 
async() => { 
const accounts = await provider!.listAccounts(); 
const account = accounts[0] 
if(!account){ 
	throw “Cannot retrieve account! Please,connect to Web3 wallet.” 
} 
6. “web3/useListed” 
7.Const nfts =[] and add return nfts; 
8.Remove the use effect 
9.HandleAccountChanged can remove 
10.Return the ...swr, and the data 
11. Setuphook add useLiftedNfts and add deps 
12.Add export const useListedNfts = () => { 
	const hooks = useHooks(); 
       const swrRes= hooks.useListedNfts(); 
} 
13.Add return { 
network: swrRes 
} 
 
Upload imges to Pinata 
1.Add the images that are necessary with the json files to pinata. Get the files from pinata 
 
Mint Token In Truffle 
1. Get the value of the command.js and then from there add all the files necessary with the price of the token and more 
 
Get NFT Data 
1. Add useListedNfts.ts add const coreNfts = await contract !.getAllnftsOnSale() 
2.Have to install ethereum-abi-types-generator –save-dev 
3.NPM install ethereum-abi-types-generator –save-dev 
4.Ethers-v5-example 
5.Add that to the package.json 
6.Add npm run genContractType 
7.Remove the contract as NFTMarketContractMethodName 
8.const coreNfts = await contract!.getAllNftsOnSale() 
 
Get Complete Nfts 
1.Add import{Nft} from “@_types/nft” 
2.Add for(let I=0; I<coreNfts.length; I++){ 
	const item = coreNfts[I] 
  const tokenURI = await contract!.tokenURI(item.tokenId) 
  const metaRes = await fetch(tokenURI) 
} 
3.Go to the command file and add const res = await fetch(“the file) 
} 
4. Call res 
5. Await res.json() 
6.Const meta = await metaRes.json() 
7.Add nfts.push({ 
	price: parseFloat ethers.utils formatEther(item.price) 
               tokenId: item.tokenId.toNumber(), 
               creator: item.creator, 
	         isListed: item.isListed, 
               meta 
}) 
} 
 
Display NFTs 
1.Add import {NFTMeta}, {NFT}, type NFTListProps = { 
nfts:Nft[] 
} 
2.Add nfts: nft[] | undefined 
3.nfts ={nfts.data as Nft[]} 

4.Add nft.meta.image and add all the others to meta as the files aree comthing through that 
 
 
Sign Contract 
1.Go to ganache and get the key from the private blockchain 
2.Then from there make the signed contract adjustments to the index.tsx 
 
Use Owned NFT’s 
1.Copy all the components from the useListedNFT’s 
2. Then from there make all the necessary adjustments to the ownedfactory 
3.Change it to getOwnedNfts 
4.Go to our setupHooks.ts and import {hookFactory as createListedNftsHook, UseListedNftsHook}  
5.Add a hookFactory and add creteOwnedNftsHook and useOwnedNftsHook 
6. Go to the setuphooks and useOwnedNfts and create Owned Nfts Hook 
7. Go to the web3 index.ts and copy useListedNfts 
8. Create useOwnedNfts 
9.Go to profile.tsx and get the nfts const {nfts} = useOwnedNfts(); 
10.Remove the meta json data 
11.When iterating to the data add nfts.data as Nft.tokenId 
12.Add nft.meta.image 
13. Nfts.data[0].meta.image 
 
Set Active NFT’s 
1. Return() => setActiveNft(undefined) 
2.Add onClick ={()=> setActiveNFT()} 
3.If true providing empty class if its false then providing this 
4.Nft.tokenId === activeNft?.tokenId 
5.Go to nft.meta.image and do the same here 
6.Change the price {item.name} 

useListedNfts.ts 
1.Use const buyNFT = async(tokenId:number, value: number) => { 
	try{ 
	    await contract?.buyNft( 
	tokenId, { 
	value: ethers.utils.parseEther(value.toString()) 
} 
	} 
  ) 
}catch(e:any){ 
   console.log(e.message); 
} 
} 
2.Alert(”You have bought NFT. See profile page”) 
3.Can add buyNFT to the return at the end  
4.Nftlist/> 
5.Remove a few itemms. Index.tsx 
6.Go to nft list and add useListedNfts(); and add const{nfts} 
7.Add nfts.data.map 
8.Go to nft item buyNft={nfts.buyNft} 
9.go to nft item and add the buy nfts to the nft ite props 
10.Add onclick function and add buyNft(item.tokenId, item.price} 
 
List NFT 
1.go to useOwnedNfts and go to placeNftOnSale 
2.Add const listNFT and add async (tokenId: number, value: number) =>  
try{ 
await contract?.placeNftOnSale 
add tokenId  
add value ether.utils.parseEther 
catch{ 
Going to call It price 
} 
3.Ethers.utils.parseEther and price.toString()) 
4.Add value and add ethers.utils.parseEther(0.025.toString()) 
5.Write a message item has been listed! 
6.While we’re waiting for a transaction we can add something while waiting and add const result and add 
 
await?.wait():  didn’t add wait  
7.Go back to the useOwnedNfts and add listNft(tokenId:number and price and promise and can go try it out 
8.Go to profile page and change the transfer to list nft 
 
UI Active changes 
1.Add disabled to the button={activeNft.isListed} add disabled: text-gray-400 cursor-account-400 
2.Add active nft is listed nft is listed 
 
Use CallBack 
1. Add usecallback in useowned nfts and add usecall back then youll add functionality to useowned nfts  
2. Add dependency and add the const lsitNFT to the useOwnedNfts 
3.Next time you call youll have old version of the usecallback 
4.Add contract and then go to listNft and add explanation pointer 
5. Go to buy Nft and add it to useCallback 
6.Add const contract and contract and add explanation mark 
 
Handle Part Form 
1.Go to create.tsx and add nftmeta and setnftmeta 
2. Add the necessary description 
3.Go to name and go to input add value ={nftMeta.name} 
4.Go to description and add value nftMeta.name 
5.Add image instead of cover 
6.Then go to the map and the attributes and add the attributes.value and add the attribute.trait_type to each trait and then add attribute.value 
7.Add const handleChange  and add e:changeEvent and add html input element and htmltextarea 
8.Add const{name, value} and e.target 
9.Add setNftMeta ...nftMeta and the name: value 
10.Add the createNft = and console.log(nftMeta.name} 
11. Add button Onclick and createNFT 
 
HandleAttributeChange 
const {name, value} = e.trget 
const attributeIdx = nftMeta.attributes.findIndex add attr => attr.trait-type ===name 
12.nftmeta attributes attributeidx.value = value 
13.sftnftmeta and add...nftmeta add attributes nftmeta.attributes 
 
Introduce Verification architecure 
What you want to do is upload the image to pinata, send the data verify the account. Needs to be some sort of verification before a user can make his/her own nft 
 
 

Client/server 
Get message, message is going to be generated to the server. Endpoint at the server will be api and server 
Message on the server will be an object going to be a contract address, going to be random id 
Network is here and address is below  
When message is constructed is going to be a session 
SetSession has a message 
Send the setsession message to the client 
Going to store a cookie in the server 
Message going to be stored in the cookies 
Create a signature provide the following data a message account number and password 
Create message account and a password 
message account password on the client side 
third step is to verify the address making request to server api/verify and is going to be a post request 
body 
api/verify post request 
body in the request in the 3 data address signature nft 
unsigned message from session  
Compare unsigned message with a signature 
match the sign and unsign w/ address 
upload nft if address not valid get error 
Handle response 
Generate a message 
 
 
With Iron Session 
1.Install what you need to install. npm install next-iron-session uuid axios 
2.Export function withSession(handler:any){ 
	return withIronSession and pass the handler here and the configuration 
} 
3.Need to provide 3 values in the authentication system 
Password 
Cookie Name 
Cookie Option 
4. Add password: process.env.SECRET_COOKIE_PASSWORD as string  
5 Add secret cookie password to the .env development 
6.CookieName= nft-auth-session 
7.Add cookieOptions: { //only true in production 
	secure : provess.env.NODE_ENV===’production’ ? true: false 
} 
8.Import the contract in the utils to get the contract address and have a contract in the public folder and get the nftmarket.json 
9.Get the networks and get 5777 and get an address. That’s the value that we want to get 
10.Can use const contractAddress = contract[”networks], ” address” 
11.Create const targetNetwork = and get the value of 577 from the target network and use the process.env and going to be using it in the client side. Process.env.Next_Public_Network_id . 

12. Copy this next public network, luckily we already have it 
13.Get password, cookie name is nft-auth session and then create a cookie for production mode and then add the contract to networks and target network and then process.env.next_public_network_id 
14.Can write const Network and add 5777 ganache 
15.Add type Network= typeof Networks 
16.process.env.NEXT_PUBLIC_NETWORK_ID as keyof Network 
17.Need to export const contract address 
 
Create message in server 
1.Add verifiy ts file 
2.Import {v4 as uuidv4} from “uuid”; //generates a random id ,generate random ids 
3.import {Session} from “next-iron-session" 
4.Import {NextApiRequest, NextApiResponse} from “next” 
5.Add export default and add import withSession from “./utils” 

6.Add withSession and add req nextapirequest and session and have session with response nextapiresponse  
7. If req.method === “GET”) { 
	try{ 
     const message = {contractAddress, id: uuidv4()}; 
     req.session.set(“message-session”, message); 
     await req.session.save(); 
}catch{ 
	res.status(422).send({message: “Cannt generate a message”}} 
} 
}else{ 
res.status(200).json(message:”Invalid api route”) 
} 
}) 
8.Add res.json(message) 
 
Fix Reload of the browser 
1. Add a set timeout w/ the global listeners and with window ethereum  
 
Sign Message 
1.Create a signature so you can sign the message in the meta mask 
2.Const {ethereum} = useWeb3();  
3.createNFT and add const accounts = await ethereum?.request({method: “eth_requestAccounts”}) as string[] 
4.const account= accounts[0] 
5.const signedData = await ethereum?.request({ 
	method: “personal_sign”, 
      params: [] 
}) 
6.Add JSON.stringify(messageToSign.data), account, messageToSign.data.id] 
7.console.log the signeddata 
 
Verify form data 
1.Created the signature for the message now have to verify the address and the form data 
2.Can also use fetch or use axios await axios.post(“/api/verify”, { 
     Data that we want to send, address: account, 
     add signature: 
     nft: nftMeta 
}) 
3.Add verify.ts and add if(req.method ===”POST){ 
	try{ 
           const body = req.body; 
           const nft = body.nft as NftMeta 
           Can get the nft values  
          add an if else if I dont have a nft image name nft description or nft attributes then return res.status(422).send(“Not all form data are included”) //write whatever you want otherwise 
 
add a res.status() 
	}catch{ 
	        res.status(422).send({message: “Cannot create J5.N file”}) 
       } 
 
 
} and add else if as well  
 
 
Get Session Back 
1. In the verify.ts file add the return to all the functions so this way something is displayed 
2.Verify the data and check the address check middleware 
3.Req.session.get() 
4.Go to utils file and export const ddressCheckMiddleware =() => { 
 
} add the request and add the response  
Nextapi request, and response 
5.Const request message 
6.Add const message = req.session.get(“message-session”) 
7.Add console.log(message) 
8.Resolve”Correct Address 
9.Uncomment verifiy.ts and add req,res and make sure its imported 
10. Make sure its await 
11.Add a debugger  
12.If you remove the cookie, youll get a json.parse error 
 
Get contract server side 
1. Import {NftMarketContract} from “@_types/nftMarketContract” 
2.Add const message = req.session.get(“message-session”); 
3.Add const provider = new ethers.providers.JSONRpcProvider(“HTTP://127.0.0.1:7545”); 
4.Add index.tsx is going to be our ganache 
5. Add contract = new ethers.Contract( 
contractAddress,  
abi, 
provider 
) 
6. As unknown as NftMarketContract; 
7.const name = await contract.name(); 
8.Add new Promise(async(resolve,reject) 
9.console.log(name); 
 
Verify Signature 
1.Import npm install ethereumjs –util 
2.Import * as util “ethereumjs-util” 
3.Let nonce: string | Buffer  
4. let nonce: string | Buffer =  

"\x19Ethereum Signed Message:\n" + 

JSON.stringify(message).length +  

JSON.stringify(message); 

Add x19 ethereum signed message json.stringify(message).length 
Json.stringify(message).length and json.stringify(message) 
 
5.Creates a buffer and can get parts of the signature  
nonce = util.keccak(Buffer.from(nonce, "utf-8")); 
const { v, r, s } = util.fromRpcSig(req.body.signature); 
const pubKey = util.ecrecover(util.toBuffer(nonce), v,r,s); 
const addrBuffer = util.pubToAddress(pubKey); 

const address = util.bufferToHex(addrBuffer);andd nonce and add v,r,s 
 
6.Unsigned message and match sign and unsigned message 
7. Add const addrBugger = util.pubToAddress(pubKey); 
8. Const address = util.bufferToHex(addrBuffer); 
9. Console.log(address) 
 
Upload Image 
1. Create a white listed address with different addresses 
0Xs2 
0X37 
 
If it is contained, then you can create an nft 
2.Ask your users to provide some data to verify themselves 
3.Only administrator of your page can add address 
4.Go to pinata and connect the api key and add the secret_api_key 
5.Pinata API Key = edwedwedwedwed 
6.Copy the secret key as well= wefwefwefwef 
7. Go to utils.ts and create an export const pinataApiKey = process.env.Pinata_api_key 
8. Create an export const pinata api secret key and create the same process.env  
9.Go to verify and add await axios and add the pinata.cloud/pinning/pinJSONToIPFS 
10.PnataMetaData and add name : uuidv4 and pinata content : nft 
11.Add headers and add pinata api key and add pinata api key 
12.Add pinata secret api key 
13.Add const await axios.post jsonResponse 
14.Instead of nft has been created can just import the jsonRes.data 
 
Get Byte Images 
1.Name and image and add upload file 
2.Add onChange ={} to create.tsx and add hangle Image 
3.Go to create.Tsx and create const handleImage and add =(e: changeEvent<HTHMLInputE4>) 
4.Add if(!e.target.files){ 
	console.error(“Select a file”) 
	      return  
} 
 
const file = e.target.files[0]; 
console.log(file) 
 
5.Dont want to get the file want to get the raw bytes get the const bugger = await file.arrayBuffer(); 
6.Add async to the handleImage 
7.Need to format the byes of the array 
8.Add bugger = await file.arrayBuffer(); 
9. Add bytes = new Uint8Array(buffer) 
10.console.log(bytes) 
11. Upload an image and should have the bytes 
 
Get signed Data (The contract address and the ip) 

1.Always want to make sure that the account information is correct. Since we’re making function reusuable can add it to create.tsx. 
2. Add getSignedData = async() => { 
 
} 
3.Go to try nd get the const messageToSign and the signed data and put it into the getSignedData 
4.Can measure it in try catch and add the signeddata and account  
 
Image upload endpoint 
1. Image address, signature, nftMeta and copy the code and add the data to the try 
2.Add api/verify image and address signature and add nft and add the nftMeta data 
3. Send the bytes to the signedData and the bytes 
4.Add the contentType: add the file.type  
5. Create a random name fileName: file.name also includes the extension of the name and want to remove the file and replace the the exentsion with empty string 
6.Data that’s going to be sent to the server 
7. Go to the file structure and go to the api and go to the verify-image.ts 
8.Export default withSession((requestL NextAPiRequest, res: NextApi resoonse) 
session object is included 
9. Create Session and withSession 
10.Add if(req.method===”POST”) and create an else return res.status(422).send( 
message: “Invalid end point”)} 
12. Making a get request and seeing if it is === post if it is then return res.status(422) 
13. Can access the file name and the type 
14. Const {} = req.body; 
15. Looking for the bytes, fileName, and the the contentType  
16.Go to nfts and add an export file 
17. Export rtype File req ={ 
bytes = Uint8Array; 
content type; string; 
fileName:string; 
18. Can write fileReq = req.body in the verify-image 
19.If !bytes ||!ilfeName || !contentType){ 
can return res.status(422).send({message:Image data are missing}} 
20. Otherwise can continue and check await address (req,res) 
21.Return res.status(200)..send({message: “Image has been created”}} 
22.console.log(fileName) 
23.console.log(contentType) 

Fix image select issue 
1. if (!e.target.files || e.target.files.length === 0) { add this line to the create.tsx and the issue should be solved 
 
 
Fix image select issue 
1. Add the length===0 
if (!e.target.files || e.target.files.length === 0) { 
 
Upload image success 
1.Add buffer and add object values 
2.Import form data 
3.add form data = new form data 
4.form data.append() 
5.import v4 
6.Await axios.post and add https://api.pinata.cloud/pinning/pinFileToIPFS” add form data 
add maxbodylength and add infinity 
7.Add headers { 
 
	“Content-type”: `multipart/form-data; boundary = ${formData.getBoundry` 
} 
8. Provide pinata_api_key 
9.provide api secret key 
 
Store image to state 
1.Go to create.tsx and add console.log(res.data) and go toipfshash and duplicate and create a type for it in the nft.ts 
2. Export type PinataRes = { 
IpfsHash: string; 
pinSize: number; 
timestamp: string; 
isDuplicate: boolean 
} 
3. Add setNFTMeta{ 
	...nftMeta, 
      image; ` 
 
but before that add to the .env development public pinata domain  
} 
4.nftMeta.image and go to <img src=efwefwefwefwef> 
 
Check NFT Structure 
1.Go to uploadMetaData, add it to const res = await axios.post(“/api/verify”) 
2. Const data = res.data as PinataRes; 
3. SetNftURI(` ${process.env.NEXT_PUBLIC_PINATA_DOMAIN`}/ipfs/${data.IpfsHash)`: 
4.Create a createNft = async() => and add the const nftRes = await axios.get(nftURI); 
5. Add const content = nftRes.data 
6.Object.keys(content).forEach(key=> and add an if else statement  
7.If allowedfields.includes the key throw an error invalid Json structure and then add a catch(e: any) 
8.add console.error(e.message) 
9.Add onClick={createNFT} 
 
Get Price 

1.Import the state and import price and set price with use state 
2.Change the onclick handler ((e) => setPrice(e.targetvalue) 
3. Value={price} 
 
Create a NFT 
1.Create an await contract?.mintToken. NftURI, ethers and import ethers 
2.ethers.utils.parseEther(price), { 
 
} 
) 
3.Add value: ethers.utils.parseEther(0.025.toString()) 
4. Add await transaction and add const tx.wait and hadnle alert nft was created 
 
 
 

 

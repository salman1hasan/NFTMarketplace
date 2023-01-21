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

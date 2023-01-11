 
NFT Marketplace [Rough overall notes to have a general idea of what im making] 
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
42.NFT security is the most important part of this project so have to keep this in mind. Always review a smart contract. Always continue to reevaluate 
 
Front end development 
1.Download npx create-next-app 
2.Delete app folder 
3.Also make sure typescript and eslint is deleted 
4.Delete the api folder 
5. Make changes to the app.js and make it into an arrow function 
6.Index.js remove all the elements and use rafce and then create home 
7.Home Module.css can delete and the global css can also delete the extra root stuff which is there cause of nextjs 13 
8.Delete the read me and add nft marketplace note 
9.One of the most important things is coding file structure and what we can do is use reuseable components 
10.Make the components folder and index.js and create three folders button, footer,navbar 
11. Add componentindex.js instead of index.js to stop confusion 
12.In the button footer and navbar create a jsx file and a module.css file to style properly 
13. In the navbar, theres going to be a lot of extra folders, youre going to have a discover folder, helpcenter, notification, profile, and sidebar. All of these will have a jsx file and will also have an index.js 
14. In the index.js going to import the navbar components discover helpcenter profile notification and sidebar and export 
15.Add rafce for all of them and make sure you have the styles imported 
16. Install React-Icons and in the navbar make sure you import use state and use effect and import image and import link and import mdnotification and also import all the navbar components as well 
17. In the navigation bar import use state The useState() is a Hook that allows you to have state variables in functional components . so basically useState is the ability to encapsulate local state in a functional component. 
18.Its going to have a discover, help, notification,profile ,opensidebarand what we’re going to do is add the setdiscover, sethelp etc 
19.Going to import div classname for all the files and add a styled navbar a navbar container and a navbar container left and right 
20. Inside of this were going to have a style logo with nft market place and have the width and height be 100 
21.Then from there want to make a search input and inside that well have another left box input as well 
Always give descriptive names 
22.Input type text and a placeholder and then get your bsSearch on click with a style.search.con 
23.Then you can start working on the right section 
24.Style.navbar container right similar to the left version 
25.Include the <p> (e) and add discover and include a navbar discover right box 
26.And then you gotta include the discover box 
27.Const open menu and include e and add const btn text and then add if btntext ===discover, 
setdiscover (true) 
sethelp(false) 
setnotification(false) 
setprofile(false) 
else if btn is helpbox then going to change it to  
setdiscover(false) 
and sethelp(true 
28.Go to the end of the left section and add div className = style.navbar_container_right 
29.Then add discover container right as well to the section 
30.Add {Discover && className ={Style.navbar_container_right_discover_box} 
31. Close the discover components  
32. Add a {style.navbar_container_right_help}> <p on click={(e)=> open menu(e)}>Help Center> 
{help &&( 
<div className={style.navbar_container_right_help_box}> and add help center 
33. Essentially what im doing here basically is and then create a Notification and add <div className={Style.navbar_container_right_notifiy} what this notify thing is when you click it the button is able to click and move 
34.Notification className={Style.notify} and onClick={} => openNotification and then from there you gotta make the const openNotification 
35.If the notification component doesn’t exist, setNotification(true), setDiscover(false), setHelp(false), setProfile(false), else setNotification(false) 
36.Then the notification button has to be rendered with {notification && <Notification/>} 
37. Create button and div className ={Style.navbar_container_right_button}> 
38.I gotta add the button as well and the btn=”text” 
39.In addition I got to add a user profile as well to make this work as well  
40.<div className={style.navbar.container.right} what this basically does it helps us with the css classes. The best way to have specific css for files in next js is to use js and jsx 
41.Then add style container right profile and add image.users1 with alt witdh={40} and height={40} and add onclick Open profile and add className to style container right profile 
42.Profile and add && <Profile/> 
43.{Menu button} <div className={style.container.right.menubtn}> 
44.CgMenuButton className = {Style.menuIcon} and add onclick=> openSidebar 
45. Then go to Sidebar component and add openmenu with div className={Style.Sidebar} 
46. Creating this menu button and then I have to render this sidebar with open sidemenu and sidebar set open side menu 
47. Const open profile if(!profile) setProfile(true), setHelp(false), setDiscover(false), setNotification(false), and then add else setProfile(false) 
48.And also have to create this openSideBar with an arrow function if(!openSidebar), setOpenSideMenu(true), else setOpenSideBar(false) 
49. Since its going to be available In every single page were going to import the navbar in the myApp and then from there add it to the myApp which Is basically the main page of the file 
50. For the componentindex.js have to add the export the {button, footer, and navbar} 
51. Go to your discover page and then from there add import Style from ‘./Discover.module.css’ 
52.Const discover =() => { 
  const discover =[ 
  name: “collection” 
                            link: “collection”, 
  }, 
  name:”Collection” 
  link: “collection” 
        } 
 ] 
} 
 
in this file add the name, link and add a few collections in object format. After the name link and all the objects are created then from there add discover.map {(el,I} and then you have to add a key <div key={I+1} className={style.discover}></div> 
53.Then need to import Link href={{pathname: `${el.link}`}} and add <Link> 
54.Import Link from “next/link” and add an internal import Style from ‘./HelpCenter.module.css 
55.Add const help center =() =>{ 
const helpCenter =[ 
] 
and add all the elements where you put name and link in an object sup and signin  
56. Then from there add div className={Style.box}> and add helpCenter.map((el,I)) 
57. Have a classname which will have style.helpcenter 
58. And from there add a link href = with pathname and have el link and have </Link> and have el.name 
59.Then go to the nofitication and import the image and do the internal import and import the css file 
60. Have to import the images itself “../../../img”; 
61. Const Notification=() =>{ 
return ( 
<div className and add style.notification with </div> 
) 
62.Add a <p> notification and add div className={Style.notification_box}></div> 
63.Add a div className={Style.notification_box_img}> and add <Image/> 
64.Add Image src and add images.user1 and add alt = profile image with width and height of 50 
65.Add Shoaib Akhter and add the<p> with measure action your user. Basically just displaying some box ingo and notification period and some data 
66.This span className and add style.notification_box_new  
67. Next is to work on the profile component and import Image from “next/image” and import FaUserAlt and from ‘react-icons/fa’ 
68.Add FaUserAlt and add FaRegImage and have to have FaUserEdit 
69.Import MdHelpCenter from react-icons/md 
70. Import TbDownloadOff from react-icons/tb and import TbDownload 
71. Have to import const Profile=()=>{ 
return <div>Profile</div> 
} 
72. Add Internal Import and import the style from ‘./Profile.module.css’ 
73. Import the images from ‘../../../img’; 
74. Import Link from “next/link”  
75. It is going to have Style.Profile and is going to have div.className Style.profile_account and also gotta add the images.user1 
76.Add div className={style.profile_account_info} and a </div> 
77. In addition add Shoaib Bhai and also add <small> with the size that is needed 
78.Add a style profile menu and add style.profile_menu_one  and add style profile menu one item 
79. Add FaUserAlt and add <p> and add the link href and add pathName: ‘/myprofile’}} 
80.Add FaUserEdit as well 
81.Add a style.profile_menu_two and add a profile menu one item 
82.<MdHelpCenter/> <p> Link href ={{pathname:’/help’}}> and add </Link> and add </p> 
83.Also add TbDownload/> as well  
84.Go to the sidebar and import usestate from react and use import image from next/image 
85.Import Link from “next/link  
86. Import GrClose from react icons/gr and import TiSocialFacebook and add all the button from “../../../Button/Button 
87.Then go to sidebar and usestate. Import useState(second) and add OpenDiscover with SetOpenDiscover and SetOpen. 
88.Import discover and add the discover navigation menu 
89.Go to sidebar and add div className={Style.sideBar} 
90.<GrClose ClassName={Styles.sidebar_closeBtn} and add onclick with closeSideBar 
91.Div className={Style.sideBar_Box}  and add images.logo/> and add alt=”logo” width={150} height={150} 
92.<p>Discover the most outstanding articles on all topics of NFT’s and your own stories</p> 
93.Div className ={Style.sideBar_social}> and add TiSocialFacebook 
94. <ahref =”#”> <TiSocialInstagram> and add all the social icons that are necessary to be added 
95.{ 
openDiscover && ( 
 <div className={Style.sidebar_discover}> 
 {discover.map((el,I)=>{ 
 <p key={I+1}> 
<Link href={{pathname: `${el.link}`}></Link> 
</p> 
))} 
   </div> 
) 
96. <div className={Style.sideBar_menu_box} and add onClick={() => openHelpMenu()}> 
97.<p> Help Center</p> and add <TiArrowSortedDown/> </div> 
98. { 
openHelp && ( 
 <div className={Style.sideBar_discover} 
{helpCenter.map((el,I)=>( 
<p key ={I+1} 
<Link href={{ pathname: `${el.link}`}}>{el.name}</Link> 
))} 
</div> 
) 
} 
99.<div className={Style.sideBar_button}></div> 
100.<Button btnName=”Create”/> 
<Button btnName=”Connect Wallet”/> 
101. Const openDiscoverMenu =()=>{ 
if(!openDiscover){ 
setOpenDiscover(true) 
}else{ 
setOpenDiscover(false) 
} 
102.Const openHelpMenu =() =>{ 
if(!openHelp){ 
setOpenHelp(true) 
}else{ 
setOpenHelp(false); 
} 
} 
103. Const closeSideBar = { 
 setOpenSideMenu(false) 
} 
104.Now we get to the point where I’m styling the navigation bar. Taking notes on this isn’t really worth the time as im not the biggest fan of this navigation bar but its good to know 
105. Good thing to know with the css and github stuff is there is root icons in the global you can edit anything with jsx youre able to edit specific things 
106. Work with the sidebar as well to create the project 
107.Create BigNFTSlider which includes jsx and module.css 
108.In the file, take a look at AifillFire, Aifillheart, and AiOutline, basically are going to add a bunch of react icons 
109.And then import the components of the project, including button, images, and styles 
200. Add a const [idNumber, setIdNumber] = useState(1) 
201.Add a const slider where you add a bunch of data, with the likes of title, id, name, collection, price etc and make 4 sections with different images  
202. Start structuring the file and also when youre using jsx its nice to be able to use Style. and its easy. All you gotta do is add Style.jsx and you’re able to complete it 
203.Import image and import IDNumber as well 
204.In order to get this to work what you have to do is import that in the componentindex.js and add bignftslider/bignftslider  
205. Add this to index.js and add {slider.data[idNumber]} and add md verified.  
206. Then add bignftslider_box_left_creator_collection and add the creator collection icon and remove the brackets 
207.Add the bigNFT Slider_box_left_bidding and this is where the nft price is going to go  
208. Then add the timer for the NFT Slider Box Left Bidding Box 
209.Add the sliderData[idNumber].time.days and add the <span>days</span> 
210.Then add the Hours and minutes as well.  
211.Create two big nftslider buttons box left button and button name =plac handleclick and button btnName=”view” handleClick ={}/> 
212. Add bigNFTSlider_box_left_slider} and add TbArrowBigRightLine with a className={Style.bigNFTSlider_box_left_SliderBtn_icon} and add an onclick to => inc() 
213.Add image src ={sliderData[idNumber].nftImage} and add alt =”NFT Image” 
214.Then create another Style.bigNFTSlider_box_right_box_link and add AiFillHeart/> and add sliderData[idNumber] 
215. The idNumber and setIdNumber add to the useState(1) and add the const sliderData ={ 
and add all the information that is necessary for the data to exist 
216.Then add the const inc=useCallBack(()=>{ 
if(idNumber+ 1<sliderData.length){ 
     setIdNumber(setIdNumber+1) 
}, [idNumber,sliderData.length]) 
217. Add const inc = usecallback(()->{ 
if(idNumber>0{ 
setIdNumber(setIdNumber+1); 
} and add [idNumber,sliderData.length]); 
218.Add useEffect(()=>{ 
}) 
219. Not going to write notes on all of the bignftslider notes but basically style it so the components look good. Its going to be repetitive such as  width margin display etc. All of this can be found online. In addition going to be adding a bunch of media queries as well to make sure that the site is mobile responsive. 
.NFTCard{ 
width: 80%; 
margin: 0 auto; 
display: grid; 
grid-template-columns: repeat(3, 1fr); 
gap: 3rem; 
margin-bottom: 10rem; 

} 
 
220. Something I didn’t know in css, grid-column 6/-1 
https://developer.mozilla.org/en-US/docs/Web/CSS/grid-column 
 
221.The inc part was basically used to move the pictures from one movement to the next movement 
222. Create a file Subscribe and add jsx and import subscribe module.css and go to componentindex.js and add the subscribe from ‘./Subscribe/Subscribe and then go to index.js and also add index.js 
223.Go to subscribe RiSendPlaneFill and then add Image from “next/image” 
224.Import images from “../../img” 
225.Go to const subscribe =() =>{ 
 add style.subscribe add style.subscribe_box and then add subscribe_box_left 
} 
226. Add <h2> Never miss a nft drop</h2> 
227.Add <p> styling as well do add more. The format of these divs are really important have to have the div in 3  
228. Then add 3 div classNames and then add a span 01 and 02 and add the files ares are necessary 
229.Add RiSendPlaneFill and className={Style.subscribe} 
230.Add div classsName={Style.subscribe_box_right> and then add the image src={images.update} 
231. Then go to subscribe.module.css and add all the css files that are necessary 
232. Import the title.jsx and add all the const {title} and go to the componentsindex.js and add title and add title to the componentindex.js and the index.js 
233.Add the <div className and add the style box as well and add the h2 and add the p as well 
234.Then go to index.js and add the heading browse by category 
235. Title Module.css and add all the files that are necessary 
236. Add Category to the file and add rafce and add the Category 
237. Then add the index.js and add the return <div> Category</div> 
238. Also complete Category Array.map ((el,I) and the style.category_box ={key 1+1} 
239.Add images src={images.createBackground} className={Style.category} with alt and width 
240.In addition add style.category_box_title and add <span> with <h4> entertainment and add small 1995 241. Then complete the Category.module.css 
242.Create a Filter.jsx and add <div> Filter</div>, and add import <div Style from ‘ ./filter/module.css’ 
243. Go to components.index.js and then go to index.js and add filter from “./Filter/Filter” 
244.Then go to index.js and add index.js  
245.FaFilter, FaAngleDown, FaAngleup and add all the files to react-icons that are going to be necessary 
246.Go to const [Filter,setFilter] and add useState(true) and add all the image, video, and music as useState as well 
247.  Return div className and add all the buttons and add onclick arts, music, sports, and photography 
248. Add FaFilter add <span> with {filter ? <FaAngleDown/> and add the <FaAngleUp/> 
249.Add all the filter && ( 
<div className={Style.filter_box_items}</div> 
250.Add the icons FaWallet and add AiFillCloseCircle  
251. Add all the files necessary for example small images and also add small videos 
252. Add the music and also add the FaUserAlt  
 
<div className={Style.filter_box_items_box}> 

<div 

className={Style.filter_box_items_box_item_trans} 

onClick={() => openVideo()} 

> 

<FaVideo /> <small>Videos</small> 

{video ? <AiFillCloseCircle /> : <TiTick />} 

</div> 

</div> 

 
 

<div className={Style.filter_box_items_box}> 

<div 

className={Style.filter_box_items_box_item_trans} 

onClick={() => openMusic()} 

> 

<FaMusic /> <small>Musics</small> 

{music ? <AiFillCloseCircle /> : <TiTick />} 

</div> 

</div> 

 
252.Create an openFilter and add if(!filter){ and add setFilter(true) and add else setFilter(false) 
253.Create the logic for the open video and the aifillclosecircle and the openmusic to see if there is going to be  
254. Create all the css files for setFilter 
255. Create NFT Template and add it to the componentsindex.js and add it to the index.js file as well 
256. Add import {AiFillHeart} and add{BsImages} and import images  
257.Add the featureArray =[1,2,3,4,5,6] 
258. Then add the const [like,setLike] and set the useState(true) 
259. Return ( 
<div className={Style.nftcard}> 
and then from there add the featureArray.map and add the export default NFT Card and add the (el,I) 
260.Style.NFTCard_box and then add the div className={Style.NFTCard_box} and then add key={I+1} 
261. Add div className={Style.NFTCard_box_img} 
262. Add the image src={} 
263. Then from there add the div classNames and add all the classNames with style nftcard_box_update and left and left like and add the onClick and add the likeNFT 
264. Add the like ? With a tenary operator and add the aioutlineheart and aifillheart 
265. Then add the style.NFTCard_box_update_right and then add nft card box update right info with remaining time and add <p> 3h: 15m :20s and add another div 
266. Then add div className={Style.NFTCard_box and add the clone number, this is going to be changed later and then from there add the NFTCard_box_update_details_price_box_box and add the other div className={Style.NFTCard_box_update_details_price_box_bid} 
277.Add the small and <p> and then from there style.NFTCard_box_update_details_price  and stock  
278.Lastly add the nftcard_box_update_details_category 
279.Rafce and add the collection import React from “react” and then add the import Style from “./Collection.module and add the const collection =()=>{ 
return <div> Collection </div> 
}; 
280. Add the collection.jsx and add all the collection.module.css and then do the usual componentsindex.js and add the index.js 
281.Import React and import BsFillAlarmFill, BsFillCalendarDateFill, and BsCalendar3 from react-icons 
282.Render the const popular selection and have the useState(true) and then have following and news to false 
283.Take const cardarray =[1,2,3,4,5,6,7,8] and create 8 components 
284. Add followingArray =[1,2,3,4] and then add const news array as well 
285. Add div className={Style.collection}> and then from there have div className = Style.collection_title and then have h2 and have the div classname and the other div className with proper format, title, collections and btn 
286. Create a button onclick and have it be open populat 
287. BsFillAlarm and add last 24 hours and then add onclick = openNews and also have OpenFollower 
288. Going to create a dynamic block and add populat && ( <div classNam={Style.collection_box}> and add card array.map((el,I)-> ( 
<Component key={I+1}/> 
289.Add following && ( <div className={Style.collection_box> and add the cardArray.map((el, I) 
290. Add following and add the news array as well to make it work 
291. Add the newsArray and add the followingArray and then add the const openPopular function this way it can open and close  
292. Add the openNews and then add the openFollower as well  
293. Then from there add all the css files for the collection file 
294.Then the next step is to work on the daycomponents, import image and then import icons mdmaterial icons and add an internal import and add images and start working on jsx and have a file called DaysComponent and is going to have a days component and then is going to have a days component box and days component_box_img  
295.In addition add the images with create background and days component img with a width and height of 500 
296.Add 3 images to the file. In addition, then add the days component box title with a h2 tag with a days component box title and info and then add days component box title info profile  
297.In addition add all the images to the images.user1 with the width and the height and then add the <p> with the creator and span Shoaib Bhai etc 
298.Then from there add the ether file 
299.Create all the css files necessary to make the module.css 
300. Create follower tab and add the jsx and then add the followertab.module.css 
301. Make sure you import it in the componentsindex.js and the index.js 
302. Import useState and useEffect icons and import {RiUserFollowFill} and then import the const cardArray=[1,2,3,4,5,6,7,8] 
303. Add the following array and then add the news array 
304. Add the div className and add the follower tab and the follower tab title 
305.<h2> Top creator list... and then add the div className style followers tab and tabs and then add the followers tabs btn 
306.Add the openPopular and add the click button to the file 
307.Add 3 of these buttons and then add popular following and then add the news as well 
308. Add the popular and add the div className and add the followertabcard 
309.Import the Follower tab card and from the same directory 
310.Go to followertabcard and add the image and add the mdverified and the titick and also add the following card as well 
311. Copy the first place emoji and get the follower tab card and the follower tab card rank 
312.Add the follower tab card box and then add the follower tabcard box image 
313.Add all the images and add the images that are necessary for the project to work 
314.Add the Giada man and then add the span with mdverified  
315.Add the <p> tag 12.232. and add another p tag 
316. In addition, add the ? onclick and then add the TiTick and then add the following 
317.In addition, add the follow me and set the button so it works properly 
318.Gotta make all the css files 
319.Thing to keep note of the css file with the image doesn’t work because something is depcreatied I think it was object fit or maybe it’s a css issue, don’t know, but it didn’t work 
320.Make sure the object is following not follow me 
321.Make more changes to the css 
322. The idea is to build the audio component in this NFT Marketplace and make a Audio Live file.Make sure to import this in the componentsindex.js and the indexjs 
323.In the index.js going to import audio live. Import the audioLive and import the audiolive_box and the audiolive_box_left 
324.Add the audio card and add the audio card small and create a file audiocardsmall and audiocard small module css 
325. Import audio card and then import the audio card small to the file as well 
326. Import the image from “next/image and also import the react-icons and import the {tbPlayer} as well and the tbplayerpause 
327. Import the style from ‘./AudioCard.module.css’ and in addition import the images from ‘../../../img’ 
328.Add the const [like and setlike] and also add the useState(false) and the const [play,setPlay 
329. Furthermore add the divclassName and add the style.audioCard and add the audioCard_box 
330. Import the div className = {Style.audioCard_box_like} and add onClick={()=>likeNFt()} 
331.Import like ? ( <AiFillHeart and add the className={Stylle.audioCard-box_like_icon} 
332. Import AiOutlineHeart className={Style.audioCard_box_like_icon_unlike}/>. This is the specific way to make sure that a person can like and dislike the picture 
333.Import the div className and add remaining time small and add h5 3h:15m:20s 
334.Import div className={Style.audioCard_box_musicPlayer} onclick as well  
335. Add play ? And add div className={Style.audiocard_box_like} and add tbPlayerPause/> 
336. Import the style.audioCard_box_details and add the Style.audioCard_box_details_info and then add the <h4> NFT music #1</h4> 
337. Add a div className={Style.audioCard_box_details_info_price> 
338.<small>Price</small> 
339. <div className={Style.audioCard_box_details_info_price} to add more imports and add how many are in stock 
340. Import the image and then add the width and the height add the const likeNFT and add the if(!like){ setLike(true) and else setLike(false) 
341.Add the const playMusic and add if (!play) and add the setPlay(false) 
342. Import div className={Style.audioPlayer}> and then add the Style.audioPlayer_box and then add the image src ={ and add the images.creatorbackground1} 
343. Import the className={Style.audioPlayer_box_img} 
344. Add div className={Style.audioPlayer_box_info} and add the <h4> NFT music #1142  
345. Div className={Style.audioPlayer_box_info_box}> and then add the like profile  
346. Import div className and add the style.audioPlayer_box_info_price and add the small price and add the <p> and add the 1.00 ETH 
347. In addition make sure to add the audioPlayer_box_playBtn} and add the onClick ={()=> playMusic() 
348.  Import all the css files that are necessary to complete this project 
349. Create another component called like profile and add the imageArray.map((el,I) and the <Image src width and height and key for the image  
350.Import all the components to the componentindex.js and then add the AudioCard and add that to the audiocard.jsx  
351. Add the slider component  for the NFT Video Add this to the component and the index js  
352.Import the npm I framer-motion and add the sliderarray =[1,2,3,4,5,6,7 
353. Add the width, setWidth =useState(0), const dragSlider = useRef() and add the slider and the slider box and add the slider box button and then from there add the slider and the slider box button and then from there import motion div and add the style slider box items and the drag slider to the slider 
354.In order for it to work you have to create another component for the slider and add the useEffect and add the setWidth and the dragslider and the dragslider  
355. Have to create another slider function inside of the function 
356.Change the slider and change it to slider key 
357.In the slider card import the like profile and import the image and add the style.slidercard and add motion. This is the design of the ball  
358. Add the image and add the src and add the alt and add the width and the height and the objectfit 
359.Add the slidercard box and the slidercard box title and the like and add the like profile as well this way components can be liked 
360.Add the <p> and the <small> 1 of 100</small> 
361.Add the slider card box price and add the slider card box price 
362.Add the current bid and the paragraph as well 
363.Add the small and add the paragraph as well 3h: 15m 
364.Add all the css files necessary for the project 
365.Make sure to add the componentindex.js and the indexjs 
366.Make sure to add the slider card module.css to the file as well. This is going to be redsigned later, but its important that i make the template the way it is. I might redesign before continuing but actually im going to complete this template and then from there and then recreate 
367.Slider card box and box-shadow and the box-shadow  
368. Add the slider array and customize It with the images and the background images 
369.Create Brand and create Brand.module.css and add the const brand <div className={Style.brand} and add the style brand box, in addition add the image src and the headers that are necessary 
370.In addition add the earn the free crypto and the <p> for the creative  agency 
371.Add a button create and add another button   
372. Import all the css files necessary for the brand and left_btn 
373. Import the Video and the video.jsx and the video.module.css and add all the files what is necessar 
374.Import the componentsindex.js and add the index.js and add the components index.js 
375.Add the span and add the paragraph and then add the necessary images, but the thing here is object fit is not there anymore so basically I have to leave it the way it is  
376.Add all the css files that are necessary 
377.Create the I, el and make all the necessay changes to followertab 
378.Collection followetab and slidercard 
379.Add a collection page and add the collection page and the collection profile with the necessary files which is the module.jsx and add the css file as well 
380.Go to import collection index.js and then from there and import the banner and the collection profile 
381.Import this to the collection page. The banner is going to be a design page that is made for the images 
382.In addition make sure to import the slider and the brand from the components file 
383.Add the div className={Style.collection} and then from there import the banner and import the images.background1 
384. Import the image from “next/image and also import the style from the banner.module and add const banner = ({bannerImage}) and add the div className={Style.banner} and add the Style.banner_img> and then import the image src banner image and add the object fit 
385. Add the div className={Style.banner_img_mobile} and add the image src={bannerImage} and  
add the images that are necessary 
386.Then from there do the necessary css files changes to make sure that the Banner.module.css is compelte 
387.Import all the social media icons for collectionProfile and import the style like usual and import the images as well. 
388. In the collectionPage make sure that you add the cardArray and make sure that cardArray=[1,2,3,4,5] 
389.Add the div className={Style.collectionProfile} and add the div className 
390. Add the div className={Style.collectionProfile_box}> and the collectionProfilebox left as you can see this is just the front end stuff with the images. 
391. Add the image src and add the images.nft_image_1 and add the alt =”nft image” 
and add the width ={800} and height ={800} and the className with Style.collectionprofile-box_left_img 
392.Add the style.collectionProfile_box_left_social and add all the <TiSocialInstagram> and add the <TiSocialLinkedin> and all the social profiles that are necessary 
393.Add the div className and add the style collectionProfile and box middle  
394. Add a header ta awesome nft collection <h1> and the necessary things 
395.Add the <p> tag and then from there add another {Style.collectionProfile_box} 
396.Add the cardArray.map((el,I}} and add the div className={Style.collectionProfile_box_middle} 
Add the small and add the other small 
397. Add the span and the other span tag  
398. Add the css files that are necessary for collection profile.module.css 
399. Go back to collection Profile and add the <small> Floor price</small? and import the NFT Collection 400.Change the box shadow of the NFT Marketplace 
401.Go to the collection profile. Import the NFT Card two and add the module and the css file, which is the usual 
402.Import the collectionindex.js banner and the nftcarttwo 
403.Import the necessary content for collectionArray =[ 
Add the images.nft_image_1 and all the necessary images 
] 
404.Add the NFTData ={CollectionArray} 
405.Import the image from “next/image” and add the BsImage and add the AiFillHeart and the AiOutline and also import the MdVerified and add the MdTimer from “react-icons” 
406.Import the style from ‘./NFTCardTwo.module.css’ and import the likeprofile from component and component index 
407.Pass the prop NFTData and import the const [like,setLike] and the useState(false) 
408.Import the const [likeInc, and the setLikeInc] and the useState(21) 
409.Add the div className={Style.NFTCardTwo}> and add the NFTData.map and add the el, I and add the div className={Style.NFTCardBox} and add the key={I+1} and add the div className={Style.NFTCardTwo_box_like} and add the other NFTCardtwo_box_like} 
410. Import the NFTCardtwo_box_like_box_box and then import the BsImage className={Style.NFTCardTwo_box_like_box_box_icon} that is necessary 
411.Add the <p tag and add the onClick => likeNft() and the {like? Add the AiOutlineHeart and the AiFillHeart 
412.Import the <span> {likeInc+1}</span} 
413. Div className={Style.NFTCardtwo_box_img> and add the image src ={el} and the usual width height etc 
414.Furthermore add the div className={Style.NFTCardTwo_box_info} and add the div className={Style.NFTCardTwo_box_info_left} and add the <LikeProfile/> 
415.<p> Add the Clone#{I+1} and add the </p> 
416. Add the div className={Style.NFTCardTwo_box_price} and add the second NFTCardTwo_box_price} 
417.Add the <small>Current Bid</small> and add the paragraph tag that is necessarya s well 
418. Add the <p className={Style.NFTCardTwo_box_price_stock} and add the MdTimer/> and the <span> {I+1} hours left</span> 
419.Create the const likeNft and add the if else statement to get the button clicks to work 
420. Add all the css files that are necessary 
421. Go to the pages and add the author.js file that is necessary and import the react and the usestate and the use effect  
422.Import the styles/ and add the styles.css 
423.Add the import {Banner} from the ../collectionPage and also add the banner and the nftcardtwo 
424.Import the author profile card and author taps and tabcard from the authorPage and the authorProfileCard and the authorProfileCard.jsx and the authorpfilecard.css 
425.Add all the images that are necessary to the images.user1 and 1-8 
426. Add the const [collectiables and add the setCollectiables with the useState 
427.Add the created,setCreated and add the useState(false) 
428. Add the like and setLike and the useState(false) 
429.Add the follower and the setFollower to the usestate(false) and the following useState false 
430.Like the the other author.js add the Banner and the bannerImage={images.author} 
431.Import the authorprofilecard and the authortabs and export authorprofilecard and the authortaps 
432. Go to the AuthorProfileCard and import React image and the mdVerified, MdCloud, and the MdOutline} 
433.Add the import {FiCopy} from AuthorProfileCard.jsx and add all the social icons as well and import the BsThreeBots  
434. Add the style and add the images from Authorprofile and also import the images and add the button from “../../components” 
435.With the profile card add the div className={Style.AuthorProfileCard} and import the box as well 
436.Add the style.authorprofilecard and the box img and import the image and the src classname and alt and the width 
437.Add the style.authorprofilecard_box_info and add the <h2></h2> 
438.Add the Style.AuthorProfileCard_box_info_address and add the input type value and the id 
439.Import the FiCopy with the onclick =()> copy Address and the className  
440.Add the button btnName=”Follow’ and add the MdCloudUpload with an arrow function to openshare 
441. In addition add the share && (with a div className={Style.AuthorProfile} 
442.Import all the Social icons in the span that are there in the other components as well  
443. Add the BsThreeBots and add the onClick=()=>OpenReport}/> 
444.Add the report && <p className={Style.AuthorProfileCard} and add the span and theMdOutlineReportProblem/> and report the abuse 
445.Make sure to add the copyAddress function as well and add the copytext with = document.getelementbyid and the myinput 
446.Add the copytext.select() 
447.Add the navigator.clipboard.writetext and the copytext.val  
448. Add the openShare function to make sure that the function can open and close 
449. Create an openReport and make sure that the setReport can oopen as well 
450.Add the necessary css files to the authorprofilecard

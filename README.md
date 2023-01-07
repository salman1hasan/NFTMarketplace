 
NFT Marketplace [Not fully uploaded after complete then going to reupload, showcasing progress]

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

22.Input type text and a placeholder and then get your bsSearch on click with a style.search.com

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
and sethelp(true)

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
 
 
 
 
 
 
 
 
 
 

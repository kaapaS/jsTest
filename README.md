# jsTest
/*
Assessment Requirements
1. Create a variable that can hold a number of NFT's. What type of variable might this be?
2. Create an object inside your mintNFT function that will hold the metadata for your NFTs. 
   The metadata values will be passed to the function as parameters. When the NFT is ready, 
   you will store it in the variable you created in step 1
3. Your listNFTs() function will print all of your NFTs metadata to the console (i.e. console.log("Name: " + someNFT.name))
4. For good measure, getTotalSupply() should return the number of NFT's you have created
*/

const NFTList = [];

function mintNFT (Id, name, eye_color, place, speciality) {
    const nft = {
        "ID": Id,
        "Name": name,
        "eyecolor": eye_color,
        "Place": place,
        "Speciality": speciality
    };
    NFTList.push(nft);
}

function listNFTs () {
    console.log("NFT List\n")
    console.log("----------\n")
    for (let i=0; i<NFTList.length;i++) {
        console.log("NFT: \t\t" + NFTList[i].ID)
        console.log("Name: \t\t"+ NFTList[i].Name)
        console.log("eyecolor: \t"+ NFTList[i].eyecolor)
        console.log("Place:\t\t" + NFTList[i].Place)
        console.log("Speciality: " +NFTList[i].Speciality)
        console.log("-----")
    }
}

function getTotalSupply() {
    return NFTList.length;
}


mintNFT("1","Saturo Gojo", "Vibrant blue", "Tokyo","cursed technique");
mintNFT("2","Naruto Uzumaki", "Blue", "Tokushima ken","chakra affinity");
mintNFT("3","Monkey D.Luffy", "Black", "Dawn Island, Goa","Rubber devil fruit");
mintNFT("4","Tanjiro Kmado", "Red", "Okutama", "Dance of Fire");

listNFTs();

console.log("\nTotal number of NFTs: " + getTotalSupply());

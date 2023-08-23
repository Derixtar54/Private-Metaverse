This is a Solidity smart contract for a basic NFT marketplace called Metaverse. Here are some key points about the contract:

-> It inherits from ERC721, which is the standard interface for non-fungible tokens (NFTs), and Ownable, for access control.

-> It uses OpenZeppelin's Counters library to keep track of the token supply.

-> There is a max supply of 100 NFTs set.

-> The NFTs are minted by calling the mint() function and paying the minting cost (set to 1 wei).

-> The mint function takes metadata (name, dimensions etc) and mints an NFT to the caller by incrementing the supply counter and assigning the tokenId.

-> An Object struct holds the NFT metadata. All NFT objects are stored in the objects array.

-> Mapping NFTOwners maps addresses to the array of Object NFTs owned by that address.

-> withdraw() allows the contract owner to withdraw ether balance.

->getOwnerObjects returns the NFTs owned by a particular address.

->To interact with this contract from the frontend, web3.js library can be used in the following ways:

*Using web3.eth.Contract to instantiate the contract ABI and interface with its methods.

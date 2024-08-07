# SWISSTRONIK Technical Task 3

Steps to mint ERC-721 Token

1. Clone repository
```shell
https://github.com/fung93/swisstronik-task-3-ERC721.git
```
```shell
cd swisstronik-task-3-ERC721
```
2. Install Dependency
```shell
npm install
```
3. Set .env File
```shell
PRIVATE_KEY="your private key"
```
4. Create smart contract
```shell
// SPDX-License-Identifier: MIT
pragma solidity ^0.8.20;

import "@openzeppelin/contracts/token/ERC721/ERC721.sol";
import "@openzeppelin/contracts/access/Ownable.sol";

contract ZunXBT is ERC721, Ownable {
    constructor(address initialOwner) ERC721("FUNG", "FNG") Ownable(initialOwner) {}

    function safeMint(address to, uint256 tokenId) public onlyOwner {
        _safeMint(to, tokenId);
    }
}
```
5. Deploy smart contract
6. Mint token
7. Finished
   - Copy the address and paste the address to testnet dashboard
   - Copy the transaction link to testnet dashboard
   - Push this project to your github and paste the repository link to testnet dashboard

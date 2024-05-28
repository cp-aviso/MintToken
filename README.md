## myToken Smart Contract
This repository contains the Tekken Token (TKN) smart contract, an ERC20-compliant token with additional functionalities for minting and burning tokens. The contract leverages OpenZeppelin's robust and secure libraries.

# MintToken
Here you will see the simple way of creating token in remix
you can see the syntax inside the sol. file 

sample syntax below :

   // SPDX-License-Identifier: MIT
// Compatible with OpenZeppelin Contracts ^5.0.0
pragma solidity ^0.8.20;

import "@openzeppelin/contracts@5.0.2/token/ERC20/ERC20.sol";
import "@openzeppelin/contracts@5.0.2/access/Ownable.sol";

contract AvisoToken is ERC20, Ownable {

    constructor(address initialOwner)
        ERC20("AvisoToken", "AVS")
        Ownable(initialOwner)
    {}

    function mint(uint256 amount) public onlyOwner {
        _mint(msg.sender, amount);
    }

    function mint(address to, uint256 amount) public onlyOwner {
        _mint(to, amount);
    }

      function transferTo(address to, uint256 amount) public  {
        transfer(to, amount);
    }
    

    function burn(uint256 amount) public {
        _burn(msg.sender, amount);
    }  

  
}

## Security
The contract uses OpenZeppelin's implementation of ERC20, which is widely regarded for its security and reliability. Despite this, it's essential to conduct independent security audits and reviews.

## License
This project is licensed under the MIT License.
## Author
Carlo Aviso

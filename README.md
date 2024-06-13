# Beginner_Solidity
// SPDX-License-Identifier: MIT
pragma solidity 0.8.26;

contract MyToken {

    //Public Variable
    
    string public tokenName = "OMKREATION";
    string public tokenAbbrv = "KREAT";
    uint public totalSupply = 0;

    // Mapping from address to balances

    mapping(address => uint) public balances;

    // Mint function to create new token

    function mint(address Add, uint value) public {
        totalsupply += value;
        balances[Add] += value;
    }

    // Burn function to destroy the token 

    function burn(address Add, uint value) public {
        if (balances[Add] >= value) {
            totalsupply -= value;
            balances[Add] -= value;
        }
    }
}

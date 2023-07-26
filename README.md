

# Create a Token
## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. 


## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

## License
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;




contract MyToken {

    // public variables here
    string public tokenname = "META";
    string public tokenabbrev = "MTA";
    uint public totalsupply = 0;

    // mapping variable here
mapping(address => uint) public balances;
    // mint function
function mint(address _address , uint _value) public{
totalsupply += _value;
balances[_address] += _value;
}
    // burn function
function burn(address _address , uint _value) public{
    if (balances[_address] >= _value){
        totalsupply -= _value;
        balances[_address] -= _value;

    }

}
}





## Authors
21bcs3833



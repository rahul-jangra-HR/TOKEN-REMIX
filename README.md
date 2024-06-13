# Token Generating 

This Solidity program is a Token Generating  program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to mint the tokens and the minted tokens could be burnt afterwards. 

## Description

This program  written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain.It includes a mint function that allows authorized accounts to generate new tokens, thereby increasing the total supply and assigning the newly created tokens to a specific address. Additionally, the contract features a burn function, which permits token holders to destroy their tokens, effectively reducing the total supply and allowing for deflationary token models or removal of tokens from circulation

## Getting Started

### Executing program


contract MyToken {

    // public variables here
  string public tokenName = "PROFESSOR";
  string public tokenAbbrv = "PROF";
  uint public totalSupply = 0;

    // mapping variable here
 mapping (address=> uint) public balances;

    // mint function
function mint (address _address, uint _value) public {
    totalSupply += _value;
    balances[_address] += _value;
}
    // burn function
function burn (address _address, uint _value) public {
    if (balances[_address] >= _value) {
        totalSupply -= _value;
        balances[_address] -= _value;
    }
}
}


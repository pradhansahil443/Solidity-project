# Tokens

This Solidity program a basic "Token" program, showcasing the fundamental syntax and functionalities of the Solidity programming language. The main objective behind this program is to offer a stepping stone for newcomers to Solidity, granting them a practical understanding of its workings.

## Description

This program is a simple contract written in Solidity "pragma solidity 0.8.18" , a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a two function "mint" that add and "burn" subtract n numbers of value from totalSupply token. This program serves as a simple and straightforward  to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Installation
To access the smart contract project, you can clone the repository from the official GitHub page.
Paste this  in  your terminal of vscode (Note : use this if only using vs code)
```
git clone https://github.com/pradhansahil443/Solidity-project/blob/main/token.sol
```
### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., module3_token.sol). Copy and paste the following code into the file:

```javascript
pragma solidity ^0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "pencil";
    string public tokenAbbrv = "pen";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _addr, uint value) public{
        totalSupply += value;
        balances[_addr] += value;
    }

    // burn function
    function burn(address _addr, uint value) public{
        if(balances[_addr] >= value){
            totalSupply -= value;
            balances[_addr] -= value;
        }
    }

}

```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile module3_token.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the "mint" or "burn" function. Click on the "MyToken" contract in the left-hand sidebar, and then click on the "mint" function. Copy the "Account" address and paste it in "_addr" and set the value. Finally, click on the "transact" button to execute the function and retrieve the "totalSupply".

Also you can burn(delete) the token with "burn" function.

## Authors

Sahil Pradhan  

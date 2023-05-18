# My Token

This Solidity program is a simple "My Token" program that demonstrates the basic syntax and functionality of the Solidity programming language. The purpose of this program is to serve as a starting point for those who are new to Solidity and want to get a feel for how it works.

## Description

This program is a simple contract written in Solidity, a programming language used for developing smart contracts on the Ethereum blockchain. The contract has a function to get the token information such as token name, token symbol, total supply, as well as a function to mint and burn the token. This program serves as a simple and straightforward introduction to Solidity programming, and can be used as a stepping stone for more complex projects in the future.

## Getting Started

### Executing program

To run this program, you can use Remix, an online Solidity IDE. To get started, go to the Remix website at https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension (e.g., MyToken.sol). Copy and paste the following code into the file:

```javascript
// SPDX-License-Identifier: MIT
pragma solidity 0.8.18;

contract MyToken {

    // public variables here
    string public tokenName = "TWITTER";
    string public tokenAbbrv = "TWTR";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

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
```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18" (or another compatible version), and then click on the "Compile MyToken.sol" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by checking the token name, token abbreviation, total supply, "mint" and "burn" function. Click on the "MyToken" contract in the left-hand sidebar, and then check the token name, token abbreviation, and total supply to gain some information the token. To execute the "mint" function, pass an account from one of the account in the ACCOUNT dropdown above and a token amount. After entering the required parameter to the function, click on the "transact" button to execute the function. Now check the account balance by entering an account to balances field and click the "transact" button. Try burning some token by going to the "burn" function and pass it an account and a token amount. Again, click the the "transact" button to execute the function and check the remaining token on the account as previously mentioned.

## Authors

Jaymes Phimmachack

## License

This project is licensed under the MIT License - see the LICENSE.md file for details

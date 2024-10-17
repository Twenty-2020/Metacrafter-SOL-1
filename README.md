# Metacrafter-SOL-1

This Solidity code demonstrates an example mint and burn functions for tokens.

## Description

The code is written in Solidity, a programming language for developing in Ethereum. The contract contains functions for minting, as well as burning tokens. The program serves as a good introduction to Solidity programming, through the use of functions and variables.

### Executing program
The code can be run using Remix, an online Solidity IDE. Remix can be accessed and used in https://remix.ethereum.org/.

Once you are on the Remix website, create a new file by clicking on the "+" icon in the left-hand sidebar. Save the file with a .sol extension. Copy and paste the code into the editor:
```
pragma solidity 0.8.18;
contract MyToken {
    // public variables here
    string public tokenName = "FEUTECH";
    string public tokenAbbreviation = "FIT";
    uint public totalSupply = 0;

    // mapping variable here
    mapping(address => uint) public balances;

    // mint function
    function mint(address _address, uint _value) public {
        totalSupply += _value;
        balances[_address] += _value; 
    }

    // burn function
    function burn(address _address, uint _value) public {
        if (balances[_address] >= _value){
            totalSupply -= _value;
            balances[_address] -= _value; 
        }
    }
}
```

To compile the code, click on the "Solidity Compiler" tab in the left-hand sidebar. Make sure the "Compiler" option is set to "0.8.18", and then click on the "Compile" button.

Once the code is compiled, you can deploy the contract by clicking on the "Deploy & Run Transactions" tab in the left-hand sidebar. Select the "MyToken" contract from the dropdown menu, and then click on the "Deploy" button.

Once the contract is deployed, you can interact with it by calling the burn, mint, and other functions in the contract. Additionally, if an address is needed for testing purposes; you can head over to the account "Deploy & Run Transactions" tab and use any of the account addresses in the accounts drop down. To use the burn and mint functions, you can head over and click the dropdown on the "mint" or "burn" section of the deployed transactions; Enter an address and a value, and finally click transact.

### Authors
TWENTY-2020



//SPDX-License-Identifier:MIT
pragma solidity 0.8.26;

    contract MyToken{
        
        // public variables here
        string public tokenName = "SILVER";
        string public tokenAbbry = "SLA";
        uint public totalSupply = 0;
    
        
        // mapping variables here
        mapping(address => uint) public balances;
        
        // mint function 
        function mintMyTokens(address _address1, uint _value) public{
            totalSupply += _value;
            balances [_address1] += _value;
        }
        // burn function
        function burnMyToken(address _address1, uint _value)public{
            if (balances[_address1] >= _value){
                totalSupply -= _value;
                balances[_address1] -= _value;
            }
        }
   
   
    } 

    
        
    

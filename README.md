# LERC20

This package allows to simply import, use and add extra functionality to LERC20 tokens. 

You can read more about [LERC20 tokens here](https://lossless-cash.gitbook.io/lossless/technical-reference/lerc20).


## Usage
  
```solidity
// SPDX-License-Identifier: MIT
pragma  solidity  ^0.8.0;

import  "@losslesscash/lerc20/contracts/LERC20.sol";

contract ScoobyToken is LERC20 {
	constructor() LERC20(
		100  *  10**18,  // total supply
		"Scooby",  // name
		"SCB",  // symbol
		0x192E176367C3Ae93f94643a53BC73345073df503,  // admin account address
		0x192E176367C3Ae93f94643a53BC73345073df503,  // recovery admin account address
		86400,  // timelock period
		0x27fce20D62f1DE73B0Ae1Dc7572F881061692de9  // lossless controller address (ropsten)
	)  {}
}

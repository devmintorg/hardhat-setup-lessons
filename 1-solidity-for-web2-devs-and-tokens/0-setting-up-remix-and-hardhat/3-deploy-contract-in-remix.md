# Deploy a Contract in Remix
*Please create the following contract in Remix. Spend no more than 15 minutes on this activity before review the answer. This section will not be graded, however you are encouraged to add the file to your GitHub for code review and feedback.*

In this exercise, we are going to deploy a custom contract using the Remix IDE. The starting contract code will be as follows:

```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;

/**
 * @title Storage
 * @dev Store & retrieve value in a variable
 */
contract Storage {

    uint256 number;
    address sender

    /**
     * @dev Store value in variable
     * @param num value to store
     */
    function store(uint256 num) public {
        number = num;
        
    }

    /**
     * @dev Return value 
     * @return value of 'number'
     */
    function retrieve() public returns (uint256){
        return number;
    }

    /**
     * @dev Return value 
     * @return value of 'sender'
     */
    function retrieve() public returns (uint256){
        return sender;
    }
}
```

There are some errors in this code that need to be fixed. We will use Remix to review the code and get it into a compilable state. Please do the following steps:

- Create a new file called 'UpdatedStorage.sol'
- Fix the bugs in the code so that is runs and deploys as expected
- Compile the code using Solidity version 0.8.4
- Deploy the code using the 'JavaScript VM (London)' environment
- Store a number with a different account than you deployed with
- View that number in the browser

Please do this exercise and then watch the video below for the full explanation.

<details>
<summary>Walkthough Video (Click to See)</summary>

VIDEO: https://www.loom.com/embed/806d0f28053f45cea8101f0054ffc283

</details>



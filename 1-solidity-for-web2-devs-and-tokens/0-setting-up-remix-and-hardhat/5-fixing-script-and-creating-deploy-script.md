# Fixing Script and Creating Deploy Script
*In this lesson, please send about 15 minutes going through the full activity to find all the commands you need. The [Hardhat Tutorial Document](https://hardhat.org/tutorial/) will be useful in finishing this lesson. Please add all of your changes to your files and then push to your GitHub repository*

In this lesson, we are going to compile the same script as we did in Remix but with our local instance of Hardhat. However, unlike Remix, where you can easily deploy a script with a single button click, Hardhat requires a few extra steps for deployment.

## Steps to Fix Update the Script and Deploy Locally
- Apply the fixes by going through the IDE interface and making the changes until the script is compiled
- Create a new script in the `scripts` folder called `DeployUpdatedStorage.js`
- Create a script that does the following:
    - Connects to our compiled instance of 'UpdatedStorage'
    - Deploys storage to the local network
    - Logs the address of the contract
    - Logs the Current Value of 'UpdatedStorage'
- Run this script using `npx hardhat run ./scripts/DeployUpdatedStorage.js`

Please complete this and then watch the walkthrough below.

#### FIVE MINUTE CONCEPTS
In this lesson, we are not providing the commands for you to be able to run the different hardhat functions. Instead, I'd like you to search the [hardhat documentation](https://hardhat.org/) and find the commands for the following:
- Compiling a Script on the command line
- Running a Script on the command line
- Create a Factory Instance in a Hardhat JS file
- Deploy an Instance of a document in a Hardhat JS file

If you have questions, feel free to ask your classmates for support!

Once you complete this section, go through the walkthrough to review the answer.

<details>
    <summary>Walkthrough of Fixing Script and Setting Up Local Deployment (Click to See)</summary>
    VIDEO: https://www.loom.com/embed/d1d6a9b19d5048a7a87505496afbc7d8
</details>
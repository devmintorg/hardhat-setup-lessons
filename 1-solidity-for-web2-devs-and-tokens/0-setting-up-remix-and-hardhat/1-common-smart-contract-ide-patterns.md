# Common Smart Contract IDE Patterns
To begin, we're going to be discussing the common patterns you're going to be seeing in most of the IDEs and Smart Contract Frameworks you will use.

We will go over some of the most common patterns and talk about how they are similar to past frameworks you've used.

## Extensions and Helper Libraries
Most frameworks that are supported by the community will often have common libraries and IDE extensions that make it easy to develop. For example, as I'm developing this lesson as a Markdown file, I have three extensions in VSCode that I am using to make it easy to develop:

- Markdown All in One
- Code Spell Checker
- Solidity (for code samples)

![My Extensions](https://dev-mint-curriculum-images.s3.amazonaws.com/schuster_extensions_example.png)

The Web3 space works exactly the same. There are a number of extensions and libraries that are useful for development purposes. These include:

- Yarn/NPM for installing local libraries
- Solidity and Javascript Language Libraries
- Linters
- Testing Libraries

Depending on the IDE, you may need to do more setup and installs, but all of them will have a robust framework to utilize.

#### ONE MINUTE CONCEPT QUESTIONS
*Please answer the following questions. This activity will not be submitted for grading.*

- When you have used an IDE that you that has made you more productive, what made it the most useful? 
- What did those tools use that other did not?
- Do you see any common patterns here from your past development experience? 
- Are there any patterns or tools that are missing?

## Folder Structure and Setup
All frameworks in the smart contract world will have a standard'way of setting up their files. The structure looks as follows:

- `contracts` will hold your contract files, ending in the `.sol` extension
- `scripts` will hold your deployment and automation files, ending in the `.js` or `.ts` extension
- `tests` will hold the testing files for your script, ending the in the `.js` or `.ts` extension
- `README.*` will have all of the information about the library
- `node_modules` or `.deps` will hold any outside libraries and files downloaded from NPM

When you create a new workspace in Remix, you automatically get this structure created for you:

![Remix Default](https://dev-mint-curriculum-images.s3.amazonaws.com/chrome_remix_example.png)

And by creating a sample advanced project in hardhat, it creates the following structure:

![Hardhat Advanced Example](https://dev-mint-curriculum-images.s3.amazonaws.com/Code_hardhat_advanced_project.png)

## Error Checking and Compiling
Most environments you deal with will have a way to check for errors in your script, both within the IDE as well as during compile time. Solidity is a compiled language, which means that before it is deployed, it needs to be compiled to run on the EVM. But even before this, the IDE can often catch errors that will fail when compiled.

The Remix IDE will show this error when removing a semi-colon from the script:

![Remix Error](https://dev-mint-curriculum-images.s3.amazonaws.com/chrome_remix_error.png)

And will show an error before allowing you to compile:

![Remix Compile Error](https://dev-mint-curriculum-images.s3.amazonaws.com/chrome_remix_compile_time_error.png)

Once compiled, the EVM compiled code will be held in a folder called `artifacts`.

## Deploying Your Code
Finally, all good Smart Contract environment will have a way for you to be able to deploy your code to multiple different environments. If you're dealing with a simple deployment, your environment might give you an option to deploy directly, much like Remix does here:

![Remix Simple Deploy](https://dev-mint-curriculum-images.s3.amazonaws.com/remix_simple_deploy.png)

Other environments might require you to create a file (stored in `scripts`) specifically to handle the deployment:

![Hardhat Simple Deploy](https://dev-mint-curriculum-images.s3.amazonaws.com/HH_simple_deploy.png)

You also have multiple options to be able to deploy your code. You can broadly think of them as:

- Local Test Networks
- 'Live' Test Networks
- Mainnet Networks

Most environments will have a way for you to be able to deploy to these environments. For example, remix allows you to chose where you deploy to:

![Remix Env Deploy](https://dev-mint-curriculum-images.s3.amazonaws.com/remix_environment_deploy.png)

Hardhat will require you to specify in the `hardhat.config.js` file which environments you can deploy to:

![HH Env Deploy](https://dev-mint-curriculum-images.s3.amazonaws.com/hh_configjs_deploy.png)

Which is then accessed by running the following command line:

`npx hardhat run scripts/deploy.js --network <network_name>`

Where Network name is the network defined in the the `networks` object.

What's nice is that most environments (including Hardhat and Remix) will have wallets that are already setup for testing purposes. So instead of having to fund your own wallets, you can just use what the environment already has.

#### ONE MINUTE CONCEPT QUESTION
*Please answer the following questions. This section will not be submitted for grading.*

- In Remix, what is the difference between the different listed environments? Which ones are designed for local networks and which ones are designed for live networks?
- Is there a functional different between deploying between a live production network and a live test network?

<details>
<summary>Answers (Click)</summary>

- In Remix, you will generally have the following environments available to you:
  - Javascript VM - Virtual environment that only exists in the browser. Upon refresh, the environment clears, with no contracts available. Good for local, ephemeral testing
  - Injected Web3 - Allows you to user your Metamask Wallet and connect to any network your wallet has access to. Is able to deploy to production.
  - Web3 Provider - Will connect to your local geth node, which can be configured however you need
  - Hardhat - Connects to your hardhat provider
  - Ganache - Connects to your ganache provider
  - Wallet Connect - Will connect to various Infura Wallets


- From a deployment perspective, there is no different between live testnet and live production networks: they are both external and function very similarly to each other from an execution perspective.

</details>

## Conclusion
While there are other similarities that we can dive into, these are the big ones that are common among most tools. We are now going to dive into the differences between these environments in the next lesson.
# Remix vs Hardhat: When To Use One Vs Another
As a smart contract developer, it's best for you to learn not one but two environments because you will use both, not just for this course, but for testing and development in your various roles in the Web3 industry. We will go over the reasons for this during this lecture.

## Using Remix
Remix has become something of a standard in the Ethereum community, and with good reason. It's a highly functional, browser based IDE to develope smart contracts. It is located at `remix.ethereum.org` and, as such, is actively supported by the Ethereum Community. Let's dive into why someone might utilize Remix.

### Benefits of Using Remix
**Ease of Setup**
You can get started using remix by going to https://remix.ethereum.org. By default, you will be taken to a workspace that is already setup to allow for standard smart contract development.

The tool has a plug-in manager, compiler, deployer (with pre-defined environment options) already built into the workspace. The tool, by default, support solidity development and already has OpenZeppelin (a common contract library we will use frequently) installed in it's dependencies. You also have a terminal window allowing you to run javascript commands.

With very minimal setup, you can create a contract and deploy it quickly.

![Schuster Workspaces](https://dev-mint-curriculum-images.s3.amazonaws.com/schuster_workspaces.png)



**Ease of Deployment and Manual Testing**
In addition, Remix also makes it very easy to be able to deploy and run scripts on both a local test network and a 'live' network. Unlike many IDEs which allow you to deploy but make it more difficult to quickly test, Remix comes built in with a Contract ABI interface, allowing you to deploy a contract and then immediately interact with it without creating any code.

![Remix Deploy Interface](https://dev-mint-curriculum-images.s3.amazonaws.com/remix_deploy_%20interface.png)

If you want to run a script to do something more complicated, you also have that option.

VIDEO: https://www.loom.com/embed/8dc32bc3f8b34a06ac921f4a7b7beb34

**Available Anywhere**
Unlike local IDEs which require you to have a local environment to be able to test, Remix is available to anyone with a browser. This means that if you're looking to develop on the road or don't have access to an appropriate computer, then Remix is an option to be able to do development.

### Downsides of Remix
**Minimal Github and Version Control Options**
Remix does not have an easy way to integrate with github, which means that if you wanted to save your on Github or use version control on your code, you don't have many great options.

This means that any code that you have here either needs to be save locally or uploaded publicly. Neither option is very attractive for long-term development.

**Lack of Portability**
While Remix is a great environment, it can only be used in a browser. If I wanted to move computers and then deploy my code locally, I'd need to go through the process of setting up something locally to be able to run my contracts code. 

And if you know you're going to use your code on a local system in the future, the time to move your code might as well be spent in setting up your local environment.

**Lack of Flexibility**
Remix does have a lot of great features built in, but once you get into more serious development, you'll realize that Remix is not as flexible as you might think. For example, if you wanted to connect to a particular test network and 'pin' to a particular block, you would have to configure quite a bit in both remix *and* your local environment to make that work.

Much of the flexibility that Remix offers comes not from Remix itself, but from the connected wallets and resources. In this case, remix does not offer much to make a highly customized experience.

## Using Hardhat
Hardhat is quickly becoming the industry standard for deploying smart contracts, and for good reason. The flexibility it offers to developers to be able to automate and test their environments is unlike anything else that has existed in the market before. We're now going to go into the pros and cons of using this for development purposes.

### Benefits of Hardhat
**Highly Customizable**
Hardhat is, at it's core, a simple javascript framework with a lot of additional functionality for interacting with smart contracts. Because of this, the tooling created by hardhat allows for almost any use case you need to be able to handle smart contracting development.

There are many plugins that allow you to connect to other [common Smart Contract tools](https://hardhat.org/getting-started/), and many configuration changes you can make to [support your exact use case](https://hardhat.org/config/).

**Highly Portable Code**
Because Hardhat is just a framework, you can use it in conjunction with other tools. This means that anything you created in Hardhat can be paired with any other command line tools, such as git. Because of this, you can use common version control practices and libraries to support your development. 

This means that your testing can go beyond what you do locally, allowing you to benefit from github's robust CI/CD and Pull Request capabilities. This is one of the biggest things that's missing from Remix and is a huge benefit of using Hardhat.

**Great Development Workflow**
While Remix technically offers scripting and testing, using that as a normal part of your workflow has always felt a bit awkward. However, Hardhat makes it easy to make testing part of your workflow. By easily integrating `Chai` into their framework, you can define what tests you need to run and have them run every time.

In addition, running scripts and deployments are just as easy, allowing you to use the same scripts for multiple networks with a single change in the command line.

VIDEO: https://www.loom.com/embed/23da1e4dd7674de581ca88b0dd3f8402

**Easy Automation**
Hardhat scripts are very easy to use, as the `hre` library makes it very easy to interact with common smart contract elements and call them from the command line. But hardhat goes one step further and offers tasks. [Tasks allow you to create your own hardhat arguments](https://hardhat.org/guides/create-task.html), allowing you to further extend the usability for hardhat in your automation.

For example, if you need a process that checks for the balance of an address and sends a notification when it's below a certain level, you can create a new task to do exactly that.

### Downsides of Hardhat
**Longer Setup**
Like any new framework, if you don't already have it setup, it's difficult to be able to get the environment working as expected. Because of this, some people will resist using a 'full' framework like hardhat until they're ready to develop a production piece of code, and never go through the setup.

We will be helping you get setup in hardhat during this course, but here is a video of me (who already knows how to setup hardhat) setting up a new project.

VIDEO: https://www.loom.com/embed/71ba790cdda24d4595a1830ee5de526c

**More Complex Toolset**
Hardhat is certainly a more complex tool, which means that if you're trying to work with someone who doesn't understand smart contracts or what Hardhat does, it's going to be more complicated than Remix.

Because of that, if you're working with less technical team members, you may need to do a bit of translation to make your project more accessible.

**Requires Scripting for Deployment**
The one downside of deploying with hardhat locally is that if you want to interact with the contract, you have to write a script to interact with it. Unlike Remix, which creates an easy ABI Interface to the contract upon deployment, any hardhat user is going to have to create a connection to their local contract and then write those instructions in the script. While there is some great boilerplate code to deploy the code, it does require some configuration.

## When to Use Which Environment
Over the course of your Web3 career, you will be utilizing both environments in your developments. Depending on your preferences or use case, either can be a fine choice. However, here are a few recommendations to help guide you:

### When Needing To Share Code, Use Hardhat
If you're in a position where you need to share your code with your team, or want to showcase a personal project you're working on, use Hardhat. Hardhat's ability to be saved into Github makes the an obvious choice.

### When Needing To Quickly Test A Contract, Use Remix
If you're playing around with a new code or just want to see how a contract works on a testnet, Remix is the easiest solution. By quickly deploying and then interacting with a contract, you're able to easily test out some feature and get it onto the appropriate network without much hassle.

### When Needing to Develop A Large Solution, Use Hardhat
Hardhat is almost always going to be the better solution for long-term development. It's automation tools and scripting framework makes it easy to develop solid contracts from the ground up without cutting corners. Remix has this ability, but it's just not as easy.

## Conclusion
In the next few lessons, we're going to dive into using both Remix and Hardhat in order to setup our environment. We will be using both extensively during this course, so please become comfortable with both sets of tools!
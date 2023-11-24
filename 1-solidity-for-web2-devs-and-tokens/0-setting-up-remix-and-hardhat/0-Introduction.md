# Introduction - Starting Off With The Right Environments

VIDEO: https://www.loom.com/embed/20d988fa72164b949241da9e772c3698

Imagine you're taking an online course and being instructed to create a website. Even better, the course provides a browser, which offers to make things super easy to develop. After some time, you're able to make the solution work and get things work.

But now, you want to do something more, you want to:

- Change the UI around to add a new element
- Add a library you saw that looks interesting
- Save the code and share it with a co-worker
- You want to save the code elsewhere and have it run like you did on your browser

However, the program only allows you to work within their IDE. Worse, they didn't teach you how to set it up yourself. The code is only useful if you use their tool! 

If you want to make the code yours, you have to create a brand new environment, setting it up from scratch. And if you're not familiar with the environment, you may be setting things up sub-optimally and causing yourself unnecessary headaches.

This is a situation I dealt with many times in my career. The one lesson I took away is that even though I was able to get work done in the short-term, I was only able to make real progress when I setup the environment myself. So, I learned very quickly that taking the time to setup the right environment was the key to long-term technical success. And so, we will start this section with that.

## Creating a Scalable Working Environment
In your pre-work, you may have used Remix, a popular online solidity IDE, to test your code. While this will be an important tool we use for this course, it has a number of major drawbacks that makes it less scalable for professional development:

- It's hard to reproduce from system to system
- You can lose your work
- The IDE isn't always consistent

Because of this, production teams do not develop full solutions in Remix, instead opting for a solution like Hardhat for development.

In this section, we're electing to start with an overview of how to setup your development environment, both in Remix and in Hardhat. In addition, we'll go over when it's appropriate to use one environment vs another and to explain what sort of tools you should expect to use.

The benefit of learning about both environments (especially hardhat) is that you'll get a chance to start setting up your environments correctly and getting to immediately use them to work on your support projects. Web3 teams will be much more impressed seeing a github repository built with hardhat rather than a random .sol published from Remix. You'll also have a much better footing to be able to go after more challenging projects and being able to show your work in Github.

## Section Objectives
By the end of this section, you should be able to:
- Be able to distinguish the right circumstance to use Remix vs Hardhat
- Setup a Remix Environment and Deploy to the Local Testnet
- Setup a Hardhat Environment and Deploy a Script to the Local Environment
- Setup a Hardhat Node and Run Commands via Hardhat Console
- Push your project to Github for review

See you in the next lesson!


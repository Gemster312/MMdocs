# First Time Setup

### Overview
Video game development in Unreal Engine is comprised of two components: The game development via Unreal Engine, and the C++ coding via Visual Studio. You'll be able to achieve a lot through the Unreal Engine (especially with the help of Blueprints), however much of the game logic is in C++. Generally speaking, C++ is more optimized than Blueprints, so the goal is to use C++ over Blueprints on any computation-heavy logic (e.g. pathfinding).

### Required Tools:
* [Unreal Engine 4.22.3](InstallingUnrealEngine.md)
* [Visual Studio 2017](InstallingVisualStudio.md) (Community is sufficient)

*Note: **Do not** use versions that aren't listed above for development. It can result in incompatability issues.*

### Recommended Tools:
* [Git Bash](https://git-scm.com/downloads) (For command-line)
* [GitHub Desktop](https://desktop.github.com/download/) (For GUI and clear diff comparisons)

*If you are already comfortable using other Git-related systems, feel free to use whatever you are comfortable with.*

### New To Unreal Engine?
If this is your first time using Unreal Engine, I recommend you give [Katie's tutorial series](https://www.youtube.com/watch?v=iTwxuahe5B4&list=PLHSMxXn4v-aGhuRxxSBVPqykMjDiRyGrJ&index=2&ab_channel=MakeGamesWithKatie) a watch. It gives a solid overview of the basics of Unreal Engine and introduces you to Blueprints.

### Git'ing Ready
Once you've got all of your development tools, it's time to get your Git repo ready. Klavvy will remain in charge of the master repository. As a developer, you will be forking the master repository and when you have a feature ready you will make a **Pull Request** for Klavvy.

If you are familiar with Git, feel free to skip this section.

First, log into your [GitHub](https://github.com/) account and then open up the [Manic Miners Development]() repository. Fork the repository to your own Git account (**ensure it is PRIVATE!!**).

Once you have the repository forked, you can clone it to your local device. Using **Git Bash**, navigate to where you want this project (e.g. `~Documents/GitHub/ManicMinersDevelopment`). Clone your repository (*not Klavvy's repository*).

Example: 
``` 
git clone https://github.com/Example/MMDev.git
```

Once cloned, you can start setting up development branches and start working! If you need some more guidance on using Git, please refer to the [Git Process](GitProcess.md) doc.

### How Can I Help?
There's no shortage of work to be done, so pick an area that you want to help in and get those hands dirty! Start by picking a task from the [Issues]() page and assigning it to yourself (or make a new issue if you think something is missing).
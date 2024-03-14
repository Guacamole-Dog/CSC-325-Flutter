## DevContainer Environment

A DevContainer is an essential component in any development environment beyond one machine because **it acts as a consistent development environment shared between multiple machines.** This is beneficial because in group software development, every person's machine is different, and therefore, some issues might appear during testing/development on for one person but not for anyone else. Being able to cut this headache out of the equation is extremely valuable, and that's exactly what DevContainers do.

### The steps I took to configure my DevContainer
1) _**I inserted a base image into devcontainer.json.**_ In this project's case, it was a Docker image for Flutter, which lets the container always have access to Flutter whenever it is opened.
2) **I downloaded Docker Desktop, the Dev Containers extension for VS Code, and the Docker extension for VS Code so that the DevContainer can run.**
3) **In the devcontainer.json, I put some post-creation commands for the container under a "postCreateCommand" section, and I added some configurations to enable Dart and bash access within the DevContainer.**

VS Code's DevContainer integration allows a user to easily create a premade configuration file for a DevContainer, add certain configurations (such as the Flutter Docker image) and run it through VS Code, as long as they have Docker Desktop. 
This integration is accessed by downloading the Docker and Dev Containers extension on VS Code.

### The steps to use the DevContainer
1) Before starting the container, make sure you have **Docker Desktop, the Docker extension for VS Code, and the Dev Containers extension for VS Code** all installed.
2) Click on the small blue square at the bottom left of your VS Code window and then click **Reopen in Container**. A new window should open and the DevContainer should start being built.
3) **Once in the DevContainer, editing code is the same as when not in a DevContainer.** To run the Flutter application, simply navigate to **Flutter/lib/main.dart** and then run it using VS Code.
4) **When using Git, everything still functions as normal**, and you can just push your changed files to your branch of choice.

#### Challenges and Conclusion
The main challenge I had was getting the necessary dependencies to properly run the development environment and getting a way for the user to not be considered 'root' while operating the DevContainer. I resolved them by finding the right Dockerfile image and then adding post-create commands and configurations to the devcontainer.json file.

**In conclusion, DevContainers are a valuable tool in software development due to standardizing the development environments of every developer in a group and therefore eliminating any chance of errors stemming from a developer's environment alone, saving a lot of time in the process.** Through implementing them here, I have learned that, thanks to the integration in VS Code, the setup of a DevContainer is more simple than I expected, which means that **any developer worth their salt does not have an excuse to not utilize one.**


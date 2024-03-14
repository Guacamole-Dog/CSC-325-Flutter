## DevContainer Environment

A DevContainer is an essential component in any development environment beyond one machine because it acts as a consistent development environment shared between multiple machines. This is beneficial because in group software development, every person's machine is different, and therefore, some issues might appear during testing/development on for one person but not for anyone else. Being able to cut this headache out of the equation is extremely valuable, and that's exactly what DevContainers do.

Here are the steps I took to configure my DevContainer:
1) I inserted a base image into devcontainer.json. In this project's case, it was a Docker image for Flutter, which lets the container always have access to Flutter whenever it is opened.
2) I downloaded Docker Desktop and the Docker extension for VS Code so that the DevContainer can run.
3) In the devcontainer.json, I put some post-creation commands for the container under a "postCreateCommand" section.
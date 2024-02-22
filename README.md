# CSC-325-Flutter
This contains my Flutter project, as well as a development container with all of the necessities and dependencies needed.

# Instructions
To run the Flutter project in its development environment, follow the below instructions.

1) Copy the devcontainer file into the root your project file
2) Open your project file in VSCode
3) Press F1 and select Dev Containers: Reopen in Container
4) Paste the following lines of code into the terminal:

curl -C - --output android-sdk-tools.zip https://dl.google.com/android/repository/commandlinetools-linux-8512546_latest.zip 

mkdir androidsdktools
unzip android-sdk-tools.zip -d androidsdktools
rm android-sdk-tools.zip

curl -C - --output flutter.tar.xz https://storage.googleapis.com/flutter_infra_release/releases/stable/linux/flutter_linux_3.19.1-stable.tar.xz
mkdir flutter
tar -xf flutter.tar.xz -C flutter
rm flutter.tar.xz

Once this is done, the container is ready to develop Flutter applications and run my Flutter project.

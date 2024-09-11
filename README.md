System Requirements:
CPU: 11th Gen Intel(R) Core(TM) i7-1165G7 @ 2.80GHz   2.80 GHz
RAM: 16.0 GB
OS: Windows 11

Installation instructions:
The first step is to set up an environment that will allow react native development. This means installing all the dependencies, which are as follows:
	Node
	Java SE Development (JDK)
	Android Development environment
For installing Node and JDK, it is recommended to use Chocolatey as your package manager.
For the Node installation run the following command:
	Choco install nodejs-lts
And run this command for the JDK
	Choco install Microsoft-openJDK17
To setup your Android development environment you will install Android studio, during installation ensure you have checked Android Virtual Device. Once installed open Android studio and open the SDK manager.
Under SDK Platforms, install Android 14.0 (“UpsideDownCake”) API level 34
Under SDK Tools, under Android SDK Build-tools 35, install 34.0.0
Inside Android studio, Create a Virtual Device with the UpsideDownCake release Name and the 34 API

Configuration steps:
After installing, open the control panel, under user account and user account again. Go to Change my environment variable and create a new variable. Name your variable ANDROID_HOME and point it to your android SDK folder, which is located in Appdata\Local\Android

Project Creation:
Start your Virtual Android Device
Navigate to the folder you would like to create your project in and run the following command
npx @react-native-community/cli@latest init [project name]
install all the required packages
Running the project:
navigate to your new folder and run the following command
npx react-native run-android
a new command prompt will open to run the metro server, when prompted enter “a” to run android

Troubleshooting:
If your environment hasn’t been configured correctly, the metro server will fail. To fix this, you can run the following command
Npx react-native doctor
This command will let you know which parts of your configuration are incorrect and have links to help troubleshoot
On first build my build failed but after running it a second time all issues were fixed

Resources:
These are the documentations I followed to properly create my android development environment
https://reactnative.dev/docs/set-up-your-environment
https://reactnative.dev/docs/getting-started-without-a-framework


# IBM MobileFirst Platform 8 w/Ionic 2


## Tools that will be required

The tools to install include:

- Install Java
- Install NodeJS
- Install Cordova
- Install Ionic Command-Line-Utility
- Install Gulp
- Install cdvLive
- Install Maven
- Create Bluemix Account
- Install MobileFirst 8.0 beta Command Line Utility
- Install MobileFirst 8.0 beta Development Kit
- Install Android Studio
- Install XCode (Mac only)

### Install Java
You will need one of the following installed:
- Oracle JVM 1.7u55+
- Oracle JVM 1.8u20+
- IcedTea OpenJDK 1.7.0.55+

To Install Oracle Java on a Mac or Windows Machine visit http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html. The current version as of the April 11, 2016 is 8u77.

Download from the section that reads: Java SE Development Kit 8u77. Accept the License Agreement to enable the selection and download of the appropriate installation.

To install IcedTea OpenJDK on a Debian, Ubuntu, Fedora, Oracle Linux or Red Hat Linux machine visit http://openjdk.java.net/install/index.html and follow the instructions to download and install.

### Install NodeJS
There are two current stable builds of NodeJS as of 4/11/2016. Download and install version 4.4.2 or the Stable LTS version. We do not recommend installing 5.10.1

Visit `https://nodejs.org/en/download/` and download the version that matches your operating system. 

#### Confirm installation
After the install you will want to confirm that the installation was successful. **On Mac or Linux** open a terminal or **On Windows** open a command prompt and type `node -v`.

### Install Cordova
Once node is installed you can use npm to install Cordova. The current version as of 4/11/2016 is 6.1.1

1. To determine your version of Cordova if you have one previously installed open a command prompt (Windows) or terminal (Mac/Linux) and type `cordova -v`.

1. To install Cordova if it is not currently installed or is a later version:

	**On Mac or Linux** open a terminal and type:

	`sudo npm install -g cordova`

	**On Windows** open a command prompt and type:

	`npm install -g cordova`

1. Confirm the correct version by typing `cordova -v`


### Install Ionic Command-Line-Utility
You will need the Ionic Command-Line-Utility to complete the labs. To install the Ionic Command-Line-Utility you will again use npm. As of 4/11/2016 the current version of Ionic is 1.7.14

1. To install Ionic if it is not currently installed or is a later version:

	**On Mac or Linux** open a terminal and type:

	`sudo npm install -g ionic@beta gulp cdvlive`

	**On Windows** open a command prompt and type:

	`npm install -g ionic@beta gulp cdvlive`

1. Confirm the correct version by typing `ionic -v`

> **Note:** If you have a previous install of Ionic, you may need to remove that version before installing the beta version.

### Install Gulp (Optional)
Gulp should have been installed with the Ionic framework in the previous step. If it was, you can skip this step.

Gulp will be used to provide real-time application builds. For more information on Glup please visit [http://gulpjs.com](http://gulpjs.com) or [Installation instructions](https://github.com/gulpjs/gulp/blob/master/docs/getting-started.md)

1. To install glup

	**On Mac or Linux** open a terminal and type:

	`sudo npm install -g gulp`

	**On Windows** open a command prompt and type:

	`npm install -g gulp`


### Install cdvlive
cdvlive should have been installed with the Ionic framework in a previous step. If it was, you can skip this step.

cdvlive provides a live reload of your application after it has been built. For more information on cdvLive please visit the [cdvlive npm site](https://www.npmjs.com/package/cdvlive)

1. To install cdvlive

	**On Mac or Linux** open a terminal and type:

	`sudo npm install -g cdvlive cordova`

	**On Windows** open a command prompt and type:

	`npm install -g cdvlive cordova`

### Install Maven
The current version of Maven as of 4/11/2016 is 3.3.9. For more information on installing Maven, please visit https://maven.apache.org/install.html

1. Download the Maven binary `apache-maven-3.3.9-bin.tar.gz` or `apache-maven-3.3.9-bin.zip` from https://maven.apache.org/download.cgi

1. Unpack the tar or zip file.

#### For Mac
1. Move the contents of the upacked directory. Open a terminal and type:

	`mv /Users/[myuser]/Downloads/apach-maven* /opt/`
	
	Replacing the `[myuser]` with your computer user name.

1. Edit your .profile to add the location of maven to your path. Open a terminal and type:

	`pico $HOME/.profile`
	
1. Enter the following on a new line or update your existing path statement:
	`export PATH=$PATH:/opt/apache-maven-3.3.9/bin`
	
1.	Ctrl-O to write the file

1.	Ctrl-X to exit pico editor

1.	Make the path available. Type

	`source $HOME/.profile`
	
	This will run the profile and make the new path available.
	
1. Verify the installtion. Type

	`mvn -v`
	
	This should return something like
	
	```
	Apache Maven 3.3.9 (bb52d8502b132ec0a5a3f4c09453c07478323dc5; 2015-11-10T08:41:47-08:00)
Maven home: /opt/apache-maven-3.3.9
Java version: 1.8.0_60, vendor: Oracle Corporation
Java home: /Library/Java/JavaVirtualMachines/jdk1.8.0_60.jdk/Contents/Home/jre
Default locale: en_US, platform encoding: UTF-8
OS name: "mac os x", version: "10.11.4", arch: "x86_64", family: "mac"
```

#### For Windows
1. Instead of re-writing the example of how to install Maven on Windows, follow this tutorial: http://www.mkyong.com/maven/how-to-install-maven-in-windows/

> **Note:** Since you have already installed Java, you can skip that portion of the tutorial on mkyong.com.

### Create a Bluemix Account
Please ensure that you have created a Bluemix account and that you can log into it. If you have not created a Bluemix account please do so using your IBM id at https://console.ng.bluemix.net/registration/

A Bluemix account is required to complete the installation instructions as well as the labs.

### Install MobileFirst 8.0 beta Command Line Utility

The development version of the MobileFirst Command Line Utility is now available as an npm install. This version can coexist with previous versions of the MobileFirst Command Line Utility.

To install the MobileFirst CLI Version 8.0 Beta, open a terminal or command prompt and type 

```npm install -g mfpdev-cli```

You can confirm the installation by typing

```mfpdev -v```

You should see something similar to

`8.0.0-201603280000`

### Install MobileFirst 8.0 beta Development Kit
IBM MobileFirst Platform Foundation v8.0 beta consists of the following components: MobileFirst Server & MobileFirst Operations Console, MobileFirst Command-line Interface (CLI), MobileFirst client SDKs and MobileFirst adapter tooling.

These components can be installed either seperately via online repositories which contain the latest releases, or downloaded bundled together through the MobileFirst Platform Foundation Development Kit Installer, for future or offline use.

> **Note:** That you installed the CLI (Command-Line-Interface) from npm in the previous step and so you will not need to re-install the MFP CLI.



## Steps
These labs are loosely based on a subset of the Hybrid Messenger lab found on the MobileFirst Developer Site. The Bybrid Messenger Lab can be found on the [MobileFirst Platform Foundation 8.0 Labs Site](https://mobilefirstplatform.ibmcloud.com/labs/developers/8.0/hybridmessenger/)


This lab will use IBM MobileFirst 8.0 Beta with Ionic 2 to create an employee directory mobile applicaiton that will be deployed on an Android simulator and iOS Simulator (if running on a Mac).

### Step 1: Create a Working Directory
Create a working directory on your computer. This working directory will contain both the mobile application source code as well as the adapter source code.

**On Mac or Linux** open a terminal and type:

`mkdir ~/EmpApp`

![Create Directory](images/create_directory.png)

**On Windows** open a command prompt and type:

`mkdir /EmpApp`

> **Note:** You can place this working directory wherever you would like, just make sure you remember where you put it for future reference.

### Step 2: Change Directory to the Working Directory

**On Mac or Linux** open a terminal and type:

`cd ~/EmpApp`

![Change Directory](images/change_directory.png)

**On Windows** open a command prompt and type:

`cd /EmpApp`

### Step 3: Create Ionic Base Application
Next you will create an Ionic application using the sidemenu template and specifiying the TypeScript option. For more information on TypeScript please visit the [TypeScript Home Page](https://www.typescriptlang.org)

**On Mac or Linux** open a terminal and type:
> **Note:** Make sure you are in the EmpApp directory

`ionic start 	employeeDirectory sidemenu --v2 --ts`

**On Windows** open a command prompt and type:
> **Note:** Make sure you are in the EmpApp directory

`ionic start 	employeeDirectory sidemenu --v2 --ts`

The `--v2` tells Ionic that we will be using version 2 of the Ionic framework.

The `--ts` tells Ionic that we will be using TypeScript instead of JavaScript.

For more information on the Ionic start command, please visit [Starting an Ionic App](http://ionicframework.com/docs/v2/cli/start/)



- 




# **COMP2042 Developing Maintainable Software**
## 1.0 My GitHub
Name: Ye Wenfeng
Student ID: 20496457
Repository Link: [GitHub Repository](https://github.com/QuantumMilktea1/CW2024)
## 2.0 Setup and Compilation Instructions
### 2.1 Prerequisites
Java Development Kit (JDK): Version 21 or higher
Apache Maven: Version 3.8.0 or higher
JavaFX SDK: Version 21.0.5
Git: Installed and configured
Recommended IDEs
IntelliJ IDEA: Version 2023.3 or higher
Eclipse: Version 2023-12 or higher
VS Code: With Java Extension Pack and JavaFX Extension installed
Environment Setup
1. Install Java Development Kit (JDK)
Download JDK 21 from Oracle or OpenJDK.
Set up the JAVA_HOME environment variable:
Windows:
[Environment]::SetEnvironmentVariable("JAVA_HOME", "C:\Program Files\Java\jdk-21", "Machine")
[Environment]::SetEnvironmentVariable("Path", $env:Path + ";%JAVA_HOME%\bin", "Machine")
Unix/MacOS:
echo 'export JAVA_HOME=/Library/Java/JavaVirtualMachines/jdk-21.jdk/Contents/Home' >> ~/.bash_profile
echo 'export PATH=$JAVA_HOME/bin:$PATH' >> ~/.bash_profile
source ~/.bash_profile
Verify installation:
java --version

2. Install JavaFX SDK
Download JavaFX SDK 21 from OpenJFX.
Extract it to a preferred location.
Optionally, add it to your PATH (although Maven will handle dependencies automatically):
Windows:
[Environment]::SetEnvironmentVariable("PATH_TO_FX", "C:\Path\To\javafx-sdk-21\lib", "Machine")
Unix/MacOS:
echo 'export PATH_TO_FX=/path/to/javafx-sdk-21/lib' >> ~/.bash_profile
source ~/.bash_profile
3. Install Git
Install Git for your operating system:

Windows: Download and install from Git for Windows.
macOS: Install via Homebrew:
brew install git
Linux (Ubuntu/Debian):
sudo apt-get install git
Linux (Fedora):
sudo dnf install git
Verify Git installation:

git --version

4. Install Apache Maven
Download Apache Maven from the Maven Official Site.
Add Maven to your system PATH:
Windows:
[Environment]::SetEnvironmentVariable("Path", $env:Path + ";C:\Path\To\Maven\bin", "Machine")
Unix/MacOS:
echo 'export PATH=/path/to/maven/bin:$PATH' >> ~/.bash_profile
source ~/.bash_profile
Verify Maven Installation
To confirm Maven is installed correctly, run the following command:
mvn --version

Project Setup Guide
Follow the steps below to set up and run the project on your local environment.

2.2 Project Setup
Clone the Repository
Clone the project repository:
git clone https://github.com/QISHEAN/CW2024.git
cd CW2024
IDE Setup
Eclipse
Open Eclipse and import the project as a Maven project:
Go to File → Import → Existing Maven Projects.
Select the project folder and click Finish.
Configure the Java Build Path if necessary:
Right-click the project in the Project Explorer → Properties → Java Build Path.
Add JavaFX libraries if they are missing:
Go to the Libraries tab.
Click Add External JARs... and select the JavaFX JAR files from your JavaFX SDK.
IntelliJ IDEA
Open IntelliJ IDEA and import the project as a Maven project:
Select Open from the IntelliJ start screen and choose the project folder.
IntelliJ will detect the pom.xml and set up the Maven configuration.
Verify the Project SDK:
Go to File → Project Structure → Project Settings → Project SDK.
Ensure the SDK is set to JDK 21.
Refresh Maven dependencies:
Open the Maven tool window (usually on the right-hand side).
Click Reload All Maven Projects to load all dependencies.
Wait for Maven to sync and ensure there are no errors in the dependencies.
VS Code
Install the required extensions from the Visual Studio Code Marketplace:
Java Extension Pack.
JavaFX Extension (optional for JavaFX development).
Open the project folder in VS Code:
Select File → Open Folder... and choose the project directory.
Use Maven commands in the integrated terminal to build and run the project:
For example:
mvn javafx:run
Alternatively, set up a launch configuration to run the project directly:
Go to the Run and Debug panel → Create a Launch Configuration → Configure it for Maven.
Compile and Run the Application
Compile the Project
Clean and compile the project using Maven:
mvn clean compile
Run the application:
mvn javafx:run
Package the application:
mvn package
Run the packaged JAR file:
java -jar target/CW2024-1.0-SNAPSHOT.jar
Common Build Commands
Use the following Maven commands to build, test, package, and run the project.

1. Clean Build Files

Removes all previously generated build files:
mvn clean
2. Compile the Project

Compiles the source code of the project:
mvn compile
3. Run Tests

Executes all test cases in the project:
mvn test
4. Package the Application

Packages the application into a JAR file:
mvn package
5. Install to Local Repository

Installs the application into the local Maven repository:
mvn install
6. Run the Application

Runs the application using the Maven JavaFX plugin:
mvn javafx:run

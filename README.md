## Installing java on macos (Using Homebrew)

- Check the current java version 
```bash
java -version
```
- Install homebrew if it is not installed
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```
- Install java using homebrew
```bash
brew install openjdk@11
```
- Verify the installation path of java
```bash
brew info openjdk@11
```
- Set the JAVA_HOME environment variable to point to the installed JDK
```bash
# Edit ~/.zshrc file
sudo nano ~/.zshrc

# Insert the following line and save the file
export JAVA_HOME=/opt/homebrew/opt/openjdk@11

# Apply the changes
source ~/.zshrc
```
- Verify that Java is installed and the JAVA_HOME variable is set correctly by running
```bash
java -version
javac -version
echo $JAVA_HOME
```
------------------------------------------
## Installing java on macOS (Using .dmg file installation)

- Download java from this link:
  https://www.oracle.com/sg/java/technologies/downloads/#jdk17-mac

- Install the dmg file

- After installation, check the installation path of java and make a note of the version
```bash
/usr/libexec/java_home -V
```

- Set the JAVA_HOME environment variable and adds the bin directory of the specified Java version to
  the beginning of the system PATH environment variable
```bash
# Edit ~/.zshrc file
sudo nano ~/.zshrc

# Add the following lines and save the file
export JAVA_HOME=$(/usr/libexec/java_home -v 17.0.10)
export PATH=$JAVA_HOME/bin:$PATH

# Apply the changes
source ~/.zshrc
```

- Verify that Java is installed and the JAVA_HOME variable is set correctly by running
```bash
java -version
javac -version
echo $JAVA_HOME
```

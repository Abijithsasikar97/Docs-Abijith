# ANDROID-SDK ==> LINUX


				1.Download tools and platform tools and create folder named (android-sdk) place those downloaded this inside that newly created folder.

tools(comandline-tool) ===> https://developer.android.com/studio/?gclid=Cj0KCQjwhb36BRCfARIsAKcXh6GHAqNAlsdWMeF-C0hYJQEXifpK9W4RstktDx9Hgl9FnQ2-e6kjKc8aAt1MEALw_wcB&gclsrc=aw.ds

Platform-tools ===> https://developer.android.com/studio/releases/platform-tools

				2. Path setup ==> open bashrc with command sudo nano ~/.bashrc set path by placing below one in that file and dont forget to reload bash with command source ~/.bashrc (NOTE: give your exact path dont just copy paste)

>export ANDROID_HOME=/home/abijith/android-sdk

>export PATH=/home/abijith/android-sdk/platform-tools:/home/abijith/android-sdk/tools:/home/abijith/android-sdk/tools/bin:${PATH}

# sdkmanager fix for java 9 and 10
#export JAVA_OPTS='-XX:+IgnoreUnrecognizedVMOptions --add-modules java.se.ee'

				3. after successfully settingup path run below commands
# Check adb version
>adb --version

# It must show the installed adb version
Android Debug Bridge version 1.0.41
Version 29.0.2-5738569
Installed as /home/abijith/android-sdk/platform-tools/adb

# Check sdkmanager version
>sdkmanager --version

# It must shown installed sdkmanager version
26.1.1

// List all the installed and available platforms, system images and other resources 
>sdkmanager --list

// Output should look like
Installed packages:=====================] 100% Computing updates...             
  Path           | Version | Description                       | Location       
  -------        | ------- | -------                           | -------        
  platform-tools | 29.0.2  | Android SDK Platform-Tools 29.0.2 | platform-tools/
  tools          | 26.1.1  | Android SDK Tools 26.1.1          | tools/

Available Packages:
...
...

# Start downloading the most recent package
>sdkmanager "platforms;android-29"

# install gradle
>sudo apt-get install gradle

				4. And if you getting this below error just do the thing which mentioned below that in terminal

ERROR ====> ANDROID_SDK_ROOT=undefined (recommended setting)

******EXECUTE THIS****
>export ANDROID_SDK_ROOT=$HOME/android-sdk

>export ANDROID_HOME=$HOME/android-sdk

>export PATH=$PATH:$ANDROID_SDK_ROOT/tools/bin

>export PATH=$PATH:$ANDROID_SDK_ROOT/platform-tools

>export PATH=$PATH:$ANDROID_SDK_ROOT/emulator

>export PATH=$PATH:$HOME/Documents/gradle-5.6.1/bin


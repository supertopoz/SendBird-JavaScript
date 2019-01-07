# Sample JavaScript React-Native Redux

SendBird React-Native sample using [SendBird SDK](https://github.com/smilefam/SendBird-SDK-JavaScript).

## IOS Environment Prerequisites

### Gobal

- [Node](https://nodejs.org/en/)
- [NPM](https://www.npmjs.com/)
- [Java SE Development Kit 8](https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

#### Android App

- [Android Studio](https://developer.android.com/studio/) (+Android SDK/Google API)
- Recomended - If it's your first time to create a React Native Application first set up a sample app from the [React Native docs](https://facebook.github.io/react-native/docs/getting-started.html)

#### IOS App

- [Cocoapods](https://cocoapods.org/)
- [XCode](https://developer.apple.com/xcode)
- [XCode Command Line Tools](https://facebook.github.io/react-native/docs/getting-started.html#xcode)


## IOS Setup


### Android app with Android Studio

#### 1. Install React Native CLI.

        npm install -g react-native-cli

#### 2. Open project
* Start Android Studio click "Open an existing Android Studio project" 
* Navigate to `SendBird-JavaScript/react-native-redux-sample/ReactNativeWithSendBird`
* Open the project

#### 3. Install dependencies
* Open the terminal in Android Studio(bottom left) 
* install the npm packages

        npm install
        

#### 4. Start emulated Android device
* Start a [new emulated device.](https://developer.android.com/studio/run/managing-avds) 
* Set the device up with Oreo 27 as per React Native's requirements
* This code was tested to work with a "Galaxy Nexus" device

####  5. Complete emulated Android device activation for development 
* Go to emulated device's "settings" and click "FINISH SETUP"
* Carefully complete the set up and don't forget to log in when prompted
* On the emulated device [start developer mode.](https://developer.android.com/studio/debug/dev-options) 

#### 6. Install and start SendBird Android SDK
* In Android Studio start the React Native compiler using the terminal

        react-native run-android
        

### ios app with xcode

#### 1. Install pod dependencies
* Open a terminal in `SendBird-JavaScript/react-native-redux-sample/ReactNativeWithSendBird/ios` and run the command:

        pod install
        
* If you don't have cocopods you can install it globally with ``sudo gem install -n /usr/local/bin cocoapods``

#### 2. Open project in Xcode
* Open Xcode and click open another project...
* Navigate to ``SendBird-JavaScript/react-native-redux-sample/ReactNativeWithSendBird/ios``
* Open the folder

#### 3. Make sure you xcode command line tools installed
* In Xcode "File" - "Preferences" - "Locations" - select the latest "Command Line Tools"

#### 4. Open iPhone emulator and install SendBird React-Native application
* Open a terminal
* Navigate to `SendBird-JavaScript/react-native-redux-sample/ReactNativeWithSendBird'
* Run 
        react-native run-ios
        
* Wait for the SendBird Application to start




# Connect your own SendBird Application

* By default this SendBird application connects to a public sample application

#### 1. Dashboard setup

* To connect your own SendBird application go to the [SendBird dashboard.](https://dashboard.sendbird.com/)
* Open an existing application or create a new one
* From the SendBird dashboard copy the "App ID"

#### 2. Application setup

#### 3. Android Studio - change application ID

* In your project using Android Studio navigate to ``src/sendbirdActions/user.js`` 
* Replace the default "APP_ID" with your SendBird Application ID
* Save the file

#### Xcode - change application ID

* In your project using Android Studio navigate to ``src/sendbirdActions/user.js`` 
* Replace the default "APP_ID" with your SendBird Application ID
* Save the file

### Apply connection changes

* If the Metro Bundler is running terminate it.
* Start the application again        
  - In Android Studio terminal ``react-native run-android``
  - In the regular terminal for Xcode navigate to `SendBird-JavaScript/react-native-redux-sample/ReactNativeWithSendBird/ios`  and run ``react-native run-ios``


#### Add a new user using SendBird React-Native App
* Open the SendBird application in the emulated Android or ios device and create a new user

#### View the new user on the SendBird dashboard
* Navigate to the SendBird [dashboard](https://dashboard.sendbird.com/) click on "users" to view the newly create user

        


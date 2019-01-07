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

1. Install React Native CLI.

        npm install -g react-native-cli

3. Open Android Studio click "Open an existing Android Studio project" and navigate to `SendBird-JavaScript/react-native-redux-sample/ReactNativeWithSendBird`.

2. Open the terminal in Android Studio(bottom left) and install the npm packages.

        npm install
        

3. Start a [new emulated device.](https://developer.android.com/studio/run/managing-avds) Whichever device you create, set it up with Oreo 27 as per React Native's requirements (this code was tested to work with a "Galaxy Nexus" device).

5. Complete the emulator set up: 
* Go to emulated device's "settings" and click "FINISH SETUP". Carefully complete the set up and don't forget to log in.
* After setup completes, on the device [start developer mode.](https://developer.android.com/studio/debug/dev-options) 

6. In Android Studio start the React Native compiler using the terminal.

        react-native run-android
        
7. To connect your own SendBird application go to the SendBird dashboard open and existing application or create a new one.

8. In your SendBird Application's dashboard copy the "App ID".

9. In Android Studio navigate to ``src/sendbirdActions/user.js`` and replace the default "APP_ID" with your SendBird Application ID. Save the file.

10. Terminate the Metro Bundler.

11. In Android studio start the application again. 
          
          react-native run-android
          
12. Create a new user. 

13. Back in the SendBird application dashboard click on "users" to view the newly create user. 

## Run the sample - IOS

3. (iOS only) Pod install.

        cd ios
        pod install

4. (iOS only) Add library in XCode

- Open XCode and load workspace
- Right click to 'Libraries' > Add Files to "Project Name" > select `node_modules/react-native/Libraries/PushNotificationIOS/RCTPushNotification.xcodeproj`
- Project Settings > Build Phases > Link Binary With Libraries > Add `libRCTPushNotification.a`

5. Run the sample. Before starting, you should launch device amulator (or actual device) to run the sample in Android. This sample is not available for real device in iOS due to Apple Development Policy. In order to run React Native sample in real device, follow [React Native official guide](https://facebook.github.io/react-native/docs/running-on-device.html) for your own setup.

        react-native run-android
        react-native run-ios

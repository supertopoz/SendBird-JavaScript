# Sample JavaScript React-Native Redux

SendBird React-Native sample using [SendBird SDK](https://github.com/smilefam/SendBird-SDK-JavaScript).

## Prerequisite

- [Node](https://nodejs.org/en/)
- [NPM](https://www.npmjs.com/)
- [Cocoapods](https://cocoapods.org/)
- [XCode](https://developer.apple.com/xcode)
- [XCode Command Line Tools](https://facebook.github.io/react-native/docs/getting-started.html#xcode)
- [Android Studio](https://developer.android.com/studio/) (+Android SDK/Google API)

## Run the sample - Android Studio

1. Install React Native CLI.

        npm install -g react-native-cli

3. Open Android Studio click "Open an existing Android Studio project" and navigate to `SendBird-JavaScript/react-native-redux-sample/ReactNativeWithSendBird`.

2. Open the terminal in Android Studio(bottom left) and install the npm packages.

        npm install
        

3. Start a [new emulated device.](https://developer.android.com/studio/run/managing-avds) Whichever device you create, set it up with Oreo 27 as per React Native's requirements (this code was tested to work on a "Galaxy Nexus").

5. Complete the emulator set up: 
* After the emulated device first starts open the devices "settings" and click "FINISH SETUP".
* Click "START" on the "Finish Android SDK built for..." screen - follow the set up process including logging in.
* After setup completes on the device [start developer mode.](https://developer.android.com/studio/debug/dev-options) 

6. In Android studio start the React Native compiler using the terminal.

        react-native run-android
        
        
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

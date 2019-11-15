# INTRODUCTION
  1. What is React Native?
  - React.js : A javaScript Library for building User Interfaces, Typically used for Web Development, React itself is Platform agnostic
  - React Native: A collection of special React components, components compiled to Native Widgets, Native Platform APIs exposed to JS, Connects Js and Native Platform Code
  - React.js + react Native = React Native Mobiles Apps
  2. Behind the Scenes
  - 
# SET UP
  1. Java jdk: https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
  2. Android studio: https://developer.android.com/studio/ https://facebook.github.io/react-native/docs/getting-started
  3. Nodejs: https://nodejs.org/en/
  4. VSCode: https://code.visualstudio.com/Download
  5. Git SCM: https://git-scm.com/download/
  6. Environment variable:
    - PLATFORM-TOOLS (Modify Path): C:\Users\duc.huynhcong\AppData\Local\Android\Sdk\platform-tools
    - JAVA_HOME (new): C:\Program Files\Java\jdk1.8.0_211
    - ANDROID_HOME (new): C:\Users\duc.huynhcong\AppData\Local\Android\Sdk
  7. VSCode Extension
    1.Auto Rename Tag: (Downloads: 1.1M)
    2.Bracket Pair Colorizer 2 (Donwloads: 66K)
    3.ES7 React/Redux/GraphQL/React-Native snippets (Downloads: 1.1M)
    4.React Native Tools (Downloads: 2.9M)
    5.Material Icon Theme (Downloads: 5M)
    6.One Dark Pro (Downloads: 7.8M)
    7.Debugger for Chrome (Downloads: 15.4M)
    8. Prettier (Downloads: 7.8M)
# CREATE NEW PROJECT
  1. Download init file (contain firebase): https://github.com/invertase/react-native-firebase-starter
  2. Open file by VSC
  3. install react-native: npm install -g react-native-cli
  4. npm install
  5. npm run rename
  6. Firebase link  
    - login : https://console.firebase.google.com
    - create project
    - create app
    - package name: in AndroidManifest.xml (android/app/src/main)
    - download google-service in to path: android/app
  7. run: react-native run-android
# INSTALL NAVIGATION (Stack, Tab, Drawer)
  1. Install  https://reactnavigation.org/docs/en/getting-started.html
    - npm install react-navigation
    - npm install react-native-gesture-handler
  2. Structure
    - navigators
     + screens: DrawerScreens, StackScreens, TabScreens
     + StackNavigator.js
     + TabNavigator.js
     + DrawerNavigator.js
     + SwitchNavigator.js
     + AppNavigator.js
# STOCKS:
  1. All stocks: http://thestocks.im
  2. Font Icons: https://oblador.github.io/react-native-vector-icons
  3. Image Icons: https://www.flaticon.com
  4. Color: https://flatuicolors.com
  4. Face / Avatar: http://pravatar.cc
  5. Animatable (Animation): https://github.com/oblador/react-native-animatable

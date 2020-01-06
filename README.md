# INTRODUCTION
  1. What is React Native?
  - React.js : A javaScript Library for building User Interfaces, Typically used for Web Development, React itself is Platform agnostic
  - React Native: A collection of special React components, components compiled to Native Widgets, Native Platform APIs exposed to JS, Connects Js and Native Platform Code
  - React.js + react Native = React Native Mobiles Apps
  2. Behind the Scenes
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
    8.Prettier (Downloads: 7.8M)
  
# CREATE NEW PROJECT
  0. Structure: https://cheesecakelabs.com/blog/efficient-way-structure-react-native-projects/
  1. Init project: https://facebook.github.io/react-native/docs/getting-started
  + Open gitbash or cmd: react-native init ProjectName
  + Open project on VSC => open Terminal
  + npm install -g react-native-cli (first time)
  + install alias package: npm install --save-dev babel-plugin-module-resolver
  
  2. Navigation: https://reactnavigation.org/docs/en/getting-started.html (step by step)
  + npm install --save react-navigation
  + npm install --save react-navigation-stack
  + npm install --save react-navigation-tabs
  + npm install --save react-native-reanimated react-native-gesture-handler react-native-screens@^1.0.0-alpha.23
  + modify some files : https://reactnavigation.org/docs/en/getting-started.html (step by step)
  + npm install --save react-native-vector-icons
  *add in the end: /app/build.gradle =>
  apply from: "../../node_modules/react-native-vector-icons/fonts.gradle"

  3. Redux saga: https://redux-saga.js.org/
  + npm install --save react-redux
  + npm install --save redux-saga
  + npm install --save redux-devtools-extension
  + npm install --save axios
(https://www.npmjs.com/package/react-native-axios)
  4. Multi language:
  + npm install --save react-native-i18n
  + npm install --save react-native-elements
  5. Add rn_src and run project
  + react-native run-android
  6. Date Picker: https://www.npmjs.com/package/react-native-datepicker
  7. Current time: https://aboutreact.com/react-native-get-current-time-in-12-hours-format-am-pm/
  8. Keyboard: android:windowSoftInputMode="adjustPan"
  
  
  
  
  
# STOCKS:
  1. All stocks: http://thestocks.im
  2. Font Icons: https://oblador.github.io/react-native-vector-icons
  3. Image Icons: https://www.flaticon.com
  4. Color: https://flatuicolors.com
  4. Face / Avatar: http://pravatar.cc
  5. Animatable (Animation): https://github.com/oblador/react-native-animatable
  
# ERRORS:
  1. 'Cannot create directory ...'
  => cd android && gradlew clean && cd .. && react-native run-android
  2. 'Can not delete directory'
  => delete file intermediates (in build and node_module)
  3. 'Package signatures do not match the previously installed version'
  => unstall app
  4. 'Cannot connect api in android 10'
  => add in AndroidManifest.xml : 
  <Application .....
    android:usesCleartextTraffic="true">
    <activity...>
  ...
  <Application>
  
 



  UI
  1. Vector-Icon : cannot show up
  - adding on android/app/build.gradle
  apply from: "../../node_modules/react-native-vector-icons/fonts.gradle"
  => reinstall again.

  2. Drawer cannot show up
  - https://reactnavigation.org/docs/en/getting-started.html: 
  Do step by step
  
  
  # APK Realease
  1. Open Cmd (Admin)
  2. cd C:\Program Files\Java\jre1.8.0_211\bin
  3. Run this code
  keytool -genkey -v -keystore d:\mykeystore.keystore -alias mykeyalias -keyalg RSA -keysize 2048 -validity 10000
  4. Enter information
  5. Copy mykeystore.keystore to android/app
  6. Setup your gradle variables in android/gradle.properties
    MYAPP_RELEASE_STORE_FILE=mykeystore.keystore
    MYAPP_RELEASE_KEY_ALIAS=mykeyalias
    MYAPP_RELEASE_STORE_PASSWORD=*****
    MYAPP_RELEASE_KEY_PASSWORD=*****
  7. Add signing config to android/app/build.gradle
    signingConfigs {
            release {
            storeFile file(MYAPP_RELEASE_STORE_FILE)
            storePassword MYAPP_RELEASE_STORE_PASSWORD
            keyAlias MYAPP_RELEASE_KEY_ALIAS
            keyPassword MYAPP_RELEASE_KEY_PASSWORD
            }
        }
      buildTypes {
            release {
                minifyEnabled enableProguardInReleaseBuilds
                proguardFiles getDefaultProguardFile("proguard-android.txt"), "proguard-rules.pro"
                signingConfig signingConfigs.release

            }
        }
  8. Run
  cd android
  ./gradlew assembleRelease
  9. You apk file in: android/app/build/outputs/apk/app-release.apk
  
  # Advance
  1. Animation
- interpolate: chuyen doi don vi tinh
2. Platform Specific
- chon he dieu hanh, de su dung thuoc tinh khac nhau
- Platform.version: xem version cua dien thoai
- .ios/.android (khi chay se auto chon file ung voi os de chay)
3. Timer
4. Debug
- inspec: ract-devtools
5. Performance monitor
- devetool: console.log
- Animation
- Flatlist
- __DEV__: moi truong dev
6. Screen orentation lock
7. Async Storage: luu tren dia cung cua dien
- bo du lieu mini
- luu tam: auto login


Google map : https://github.com/react-native-community/react-native-maps
** check version: https://www.npmjs.com/search?q=react-native-maps
- install/link: https://github.com/react-native-community/react-native-maps/blob/master/docs/installation.md
- modify: manifest.xml/enter: key (https://developers.google.com/maps/documentation/android-sdk/get-api-key)	

get map: get geolocation
- modify manifest: to get allow: https://facebook.github.io/react-native/docs/geolocation

8. Camera
- install: https://github.com/react-native-community/react-native-camera	
- https://react-native-community.github.io/react-native-camera/docs/installation.html
1.6.4

# API
1. Events cach goi ham
- binding: khi render thi duoc tao lai
- bind(this): co moi su dung duoc this trong ham
- arrow function = da binding(khai bao) o contructor

2. Networking:
ham fetch(''): ham cho phep tuong tac API (web service) co san trong js
- vi js bat dong bo nen phai dung .then
- lenh lm viec voi API nen dat coponent Didmount (display: lam lag UI) do lifecycle cua (cont=>render) nhanh hon
- java call back hell
- muon tuan tu: async await
- truyen params phai chuyen sang string
- co bien de danh giau da loading xong
- ActivityDicator: v?g xoay khi dang loading
- Map: giong lenh for
- Nen co key: de render
3. Axios: tien nghi, cau hinh bai ban hon fetch (set up Axio)
4. Scroll View: Neu lay nhieu du lieu thi render rat lau => khong dung de lap lai mang du lieu (dung de sap xep UI)
5. List view
- FlatView: chi render nhung view chuan bi xuat hien
+ data
+ KeyExtrator
+ renderItem
- Sessionlist: 
6. Postman: test truoc khi lam viec voi API
7. Lam viec voi API
- Description: url, method, body
8 Animitable: chay hieu ung (set up react-native-animatable)

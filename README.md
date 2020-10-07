# Wallet

Ionic 3 App Base Project
=====================

Tam Wallet written in ionic 3 .
Ionic is the open-source mobile app development framework that makes it easy to build top quality native and progressive web apps with web technologies.

Ionic is based on Angular and comes with many significant performance, usability, and feature improvements over the past versions.

## Using this project

You'll need the Ionic CLI with support for v3 apps:

```bash
$ npm install -g ionic@3.20.0.
```

## Creating project

Ionic relies on two dependencies: 
- Ionic Command Line Utility
  - Enables you to use command line commands to easily create Ionic apps
  
  Create New Project Example:
  ```
  $ ionic start <name>
  $ cd ./name
  $ ionic server
  ```
  
- Cordova
  - Enables native capabilties in your apps
  
  iOS Example:
  ```
  $ npm install -g cordova
  $ ionic cordova --help
  $ ionic cordova run ios
  ```
  
  Android Example:
    ```
    $ npm install -g cordova
    $ ionic cordova --help
    $ ionic cordova run android
    ```
  
   ├── .io-config.json              # Ionic ID
   ├── config.xml                   # Ionic config file
   ├── .ionic.config.json           # Global configuration for your Ionic app
   ├── package.json                 # Dependencies and build scripts
   ├── readme.md                    # Project description
   ├── tsconfig.json                # TypeScript configurations
   └── tslint.json                  # TypeScript linting options
  ```
  
  ### src directory
  ```
  .
     ├── ...
     ├── src                       
     │   ├── app                    # This folder contains global modules and styling
     │   ├── assets                 # This folder contains images and the *data.json*
     |   ├── pages                  # Contains all the individual pages (home, tabs, category, list, single-item)
     |   ├── services               # Contains the item-api service that retrieves data from the JSON file
     |   ├── theme                  # The global SCSS variables to use throughout the app
     |   ├── declarations.d.ts      # A config file to make TypeScript objects available in intellisense
     |   ├── index.html             # The root index app file - This launches the app
     |   ├── manifest.json          # Metadata for the app
     │   └── service-worker.js      # Cache configurations
     └── ...
  ```
  
  
  ## Start the project
  The project is started with the regular ionic commands.
  
  1. Run `npm install` to install all dependencies.
  2. Run `ionic serve` to start the development environment.
  3. To build the project run `ionic build android` or `ionic build ios`. In order for you to build an iOS app, you need to run on MacOS.
  
  An alternative is to emulate the app on a device or upload it to the ionic cloud. From here you can download the ionic view app and use the app on all devices.

#Releasing & *FB Authentication*#
ionic plugin add cordova-plugin-facebook4 --variable APP_ID="1336689246395066" --variable APP_NAME="iMobileDemo"

http://www.angulartypescript.com/angular-2-ionic-2-build-android/
Requieremnet Open SSL
Hash Fix - https://forum.ionicframework.com/t/key-hash-for-facebook-not-working/44357/5 

*For andorid*
- gen key

keytool -export -alias iMobileDemo -keystore iMobileDemo.keystore | C:\OpenSSL\bin\openssl sha1 -binary | C:\OpenSSL\bin\openssl base64
keytool -list -printcert -jarfile android-debug.apk

- gen hash

keytool -genkey -v -keystore iMobileDemo.keystore -alias iMobileDemo -keyalg RSA -keysize 2048 -validity 10000

Or 

keytool -export -alias iMobileDemo -keystore C:\Users\User\Desktop\ionic\MyIonic2Project\platforms\android\iMobileDemo.keystore | C:\OpenSSL\bin\openssl sha1 -binary | C:\OpenSSL\bin\openssl enc -a -e

// To get proper hash use Hash Fix - https://forum.ionicframework.com/t/key-hash-for-facebook-not-working/44357/5 
//Short Cut to get Hex - keytool -exportcert -keystore C:\Users\User\Desktop\ionic\MyIonic2Project\platforms\android\iMobileDemo.keystore -list -v

1.  Copy the file to java folder and run
2. keytool -list -printcert -jarfile android-release-unsigned.apk
3. Get sha1
4. Convert from http://tomeko.net/online_tools/hex_to_base64.php and put it in FB

#Gen has for debug#
keytool -exportcert -keystore path-to-debug-or-production-keystore -list -v
-7C:B2:0C:5B:86:A7:EB:CD:2E:F0:D8:18:04:6E:E2:A5:A2:AD:83:BC
1.  Copy the file to java folder and run
2. keytool -list -printcert -jarfile android-debug.apk
3. Get sha1
4. Convert from http://tomeko.net/online_tools/hex_to_base64.php and put it in FB



#Google Plus#
{"installed":
{"client_id":"366054038002-nq33mmkpoelanhgua7d5am2lu8fgs31g.apps.googleusercontent.com",
"project_id":"test-1-154115",
"auth_uri":"https://accounts.google.com/o/oauth2/auth",
"token_uri":"https://accounts.google.com/o/oauth2/token",
"auth_provider_x509_cert_url":"https://www.googleapis.com/oauth2/v1/certs",
"redirect_uris":["urn:ietf:wg:oauth:2.0:oob","http://localhost"]},
REVERSED_CLIENT_ID: "com.googleusercontent.apps.366054038002-nq33mmkpoelanhgua7d5am2lu8fgs31g"
}

ionic plugin add cordova-plugin-googleplus --save --variable REVERSED_CLIENT_ID=com.googleusercontent.apps.366054038002-nq33mmkpoelanhgua7d5am2lu8fgs31g



#Twitter#
https://ionicthemes.com/tutorials/about/ionic2-twitter-login
Fabric API - bc96a62edb8467d017903eb8fcd71fa366329f08
Consumer Key (API Key)	bd9flnVtMqxNiM800LlFjW13l
Consumer Secret (API Secret)	eSMnkpryProV0nFoI8tcLadt0VNlQGRkYXDkSh0WC6bgYfyZGJ

ionic plugin add twitter-connect-plugin --variable FABRIC_KEY=bc96a62edb8467d017903eb8fcd71fa366329f08

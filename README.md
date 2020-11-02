# https://ionicframework.com/docs

TAM Wallet Ionic 3 App Base Project
=====================

Tam Wallet written in ionic 3 .
Ionic is the open-source mobile app development framework that makes it easy to build top quality native and progressive web apps with web technologies.

Ionic is based on Angular and comes with many significant performance, usability, and feature improvements over the past versions.

## Using this project

You'll need the Ionic CLI with support for v3 apps:

```bash
$ npm install -g ionic
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
  
  ## Project Structure

```
.
 ├── resources                    # Build files on the specific platforms (iOS, Android) and app icon + splash
 ├── src                          # This is where the app lives - *the main folder*
 ├── .editorconfig                # A helper file to define and maintain coding styles across environments
 ├── .gitignore                   # Specifies intentionally untracked files to ignore when using Git
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

  
 # Further development
we have to youse v3 documentation not v4 documentations

 # Ionic 3 development beginning
 
Creating sample project 

`ionic start MyProject --type=ionic-angular`


ionic info

`ionic info`

`Ionic:

   Ionic CLI          : 5.2.5 (/usr/local/lib/node_modules/ionic)
   Ionic Framework    : ionic-angular 3.9.9
   @ionic/app-scripts : 3.2.3

Cordova:

   Cordova CLI       : 7.1.0
   Cordova Platforms : ios 5.1.1
   Cordova Plugins   : cordova-plugin-ionic-keyboard 2.2.0, cordova-plugin-ionic-webview 5.0.0, (and 41 other plugins)

Utility:

   cordova-res : 0.14.0 (update available: 0.15.1)
   native-run  : 0.2.7 (update available: 1.2.2)

System:

   Android SDK Tools : 26.1.1 (/Users/xxxxx/Library/Android/sdk/)
   ios-deploy        : 1.11.0
   ios-sim           : 8.0.2
   NodeJS            : v12.16.1 (/usr/local/bin/node)
   npm               : 6.14.4
   OS                : macOS Catalina
   Xcode             : Xcode 11.6 Build version 11E708
`
https://ionicframework.com/docs/v3/

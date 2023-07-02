Roku Summer Practice
=====================================

- - - -

# Description

Roku application developed during the Summer Practice 2023.


## Requirements

- [Node](https://nodejs.org/en/download/) **v12+**

## Quick reference

* I want to find all devices from the network

    * Install [BrightScript Language extension for VSCode](https://marketplace.visualstudio.com/items?itemName=RokuCommunity.brightscript) and select the "BRS" tab in order to see the active devices list. For a more in-depth guide please see the [extension documentation](https://rokucommunity.github.io/vscode-brightscript-language).

* I want to build my project
```
bsc --deploy false
```

## Deploy app
To deploy the current application on your roku device, you need to follow the steps:

### 1. Enable Developer mode on you're device

Go to roku home screen and press:

```
Home 3x, Up 2x, Right, Left, Right, Left, Right
```

- Save `username` and `ip address` provided by roku. We will need them later to build and run our code.
- Click on `Enable installer and restart`.
- After that you will be asked if you agree SKD License Agreement.
- Click "I agree" after you read it.
- Now you will need to setup the `developer webserver password`.
- After that Click on `Set password and reboot`

After reboot you're roku device will be in developer mode.

### 2. Install project dependencies

If your not setup your project yet, run following command to install all project dependencies:
```
npm install
```

### 3. Upload app to roku device

To upload the app on your device run:
```
bsc
```

## Debug app
To debug our app we can use the telnet network protocol. In order to do so, launch the telnet into your Linux terminal by using the following command:
```
telnet [device-ip] 8085
```

## Config file
The `bsconfig.json` file is the application configuration file used for building applications using the BrighterScript language.

In order to be able to deploy the application to a specific device, make sure to configure hhe following field:
```
"host": "your-roku-ip"
```
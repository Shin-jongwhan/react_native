# 221104

# React Native Tutorial for Beginners - Build a React Native App
### https://www.youtube.com/watch?v=0-S5a0eXPoc&t=573s

### <br/><br/><br/>
--------------------------------------
--------------------------------------

## setting up dev environment
### 1. visual studio code
#### https://code.visualstudio.com/
### <br/><br/>

### 2. npm (node.js)
### install
#### https://nodejs.org/en/
### check version
#### ![image](https://user-images.githubusercontent.com/62974484/199886353-61a263d5-88fa-48c6-9405-086ae07301af.png)
### <br/><br/>

### 3. expo
```
# i = install
> npm install -g react-native-cli
> npm i -g expo-cli
```
### <br/><br/>

### 3-2. expo client
#### It's android app which is to execute the app you created.
### <br/><br/>
### VS code extension : react antive tools
#### ![image](https://user-images.githubusercontent.com/62974484/199887798-02927c6e-d8ed-4e13-8a6d-6f3a3d7b0d15.png)
### <br/><br/>

### VS code extension : React-Native/React/Redux snippets for es6/es7
#### ![image](https://user-images.githubusercontent.com/62974484/199889734-7b574098-1a53-457b-990b-0a548b5e7cf6.png)
### <br/><br/>

### VS code extension : Prettier - Code formatter
#### ![image](https://user-images.githubusercontent.com/62974484/199890004-5a5cb0cc-c7ec-4753-b712-08425a4e6113.png)
### <br/><br/>

### VS code extension : Prettier - Material Icon Theme
#### ![image](https://user-images.githubusercontent.com/62974484/199890066-837e4e5a-2d3e-4695-9bc7-379149cac292.png)
#### ![image](https://user-images.githubusercontent.com/62974484/199890107-83c2f941-02b2-44e2-861d-68e0c8ae893d.png)
### <br/><br/>

### VS code - preferences - settings : format on save -> enabled
#### It can automatically format unnecessary multiple space to single space etc...
#### ![image](https://user-images.githubusercontent.com/62974484/199890618-4d7f0637-e870-4795-afe5-aec975a5b4d0.png)
#### ex)
#### ![image](https://user-images.githubusercontent.com/62974484/199890850-8ac40235-850f-42da-a56e-5a02d54b6b72.png)
#### ![image](https://user-images.githubusercontent.com/62974484/199890898-6f7e81a5-a474-46c6-b65c-06b1c6f6e424.png)
### <br/><br/>

### android studio for android emulator
#### https://developer.android.com/studio?hl=ko
#### ![image](https://user-images.githubusercontent.com/62974484/200297974-65060f0a-2521-4f23-b289-cb1f9f270d8c.png)
#### ![image](https://user-images.githubusercontent.com/62974484/200298421-373f87c8-e6b7-4e60-841b-1c2e4d79b2cd.png)
#### ![image](https://user-images.githubusercontent.com/62974484/200298780-89e58919-04fe-438d-a755-55a7d452e780.png)
### install android emulator, the version you're interested in
#### ![image](https://user-images.githubusercontent.com/62974484/200299021-d7afa888-0e75-4fa3-8f95-c832dbded7bf.png)
### register and execute emulator
#### ![image](https://user-images.githubusercontent.com/62974484/200299313-5328e1fc-a0a3-40b9-b5b2-296b576917e0.png)
#### ![image](https://user-images.githubusercontent.com/62974484/200300000-451ca1de-acb0-4cee-8051-7de31bcfb4f9.png)
#### ![image](https://user-images.githubusercontent.com/62974484/200300092-d417e412-d03b-42ca-ab64-271804352d28.png)

### <br/><br/><br/>

--------------------------------------

## Your first native app
### init
```
> expo init DoneWithIt
```
### choose one of these otions. We gonna choose blank.
#### ![image](https://user-images.githubusercontent.com/62974484/199898330-b9fbbf39-953a-4f09-b901-4cf0d0aad5ca.png)
```
> cd DoneWithIt
# code . -> open current folder on VS code
> code .
```

### app.js
```
import React from 'react';
import { StatusBar } from 'expo-status-bar';
import { StyleSheet, Text, View } from 'react-native';

// View -> UIView
export default function App() {
  return (
    <View style={styles.container}>
      <Text>Open up App.js to start working on your app!</Text>
      <StatusBar style="auto" />
    </View>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#fff',
    alignItems: 'center',
    justifyContent: 'center',
  },
});
```

### execute command
```
> npm start
```
#### ![image](https://user-images.githubusercontent.com/62974484/200295436-6e60b1df-c884-42f2-8621-946d21d426e2.png)

### install 'Expo Go' into tour mobile phone, and scan QR code
#### ![image](https://user-images.githubusercontent.com/62974484/200295099-7246548c-fa85-4ca4-a1aa-5f64ad8db446.png)
#### ![image](https://user-images.githubusercontent.com/62974484/200295563-8883a632-c966-4882-8e28-46c2f16d901a.png)

### You can connect your app onto android emulator
### press a
#### ![image](https://user-images.githubusercontent.com/62974484/200337028-5979631b-1a6c-4be1-afde-faa6c7734067.png)
### check your emulator
#### ![image](https://user-images.githubusercontent.com/62974484/200300791-956cba75-c124-4e4c-ba8b-c6ce951b79b2.png)
### menubar for expo app : ctrl + M
#### ![image](https://user-images.githubusercontent.com/62974484/200335663-5352ff13-b0f6-46ed-987e-e8721a26b2af.png)

### <br/><br/><br/>

--------------------------------------

## Debugging - logging
### console.log("str")
```
// View -> UIView
export default function App() {
  console.log("App executed")
  return (
    <View style={styles.container}>
      <Text>Hello React Native !</Text>
      <StatusBar style="auto" />
    </View>
  );
}
```
#### ![image](https://user-images.githubusercontent.com/62974484/200340769-8b0aba74-0530-44df-b80f-8e80556b1c3b.png)

### <br/><br/><br/>

--------------------------------------

## debugging
### http://localhost:[port_num]/debugger-ui/
#### ![image](https://user-images.githubusercontent.com/62974484/200342464-a848db22-1a5f-4a2a-aefc-8b10fcc707b3.png)
### <br/><br/>

### press F12 and see console window
#### ![image](https://user-images.githubusercontent.com/62974484/200342645-344a7836-3d51-48b8-bf5f-7b22b1891e11.png)
### <br/><br/>

### dev tools - source - pause button
### and check 'pause on caught exceptions' (catch된 예외에서 일시 중지)
#### ![image](https://user-images.githubusercontent.com/62974484/200343570-41457234-d617-49a9-964a-a2916ac82bc8.png)
### <br/><br/>

### The error will be stop at error code and You can check what error occur.
https://user-images.githubusercontent.com/62974484/200348266-613e0190-076c-4535-a31e-1dc531005344.mp4
### <br/>

### You can type variables into 'Watch (조사식)' and it show you what the variant type is.
#### ![image](https://user-images.githubusercontent.com/62974484/200349452-050a481a-ed1b-4d55-b342-f943447bc7ce.png)

### <br/><br/><br/>

--------------------------------------

## debug in VScode
### [make sure you installed react native tools extension]
### Go to 'run and debug' and click create json file, check attach to packager
#### ![image](https://user-images.githubusercontent.com/62974484/200353616-97c5eda6-6b5d-4f54-acae-0fa538b12ed8.png)
#### ![image](https://user-images.githubusercontent.com/62974484/200354486-e9468936-2f13-494f-a33b-5c0dcc9492a2.png)
#### ![image](https://user-images.githubusercontent.com/62974484/200354560-303ad4ba-73cb-458e-a157-a7e8d8106cbe.png)
#### ![image](https://user-images.githubusercontent.com/62974484/200354623-4b987576-8b51-4b3e-afff-b8e0fe4f57b7.png)
#### ![image](https://user-images.githubusercontent.com/62974484/200354776-68abd8a3-2480-45d2-a933-a826f38b8b8f.png)
### <br/>

### Automatically added 'debug android' into json file
```
{
  // Use IntelliSense to learn about possible attributes.
  // Hover to view descriptions of existing attributes.
  // For more information, visit: https://go.microsoft.com/fwlink/?linkid=830387
  "version": "0.2.0",
  "configurations": [
    {
      "name": "Debug Android",
      "request": "launch",
      "type": "reactnative",
      "cwd": "${workspaceFolder}",
      "platform": "android"
    },
    {
      "name": "Attach to packager",
      "cwd": "${workspaceFolder}",
      "type": "reactnative",
      "request": "attach"
    }
  ]
}
```
### <br/>

### You can insert red dot to the left of the code
#### ![image](https://user-images.githubusercontent.com/62974484/200357656-f9297791-8eb0-4cd5-a4ae-c081742a8252.png)
### <br/>

### select attach to packager and click run button
#### ![image](https://user-images.githubusercontent.com/62974484/200357401-95989827-1af3-4946-8901-03feeb1a15aa.png)
### <br/>

### settings - preference - change react native port
#### ![image](https://user-images.githubusercontent.com/62974484/200596323-59e58100-f4c7-4600-b3eb-5fcd83137780.png)
#### ![image](https://user-images.githubusercontent.com/62974484/200596648-9ec54fc4-1fa2-494a-8b2f-564b947912a5.png)
### <br/>

### execute debugger.
### caution : The web debugger browser should close.
#### ![image](https://user-images.githubusercontent.com/62974484/200599135-1f5436b1-9ca9-435b-b67c-12c7261151e7.png)
### <br/>

### You can pause app here
#### ![image](https://user-images.githubusercontent.com/62974484/200597562-3bed843b-4e83-4e1a-8cf0-18fe24b26a8d.png)
### You can continue through pressing continue button
#### ![image](https://user-images.githubusercontent.com/62974484/200597980-e78dad37-af58-4b50-9248-e22a47a3c642.png)
### check log
#### ![image](https://user-images.githubusercontent.com/62974484/200598778-092f8f7f-3de5-4bac-b12d-2186694e82e4.png)

### <br/><br/><br/>
--------------------------------------

## Publishing



--------------------------------------

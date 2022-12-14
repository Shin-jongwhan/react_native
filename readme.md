# 221104

# React Native Tutorial for Beginners - Build a React Native App
### https://www.youtube.com/watch?v=0-S5a0eXPoc&t=573s
### <br/><br/>

# react native
### https://reactnative.dev/docs/0.69/components-and-apis

### <br/><br/><br/>
--------------------------------------
# 목차
### <br/><br/><br/>

## 1. Settings
## 2. Llogging, debugging, publishing
## 3. Fundamental concepts and components
## 4. Layouts
## 5. Excercises


### <br/><br/><br/>

--------------------------------------

## 1. Settings
### <br/><br/><br/>

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
# 2. Llogging, debugging, publishing
### <br/><br/><br/>

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
### app.json : check publishing info
#### ![image](https://user-images.githubusercontent.com/62974484/200603322-82727fcf-f259-4ed6-af3c-d52c3b25b721.png)
### <br/><br/>

### go to expo io and sign up
#### https://expo.dev/
### <br/>

### In terminal, type
```
> expo publish
```
<br/>

### You can find the published app at expo io
#### ![image](https://user-images.githubusercontent.com/62974484/200603974-9cb383b8-60f5-4e49-a1ed-47acd43af6b6.png)
### <br/>

### in terminal
### https://expo.dev/@\[user_name\]/DoneWithIt
#### ![image](https://user-images.githubusercontent.com/62974484/200605471-aaa01bbc-28cf-4d50-8503-790732fe6c46.png)

### <br/><br/><br/>
--------------------------------------

## build (expo)
### 상업적으로 사용하려면 유료다. 비싸다... expo 로는 build 해보고 테스트 용으로만 사용한다.
### 상업적인 이용은 react-native-cli 로 build 한다.
#### ![image](https://user-images.githubusercontent.com/62974484/200618769-f718fbe2-19d9-4308-8248-1e32ba5b9485.png)
### <br/>

### see site below to build to expo
#### https://docs.expo.dev/build/setup/
```
> npm install -g eas-cli
> eas login
> eas build:configure
> eas build --platform android
```
### <br/>

### build complete
#### ![image](https://user-images.githubusercontent.com/62974484/200619572-fdef3aa7-fd93-4046-a23b-fa030b0ac29f.png)

### <br/><br/><br/>
--------------------------------------

# 3. Fundamental concepts and components
### <br/><br/><br/>

## view - SafeAreaView
### Let's check how the words are aligned.
### remove algin component on styles variable in app.js 
### app.js
```
const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: 'dodgerblue'
  },
});
```
### add `SafeAreaView`
```
import { StyleSheet, Text, View, SafeAreaView } from 'react-native';
```
### <br/>

### Words are aligned left top. There is no margin.
#### ![image](https://user-images.githubusercontent.com/62974484/200624170-c642e182-9aee-4742-8ed9-bd0de94c89b7.png)

### edit app()
```
  return (
    <View style={styles.container}>
      <Text>Hello React Native !</Text>
      <StatusBar style="auto" />
    </View>
  );
```
### to
```
  return (
    <SafeAreaView style={styles.container}>
      <Text>Hello React Native !</Text>
    </SafeAreaView>
  );
```
### <br/>

### You can check the safe area
#### ![image](https://user-images.githubusercontent.com/62974484/200625819-dc4c0304-4747-43ee-85a7-e24972bf2e25.png)

### <br/><br/>

### SafeAreaView doesn't work ! -> how to fix
#### * SafeAreaView is working on ios only.
### I would advise you to not just follow safeAreaView functionalities. rather its better extract the Status bar height and give a marginTop to whole container so its always below the status bar.
#### https://stackoverflow.com/questions/59428494/safeareaview-not-work-views-go-above-the-notification-tab
```
const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: 'dodgerblue',
    marginTop:StatusBar.currentHeight
  },
});
```
### <br/>

### Not recommend : only use SafeAreaView (error)
#### ![image](https://user-images.githubusercontent.com/62974484/200882946-8f9845e0-368e-44eb-9bff-dd0866ed3976.png)
### <br/>

### Recommend : use `marginTop:StatusBar.currentHeight`
#### ![image](https://user-images.githubusercontent.com/62974484/200883102-423641ce-ace9-4988-bf7c-d9348ae76b3d.png)

### <br/><br/><br/>
--------------------------------------

## Text
### See react native docs
#### https://reactnative.dev/docs/0.69/text
### <br/><br/>

### `NumberOfLines`
#### ![image](https://user-images.githubusercontent.com/62974484/200884283-c22b10aa-bbf4-4dea-a468-dca6f745f40d.png)
```
  return (
    <SafeAreaView style={styles.container}>
      <Text>
        Hello React Native ! 1 Hello React Native ! 2 Hello React Native ! 3 Hello React Native ! 4 Hello React Native ! 5
      </Text>
    </SafeAreaView>
  );
}
```
#### ![image](https://user-images.githubusercontent.com/62974484/200884988-7c0aec48-d3d2-465c-b81d-308161a09130.png)
### <br/>

### add numberOfLines to Text area
```
      <Text numberOfLines={1}>
        Hello React Native ! 1 Hello React Native ! 2 Hello React Native ! 3 Hello React Native ! 4 Hello React Native ! 5
      </Text>
```
#### ![image](https://user-images.githubusercontent.com/62974484/200885295-f2be37f9-6e36-4017-8d3c-7c995c2c7d26.png)
### <br/>

### Let's add `onPress`
```
      <Text numberOfLines={1} onPress={() => console.log("Text clicked")}>
```

### or
```
  const handlePress = () => console.log("Text pressed");

  return (
    <SafeAreaView style={styles.container}>
      <Text numberOfLines={1} onPress={handlePress}>
      ....
```
https://user-images.githubusercontent.com/62974484/200886753-dc1dcaeb-315c-4593-9f19-8a042be21c5b.mp4

### <br/><br/><br/>
--------------------------------------

## Image

### add `Image`
```
import { StyleSheet, Text, View, SafeAreaView, StatusBar, Image } from 'react-native';
```

#### add `<Image source = {require('./assets/icon.png')} />`
```
return (
    <SafeAreaView style={styles.container}>
      <Text numberOfLines={1} onPress={() => console.log("Text clicked")}>
        Hello React Native !
      </Text>
      <Image source = {require('./assets/icon.png')} />
    </SafeAreaView>
  );
```
#### ![image](https://user-images.githubusercontent.com/62974484/200890817-a461ea39-2c4d-4a7a-b816-493ce61f8dfd.png)
### <br/>

### `require` function return value is number
### You can check through console
```
console.log(require("./assets/icon.png"))
```
#### ![image](https://user-images.githubusercontent.com/62974484/200891159-6edb4756-0aba-4f7c-84f5-d101645b079c.png)
### <br/>

### resize image
```
      <Image 
        style = {{ width: '100%' }}
        source = {{
          height: 200,
          uri: require("./assets/icon.png")
        }}
        resizeMode='cover'
      />
```
#### ![image](https://user-images.githubusercontent.com/62974484/200895271-252594d7-2a5d-4ea9-be56-c24f6d9643e7.png)
### <br/>

### There's some problem with image size
### See `resizeMode`
#### ![image](https://user-images.githubusercontent.com/62974484/200900226-bf3cf78d-1ff1-4f3c-a50e-19469500f1d5.png)

### code cleanup using StyleSheet
```
  return (
    <SafeAreaView style={styles.container}>
      <Text numberOfLines={1} onPress={() => console.log("Text clicked")}>
        Hello React Native !
      </Text>
      <Image 
        style = {styles.logo}
        source = {{
          uri: require("./assets/icon.png")
        }}
      />
    </SafeAreaView>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#fff',
    marginTop:StatusBar.currentHeight,
    justifyContent: "center",
    alignItems: "center"
  },
  logo: {
    width: 200,
    height: 300,
    resizeMode: 'cover'
  },
});
```
### `resizeMode: 'cover'`
#### ![image](https://user-images.githubusercontent.com/62974484/200897389-7b30e0aa-9e87-47fc-a6fc-7a80396426d7.png)
### <br/>

### `resizeMode: 'stretch'`
#### ![image](https://user-images.githubusercontent.com/62974484/200897550-0747afdb-86b2-4412-89bd-7881957c9b6e.png)
### <br/>

### You can also put url image
```
      <Image 
        style = {styles.logo}
        source = {{
          uri: "https://cdn.pixabay.com/photo/2022/01/18/07/36/cat-6946498_960_720.jpg"
        }}
      />
```
#### ![image](https://user-images.githubusercontent.com/62974484/200898531-aac25ccd-fd8c-42e6-b93a-0d177b9d4b92.png)
### <br/>

### `blurRadius`
```
      <Image 
        style = {styles.logo}
        blurRadius = {10}
        source = {{
          uri: "https://cdn.pixabay.com/photo/2022/01/18/07/36/cat-6946498_960_720.jpg"
        }}
      />
```
#### ![image](https://user-images.githubusercontent.com/62974484/200898889-8a1c69c3-d6f3-4bcc-b27b-cc6d30262010.png)
### <br/>

### `fadeDuration`
### It only works in android, it has no effects in ios app
```
      <Image 
        style = {styles.logo}
        blurRadius = {10}
        fadeDuration = {1000}
        source = {{
          uri: "https://cdn.pixabay.com/photo/2022/01/18/07/36/cat-6946498_960_720.jpg"
        }}
      />
```
https://user-images.githubusercontent.com/62974484/200899770-6d985e4d-f60f-4525-b07e-113a439efb79.mp4
### <br/>

### <br/><br/><br/>

--------------------------------------
## touchables
### <br/><br/><br/>

```
import { 
  StyleSheet, 
  Text, 
  TouchableWithoutFeedback, 
  TouchableOpacity,
  TouchableHighlight,
  TouchableNativeFeedback,
  View, 
  SafeAreaView, 
  StatusBar, 
  Image 
} from 'react-native';
```

### `TouchableWithoutFeedback`
### 다음과 같이 Image 태그를 TouchableWithoutFeedback 안으로 감싼다.
### 기능을 알기 위해 onPress 기능으로 log 를 찍어본다.
```
      <TouchableWithoutFeedback onPress = {() => console.log("Image tapped")}>
        <Image 
          style = {styles.logo}
          blurRadius = {10}
          fadeDuration = {1000}
          source = {{
            uri: "https://cdn.pixabay.com/photo/2022/01/18/07/36/cat-6946498_960_720.jpg"
          }}
        />
```
### 이미지를 클릭하면 로그에 찍힌다.
#### ![image](https://user-images.githubusercontent.com/62974484/201522475-3e452def-4d31-4790-9530-90c202192006.png)
### <br/><br/><br/>

### `TouchableOpacity`
#### return 안에다가 넣어준다.
```
      <TouchableOpacity onPress = {() => console.log("Image tapped")}>
        <Image 
          style = {styles.logo}
          blurRadius = {10}
          fadeDuration = {1000}
          source = {{
            uri: "https://cdn.pixabay.com/photo/2022/01/18/07/36/cat-6946498_960_720.jpg"
          }}
        />
      </TouchableOpacity>
```
### 클릭하면 opacity 가 계속 변화한다.
https://user-images.githubusercontent.com/62974484/201522622-802ef223-b2f0-48e5-b83f-f2a10b6ebb36.mp4
### <br/><br/><br/>

### `TouchableHighlight`
#### return 안에다가 넣어준다. 
```
      <TouchableHighlight onPress = {() => console.log("Image tapped")}>
        <Image 
          style = {styles.logo}
          blurRadius = {10}
          fadeDuration = {1000}
          source = {{
            uri: "https://cdn.pixabay.com/photo/2022/01/18/07/36/cat-6946498_960_720.jpg"
          }}
        />
      </TouchableHighlight>
```
### 클릭하면 하이라이트만 슉 하고 나타나고 다시 원래 그림으로 되돌아온다.
https://user-images.githubusercontent.com/62974484/201522774-57f7cd58-a808-4213-b9c9-6578438ebca9.mp4
### <br/><br/><br/>

### `TouchableNativeFeedback`
### 안드로이드 앱에서만 구동한다.
#### return 안에다가 넣어준다.
```
      <TouchableNativeFeedback onPress = {() => console.log("Image tapped")}>
        <View style={{width: 200, height: 70, backgroundColor: "dodgerblue"}}></View>
      </TouchableNativeFeedback>
```
https://user-images.githubusercontent.com/62974484/201526369-708f7381-ee81-43ee-b1e3-4cc979328e81.mp4
### <br/><br/><br/>

--------------------------------------

## Button
### <br/><br/><br/>

### 버튼의 기본 color 는 blue
```
<Button title="Click Me" onPress={() => console.log("Button tapped")}/>
```
#### ![image](https://user-images.githubusercontent.com/62974484/201526896-9f38adf2-8c32-4c0e-9f98-0eab127366ba.png)
### <br/><br/><br/>

### 배경색 변경 태그 : color
#### return 안에 넣어준다.
```
      <Button 
        color="orange"
        title="Click Me" 
        onPress={() => console.log("Button tapped")}
      />
```
#### ![image](https://user-images.githubusercontent.com/62974484/201526982-5c8e5a4d-f6c4-4a68-9ba7-73f8884d6928.png)
### <br/><br/><br/>

--------------------------------------

## alert
### <br/><br/><br/>

### `alert`
### react native 의 기본 기능으로 Button 등에 활용할 수 있다.
```
      <Button 
        color="orange"
        title="Click Me" 
        onPress={() => alert("Button tapped")}
      />
```
https://user-images.githubusercontent.com/62974484/201527172-4ca182b0-c97c-499a-b6c8-0c3dd3814432.mp4
### <br/><br/><br/>

### `Alert`
### import 하여 사용하는 API 이다.
```
import { 
  Alert
} from 'react-native';
```
### <br/>

### 버튼을 호출할 때 안 쪽에 클릭할 수 있는 버튼을 만들어줄 수 있다.
### 버튼 안에 sub-text button 에 기능을 넣어주면 어떤 기능이 실행할지 넣어줄 수 있다.
#### onPress 를 통해 작동하는 것을 보자.
```
      <Button 
        color="orange"
        title="Click Me" 
        onPress={() => Alert.alert("My title", "My messqge", [
          {text: "Yes"}, 
          {text: "No"},
        ])}
      />
```
https://user-images.githubusercontent.com/62974484/201527531-442db5f6-25f6-4d91-8ed0-864ff61a514e.mp4
### <br/><br/><br/>

### Alert.prompt
### ios 에서만 작동한다.
### 안드로이드에서는 클릭만 되고 아무 기능도 안 일어난다.
```
      <Button
        title="Click Me"
        onPress={() => 
          Alert.prompt("My title", "My message", (text) => console.log(text))
        }
      />
```
#### ![image](https://user-images.githubusercontent.com/62974484/201527935-de8aa090-e2af-40ea-8100-41e182173ce9.png)
### <br/><br/><br/>


--------------------------------------

## StyleSheet
### <br/><br/><br/>

### 다음과 같이도 쓸 수 있지만 권장하지 않는다.
```
const containerStyle = {backgroundColor: "orange"};
<SafeAreaView style={containerStyle}>
...
</SafeAreaView>
```
### <br/><br/><br/>

### `StyleSheet.create` 를 사용하는 것을 권장한다.
### stylesheet 의 문법을 검사해준다.
```
  return (
    <SafeAreaView style={styles.container}>
      ...
    </SafeAreaView>
  );

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#fff',
    marginTop:StatusBar.currentHeight,
    justifyContent: "center",
    alignItems: "center"
  },
  logo: {
    width: 200,
    height: 300,
    resizeMode: 'stretch'
  },
}
```
### <br/><br/><br/>

### \[\] 으로 넣어주면 여러 style 을 넣어줄 수 있다.
#### * 맨 마지막에 , 을 넣어주는 것은 separation 을 위해서 편의상 넣어주는 것이다. 안 넣고 싶으면 안 넣어도 된다.
```
  return (
    <SafeAreaView style={[styles.container, styles.background_orange]}>
      <Text numberOfLines={1} onPress={() => console.log("Text clicked")}>
        Hello React Native !
      </Text>
      <Button 
        color="orange"
        title="Click Me" 
        onPress={() => Alert.alert("My title", "My messqge", [
          {text: "Yes", onPress: () => console.log("Yes")}, 
          {text: "No", onPress: () => console.log("No")},
        ])}
      />
    </SafeAreaView>
  );
}

const styles = StyleSheet.create({
  container: {
    flex: 1,
    backgroundColor: '#fff',
    marginTop:StatusBar.currentHeight,
    justifyContent: "center",
    alignItems: "center"
  },
  logo: {
    width: 200,
    height: 300,
    resizeMode: 'stretch'
  },
  background_orange: {
    backgroundColor: 'orange',
  },
}
```
#### ![image](https://user-images.githubusercontent.com/62974484/201528683-b97f73c2-56cb-4af8-85dd-65103a0d1db0.png)
### <br/><br/><br/>

--------------------------------------

## platform-specific code
### <br/><br/><br/>

### `Platform`
### SafeAreaView 는 ios 에서만 동작한다.
### 만약 OS 에서 동작하게 하는 기능을 만들고 싶다면 Platform 을 사용한다.
### <br/>

### Platform 을 지정해주지 않았을 때 -> SafeAreaView 가 작동하지 않는다.
```
  container: {
    flex: 1,
    backgroundColor: '#fff',
    marginTop:StatusBar.currentHeight,
  },
```
#### ![image](https://user-images.githubusercontent.com/62974484/201534148-9e586eab-5c05-4ade-9c31-1eb8b4730420.png)
### <br/>

### Platform 을 지정해줬을 때 -> 특정 기능을 넣어줄 수 있다.
#### android 라면 paddingTop 을 20 주고 아니면 0
```
  container: {
    flex: 1,
    backgroundColor: '#fff',
    paddingTop: Platform.OS === "android" ? 20 : 0
  },
```
#### ![image](https://user-images.githubusercontent.com/62974484/201534198-8cfb724b-d6bd-447a-9121-93b6e9c74a2d.png)
### <br/>

### 이렇게 하면 특정 OS 에서 다른 기능을 할 수 있게 만든다.
### before
```
  container: {
    flex: 1,
    backgroundColor: '#fff',
    marginTop:StatusBar.currentHeight,
    justifyContent: "center",
    alignItems: "center",
  },
```
### after
```
  container: {
    flex: 1,
    backgroundColor: '#fff',
    justifyContent: "center",
    alignItems: "center",
    paddingTop: Platform.OS === "android" ? StatusBar.currentHeight : 0
  },
```
### <br/><br/><br/>

--------------------------------------

# 4. Layout
### <br/><br/><br/>

## Demensions
### <br/><br/><br/>

### mobile OS 는 실제 pixel 을 scale 값을 곱해줘서 구한다.
### mobile OS 의 1 point 는 scale 값이 3 이면 3 pixcel 이다.
#### ![image](https://user-images.githubusercontent.com/62974484/201535533-0b63a663-7d02-48dd-826d-657d206b80f2.png)
### DIP : Density-independent Pixels
### Physical Pixels = DIPs * Scale Factor
### <br/><br/><br/>

### DIP 로 값을 주었을 때
```
export default function App() {
  console.log("App executed");
  return (
    <SafeAreaView>
      <View style={{
        backgroundColor: 'dodgerblue',
        width: 150, 
        height: 70
      }}>
      </View>
    </SafeAreaView>
  );
}
```
#### ![image](https://user-images.githubusercontent.com/62974484/201535676-b038da50-168a-43f4-9b28-66bca5e1bad0.png)
### <br/>

### % 로 값을 주었을 때
```
    <SafeAreaView>
      <View style={{
        backgroundColor: 'dodgerblue',
        width: "50%", 
        height: 70
      }}>
      </View>
    </SafeAreaView>
```
#### ![image](https://user-images.githubusercontent.com/62974484/201535735-1f1e2069-4aeb-47f3-991f-5b9555cad8e7.png)
### <br/><br/><br/>

### Dimension 으로 OS 의 scale 을 확인할 수 있다.
### window, screen 2 가지를 사용할 수 있다.
- window : 현재 앱에서 실제로 사용할 수 있는 크기
- screen : OS 의 전체 크기 
### console.log(Dimensions.get("window"));
```
import { 
  StyleSheet, 
  Text, 
  View, 
  SafeAreaView, 
  StatusBar, 
  Image, 
  Button, 
  Alert,
  Platform,
  Dimensions
} from 'react-native';

// View -> UIView
export default function App() {
  console.log("App executed");
  console.log(Dimensions.get("screen"));

  return (
    <SafeAreaView>
      <View style={{
        backgroundColor: 'dodgerblue',
        width: "50%", 
        height: 70
      }}>
      </View>
    </SafeAreaView>
  );
}
```
#### ![image](https://user-images.githubusercontent.com/62974484/201536011-ce8765b6-4046-4b3e-b78f-91bea924c606.png)
### <br/>


### console.log(Dimensions.get("screen"));
#### ![image](https://user-images.githubusercontent.com/62974484/201536089-97ad74a3-1c11-4e72-a531-12ecc14507fb.png)
### <br/><br/><br/>

--------------------------------------

## Detecting orientation changes
### <br/><br/><br/>

### app.json
### orientation 이라는 항목이 있는데, 여기에 화면에 대해 3가지 지원 모드 설정할 수 있다.
- portrait : 세로 모드
- landcape : 가로 모드
- default : both
#### * expo 에 관한 이야기이다.
```
{
  "expo": {
    "name": "DoneWithIt",
    "slug": "DoneWithIt",
    "version": "1.0.1",
    "orientation": "portrait",
    "icon": "./assets/icon.png",
    "userInterfaceStyle": "light",
    "splash": {
      "image": "./assets/splash.png",
      "resizeMode": "contain",
      "backgroundColor": "#ffffff"
    },
```
### <br/><br/>

### 아래 깃허브는 screen orientation detection function 이다.
### https://github.com/react-native-community/hooks
### npm 설치
```
npm i @react-native-community/hooks
```
### <br/><br/>

### App() 에 log 을 찍어본다. 그럼 스크린의 사이즈 정보를 알 수 있는 값이 출력된다.
```
import { useDimensions } from '@react-native-community/hooks';    // screen orientation detection

export default function App() {
  console.log("App executed");
  //console.log(Dimensions.get("screen"));
  console.log(useDimensions());
  
  return (
    <SafeAreaView style={styles.container}>
      <View style={{
        backgroundColor: 'dodgerblue',
        width: "100%", 
        height: "30%",
      }}>
      </View>
    </SafeAreaView>
  );
}  
```
#### ![image](https://user-images.githubusercontent.com/62974484/202908375-1567e962-393f-420e-b6d0-aeb7bf50cb9b.png)
### <br/><br/>

### 디바이스를 회전시키면 회전시킨 값이 나온다
#### ![image](https://user-images.githubusercontent.com/62974484/202908442-d4bb05de-c3e4-429e-85cd-400d5c2a4d4f.png)
### <br/><br/><br/>

### useDeviceOrientation 는 portrait 인지, landscape 인지 알려준다.
```
import { useDimensions, useDeviceOrientation } from '@react-native-community/hooks';    // screen orientation detection

// View -> UIView
export default function App() {
  console.log("App executed");
  //console.log(Dimensions.get("screen"));
  //console.log(useDimensions());
  console.log(useDeviceOrientation());

  return (
    <SafeAreaView style={styles.container}>
      <View style={{
        backgroundColor: 'dodgerblue',
        width: "100%", 
        height: "30%",
      }}>
      </View>
    </SafeAreaView>
  );
}
```
#### ![image](https://user-images.githubusercontent.com/62974484/202908651-4caf9625-cfc8-4e5a-b877-b1f45d885a13.png)
#### ![image](https://user-images.githubusercontent.com/62974484/202908659-64cb80bc-09e3-46ac-b156-707d441b9a80.png)
### <br/><br/>

### 다음과 같이 가로 모드냐, 세로 모드냐에 따라 어떻게 보여줄지 정할 수 있다.
### 가로 모드일 경우 100%, 세로 모드일 경우 30%
```
export default function App() {
  console.log("App executed");
  //console.log(Dimensions.get("screen"));
  //console.log(useDimensions());
  console.log(useDeviceOrientation());
  const {landscape} = useDeviceOrientation();

  return (
    <SafeAreaView style={styles.container}>
      <View style={{
        backgroundColor: 'dodgerblue',
        width: "100%", 
        height: landscape ? "100%" : "30%",
      }}>
      </View>
    </SafeAreaView>
  );
}
```
### 세로
#### ![image](https://user-images.githubusercontent.com/62974484/202909404-e17fdc31-2404-41ad-8491-9ec2045765b9.png)
### 가로
#### ![image](https://user-images.githubusercontent.com/62974484/202909420-e1a7e5b8-d9b8-4dc5-ba63-c6e7b7ddb369.png)

### <br/><br/><br/>

--------------------------------------

## Flex box
### <br/><br/><br/>

### flex 는 화면 상단부터 어디까지 차지할지 설정해준다.
```
  return (
    <View style={{
      backgroundColor: "dodgerblue",
      flex: 0.5,
    }}></View>
  );
```
#### ![image](https://user-images.githubusercontent.com/62974484/202909679-f08650bb-633c-4903-902a-faad7d5d9c89.png)
### <br/><br/>

### flex component 안 쪽에 3가지 태그를 넣어준다면 3 등분해준다(1:1:1).
### 만약 dodgerblue 에 2 를 넣어주면 2:1:1 이 된다.
```
  return (
    <View style={{
      backgroundColor: "#fff",
      flex: 1,
    }}>
      <View 
        style={{
          backgroundColor: "dodgerblue",
          flex: 1,
        }}
      />
      <View 
        style={{
          backgroundColor: "gold",
          flex: 1,
        }}
      />
      <View 
        style={{
          backgroundColor: "tomato",
          flex: 1,
        }}
      />
    </View>
  );
```
### 1:1:1
#### ![image](https://user-images.githubusercontent.com/62974484/202909822-5bf7ff5a-c142-4bd3-973d-24179e19968f.png)
### 2:1:1
#### ![image](https://user-images.githubusercontent.com/62974484/202909905-64644115-8164-4eac-9d3e-2a5cb4b4cfd1.png)
### <br/><br/>

### `flex direction`
### flex 가 아닌 width 와 height 로 설정해주면 전체 크기에서 등분해준다.
```
  return (
    <View style={{
      backgroundColor: "#fff",
      flex: 1,
    }}>
      <View 
        style={{
          backgroundColor: "dodgerblue",
          width: 100,
          height: 100
        }}
      />
      <View 
        style={{
          backgroundColor: "gold",
          width: 100,
          height: 100
        }}
      />
      <View 
        style={{
          backgroundColor: "tomato",
          width: 100,
          height: 100
        }}
      />
    </View>
  );
```
#### ![image](https://user-images.githubusercontent.com/62974484/202910052-b6227dc1-7945-4290-a023-071b37b028a8.png)
### <br/><br/>

### 세로 정렬 반대
```
    <View style={{
      backgroundColor: "#fff",
      flex: 1,
      flexDirection: "column-reverse"
```
#### ![image](https://user-images.githubusercontent.com/62974484/202910279-4e974f23-67b7-4427-8dd8-886cacf761c9.png)
### <br/><br/>

### 가로 정렬 `flexDirection: "row"`
```
  return (
    <View style={{
      backgroundColor: "#fff",
      flex: 1,
      flexDirection: "row"
```
#### ![image](https://user-images.githubusercontent.com/62974484/202910103-9f0aca0f-5d79-44f7-9e49-29655a7d6142.png)
### <br/><br/>

### 가로 정렬 반대 `flexDirection: "row-reverse"`
```
    <View style={{
      backgroundColor: "#fff",
      flex: 1,
      flexDirection: "row-reverse"
```
#### ![image](https://user-images.githubusercontent.com/62974484/202910158-5e3c2395-0bd3-47fe-80e2-b2c9fb2de27d.png)
### <br/><br/>

### flex 에 대한 가로 축은 primary axis 라고 하고, 세로 축은 cross axis 라고 한다.
#### ![image](https://user-images.githubusercontent.com/62974484/202910376-3c8282f0-6ff0-4039-a553-f3b0edcfba75.png)
### <br/><br/><br/>

--------------------------------------

## justifyContent, alignItems
### <br/><br/><br/>

### 사용 방법
```
    <View style={{
      backgroundColor: "#fff",
      flex: 1,
      flexDirection: "row", // horizontal
      justifyContent: "center", // main
      alignItems: "baseline"  // secondary
```

### `justifyContent`
- center : 중앙 정렬. 
- flex-end : 오르쪽 위
- flex-start : 왼쪽 위
- space-around : 1) 컴포넌트들의 중간에 간격이 같고, 2) 양 끝쪽이 같다.
- space-evenly : 간격이 모두 같다.
- space-between : 양 끝쪽 간격이 없이 중간 간격이 같다.
### <br/><br/>

### `alignItems`
- baseline : 컴포넌트들이 컴포넌트 아래쪽 기준으로 정렬이 된다.
#### ![image](https://user-images.githubusercontent.com/62974484/202910940-286a68c5-a4db-4580-aabc-6b0cd9c9327b.png)
- flex-end : 맨 아래쪽으로 정렬이 된다.
#### ![image](https://user-images.githubusercontent.com/62974484/202910971-3d229d9a-e67d-4c39-ab3d-698279951efd.png)
- flex-start : 부모 컴포넌트 위쪽을 기준으로 정렬이 된다.
#### ![image](https://user-images.githubusercontent.com/62974484/202911051-3e625fdb-d960-4b42-8696-a22f363562fb.png)
- stretch : 세로로 늘린다. justifyCentent 에서 alignItems 지정 안 해주더라도 default value 라서 자동으로 지정이 된다.
```
// dodgerblue 쪽에 height 를 지정 안 해줌
    <View style={{
      backgroundColor: "#fff",
      flex: 1,
      flexDirection: "row", // horizontal
      justifyContent: "center", // main
      alignItems: "stretch"  // secondary
    }}>
      <View 
        style={{
          backgroundColor: "dodgerblue",
          width: 100,
        }}
```
#### ![image](https://user-images.githubusercontent.com/62974484/202911112-9428d047-a7d4-406c-9321-bf238b2e96cf.png)
- center : 가운데를 기준으로 정렬한다.
#### ![image](https://user-images.githubusercontent.com/62974484/202911262-b4e62ff7-4a1e-4316-9b32-bf129250d9e1.png)
### <br/><br/>

### `alignSelf`
### 정렬 기준이 설정되어 있더라도 컴포넌트에 alginSelf 를 설정해주면 그 컴포넌트만 따로 정렬이 된다.
```
      <View 
        style={{
          backgroundColor: "dodgerblue",
          width: 100,
          height: 300,
          alignSelf: "flex-start"
        }}
```
#### ![image](https://user-images.githubusercontent.com/62974484/202911416-a39474a8-aec1-415c-bf5f-5a55506e7462.png)

### <br/><br/><br/>

--------------------------------------

## flexWrap and alignContent
### <br/><br/><br/>

### alignItems 와 alignContent 의 차이점 : alignItems 은 item 에 대해 정렬 기준을 세우고, alignContent 전체 정렬 기준을 세운다. 그리고 alignContent 는 flexWrap 을 같이 써야만 작동한다.

### justifyContent 에서 컴포넌트를 4 가지를 써보자
```
  return (
    <View style={{
      backgroundColor: "#fff",
      flex: 1,
      flexDirection: "row", // horizontal
      justifyContent: "center", // main
      alignItems: "center"  // secondary
    }}>
      <View 
        style={{
          backgroundColor: "dodgerblue",
          width: 100,
          height: 100
        }}
      />
      <View 
        style={{
          backgroundColor: "gold",
          width: 100,
          height: 100
        }}
      />
      <View 
        style={{
          backgroundColor: "tomato",
          width: 100,
          height: 100
        }}
      />
      <View 
        style={{
          backgroundColor: "gray",
          width: 100,
          height: 100
        }}
      />
    </View>
```
### 그러면 양쪽 끝에 약간의 마진이 생긴 것을 알 수 있다.
#### ![image](https://user-images.githubusercontent.com/62974484/202911606-db02df6c-9da9-48ea-ae3c-c170069c2989.png)
### <br/>

### 5 개를 하면 마진이 없어진다.
#### ![image](https://user-images.githubusercontent.com/62974484/202911645-2eceff66-1e3b-455c-b67d-0f82486b863b.png)
### <br/>

### 정렬할 수 있는 컴포넌트 최대 수가 넘어가면 정렬이 이상하게 되는 현상이 발생한 것이다.
### `wrap` 을 써주면 정렬이 깨지는 것을 막을 수 있다. 
```
    <View style={{
      backgroundColor: "#fff",
      flex: 1,
      flexDirection: "row", // horizontal
      justifyContent: "center", // main
      alignItems: "center",  // secondary
      flexWrap: "wrap",
    }}>
```
#### ![image](https://user-images.githubusercontent.com/62974484/202911759-76395db8-63d0-4d37-ac2b-4c97163b8854.png)
### <br/><br/>

### 그런데 수직 정렬이 깨졌다.
### 이럴 때는 `alignContent` 를 써준다.
```
    <View style={{
      backgroundColor: "#fff",
      flex: 1,
      flexDirection: "row", // horizontal
      justifyContent: "center", // main
      alignItems: "center",  // secondary
      alignContent: "center",
      flexWrap: "wrap",
    }}>
```
#### ![image](https://user-images.githubusercontent.com/62974484/202911904-bc8cabae-c894-4066-9ae6-f7b7d48edd44.png)
### <br/><br/><br/>

--------------------------------------

## flexBasis, flexGrow and flexShrink
### <br/><br/><br/>

### `flexBasis`
### width 를 지우고 flexBasis 로 대체해도 같은 결과를 낸다.
### flexBasis 는 width 또는 height 의 역할을 한다.
```
        style={{
          backgroundColor: "dodgerblue",
          flexBasis: 100,
          //width: 100,
          height: 100
        }}
```
### <br/><br/>

### `flexGrow`
### 늘린다.
```
        style={{
          backgroundColor: "dodgerblue",
          flexBasis: 100,
          flexGrow: 1,
          //width: 100,
          height: 100
        }}
```
#### ![image](https://user-images.githubusercontent.com/62974484/202912629-d8e95c7b-9656-405d-8d5f-22f6c7bc5590.png)
### <br/><br/>

### `flexShrink`
### 다음과 같이 하면 화면 밖으로 컴포넌트가 벗어난다.
```
    <View style={{
      backgroundColor: "#fff",
      flex: 1,
      flexDirection: "row", // horizontal
      justifyContent: "center", // main
      alignItems: "center",  // secondary
    }}>
      <View 
        style={{
          backgroundColor: "dodgerblue",
          width: 400,
          height: 100
        }}
      />
```
#### ![image](https://user-images.githubusercontent.com/62974484/202912800-288325d3-674b-4780-abc5-dbc94768b5cf.png)
### <br/>

### flexShrink 를 사용하면 벗어나지 못 하게 크기가 줄어든다.
### 표시 할 영역이 없다면 사라진다.
```
      <View 
        style={{
          backgroundColor: "dodgerblue",
          width: 400,
          flexShrink: 1,
          height: 100
        }}
      />
```
### 다음과 같이 써도 똑같은 결과를 나타낸다.
```
      <View 
        style={{
          backgroundColor: "dodgerblue",
          width: 400,
          flex: -1,
          height: 100
        }}
      />
```
#### ![image](https://user-images.githubusercontent.com/62974484/202912882-d0333073-2320-4c2e-ac66-d35b66cdc0a8.png)
### <br/><br/><br/>

--------------------------------------

## Alsolute and relative positioning
### <br/><br/><br/>

### 컴포넌트에 따로 position 을 줘서 옮길 수 있다.
- top
- bottom
- left
- right
```
      <View 
        style={{
          backgroundColor: "gold",
          width: 100,
          height: 100,
          top: 20
        }}
      />
```
#### ![image](https://user-images.githubusercontent.com/62974484/202913173-68eadbe7-2222-4cc8-b24e-d2e57bab812b.png)
### <br/><br/>

### `position`
- relative : 부모 컴포넌트 기준. default.
- absolute : 전체 화면 기준
### absolute 를 사용하면 부모 컴포넌트의 정렬을 무시한다.
```
      <View 
        style={{
          backgroundColor: "gold",
          width: 100,
          height: 100,
          top: 20,
          left: 20,
          position: "absolute"
        }}
      />
```
#### ![image](https://user-images.githubusercontent.com/62974484/202913376-3aa6e113-4027-4032-9e2d-97b3f698c13b.png)
### <br/><br/>

### relative 를 사용하면 부모 컴포넌트의 정렬을 따른다. relative 가 default 이다.
```
      <View 
        style={{
          backgroundColor: "gold",
          width: 100,
          height: 100,
          top: 20,
          left: 20,
          position: "relative"
        }}
      />
```
#### ![image](https://user-images.githubusercontent.com/62974484/202913413-fb14899a-abff-4cb2-b724-e223a031de4e.png)
### <br/><br/><br/>

--------------------------------------

# 5. Excercises
### <br/><br/><br/>

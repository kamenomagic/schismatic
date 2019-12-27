---
layout: page
title: React Native
---

## Splash Screen Hanging and Unknown agument type 'attribute' in method on Simulator
[Kapil's Blog - Splash Screen](https://www.kapilgoyal.info/2019/12/reactnative-xcode-splash-screen-stucks.html)
```
In the file project_folder/ios/projectcreens/AppDelegate.m
Comment this line [RNSplashScreen show];
```

[Kapil's Blog - Unknown argument type](https://www.kapilgoyal.info/2019/12/react-native-unknown-argument-type.html)
```
React Native — Unknown argument type ‘attribute’ in method -[RCTAppState getCurrentAppState:error:]
Modify this file
project_folder/node_modules/react-native/React/Base/RCTModuleMethod.mm

search for about line 91, or looking for this
static BOOL RCTParseUnused(const char **input)

after this line
return RCTReadString(input, “__attribute__((unused))”) ||

add
RCTReadString(input, “__attribute__((__unused__))”) ||
```


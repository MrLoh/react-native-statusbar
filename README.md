# react-native-status-bar

[![npm package](https://img.shields.io/npm/v/material-ui-pickers.svg)](https://www.npmjs.org/package/@react-native-community/status-bar)
[![CircleCI Status](https://img.shields.io/circleci/project/github/react-native-community/react-native-statusbar/master.svg)](https://circleci.com/gh/react-native-community/workflows/react-native-netinfo/tree/master) ![Supports Android and iOS](https://img.shields.io/badge/platforms-android%20|%20ios-lightgrey.svg) 
![MIT License](https://img.shields.io/npm/l/@react-native-community/status-bar.svg)
[![code style: prettier](https://img.shields.io/badge/code_style-prettier-ff69b4.svg?style=flat-square)](https://github.com/prettier/prettier)

## Getting started

`$ npm install @react-native-community/status-bar --save`

### Mostly automatic installation

`$ react-native link @react-native-community/status-bar`

### Manual installation

#### iOS

1. In XCode, in the project navigator, right click `Libraries` ➜ `Add Files to [your project's name]`
2. Go to `node_modules` ➜ `react-native-status-bar` and add `RNCStatusBar.xcodeproj`
3. In XCode, in the project navigator, select your project. Add `libRNCStatusBar.a` to your project's `Build Phases` ➜ `Link Binary With Libraries`
4. Run your project (`Cmd+R`)<

#### Android

1. Open up `android/app/src/main/java/[...]/MainActivity.java`

- Add `import com.reactnativecommunity.statusbar.RNCStatusBarPackage;` to the imports at the top of the file
- Add `new RNCStatusBarPackage()` to the list returned by the `getPackages()` method

2. Append the following lines to `android/settings.gradle`:
   ```
   include ':react-native-status-bar'
   project(':react-native-status-bar').projectDir = new File(rootProject.projectDir,  '../../node_modules/@react-native-community/status-bar/android')
   ```
3. Insert the following lines inside the dependencies block in `android/app/build.gradle`:
   ```
   implementation project(':react-native-status-bar')
   ```

## Usage

```javascript
import StatusBar from '@react-native-community/status-bar';

function MyComponent() {
  return (
    <TouchableHighlight
      style={styles.wrapper}
      onPress={() => StatusBar.setHidden(true, "slide");} // or "fade"
    >
      <View style={styles.button}>
        <Text> Hide status bar </Text>
      </View>
    </TouchableHighlight>
  )
}
```

### react-native-dropdownalert

[![npm version](http://img.shields.io/npm/v/react-native-dropdownalert.svg?style=flat-square)](https://www.npmjs.com/package/react-native-dropdownalert "View this project on npm")
[![npm version](http://img.shields.io/npm/dm/react-native-dropdownalert.svg?style=flat-square)](https://www.npmjs.com/package/react-native-dropdownalert "View this project on npm")
[![Build Status](https://travis-ci.org/devBrian/react-native-dropdownalert.svg?branch=master)](https://travis-ci.org/devBrian/react-native-dropdownalert)

A dropdown alert that allows you to display bits of information to your user. Try 1 of 3 types or roll your own custom type (see props below). Tap the alert to close or provide a time interval to close automatically.

### Demo

![screenshot](https://raw.github.com/devBrian/react-native-dropdownalert/master/screenshots/demo.gif)

### Usage

```javascript

import DropdownAlert from 'react-native-dropdownalert'
// ...
constructor(props) {
  super(props);
  this.showAlert = this.showAlert.bind(this)
}
render() {
  return (
    <View>
      <DropdownAlert ref={"dropdownalert"} />
      <TouchableHighlight onPress={this.showAlert}>
        <Text> {'Show Alert'} </Text>
      </TouchableHighlight>
    </View>
  )
}
showAlert() {
  this.refs.dropdownalert.alert('info', 'Info', 'Chicago Cubs won the World Series!')
}
// ...

```

### Types 

![screenshot](https://raw.github.com/devBrian/react-native-dropdownalert/master/screenshots/info.png)
![screenshot](https://raw.github.com/devBrian/react-native-dropdownalert/master/screenshots/warning.png)
![screenshot](https://raw.github.com/devBrian/react-native-dropdownalert/master/screenshots/error.png)
![screenshot](https://raw.github.com/devBrian/react-native-dropdownalert/master/screenshots/custom.png)

### Props

| Props name | Type | Description | Platform | Default
| ------------ | ------------- | ------------ |------------ |------------ |
| closeInterval | Number  | Dismiss alert at a certain interval | Both | 4000
| backgroundColor | String  | background color | Both | steelblue
| imageUri | String  | source uri for network image | Both | ''
| imageSrc | Number  | source for local image | Both | null
| textColor | String  | color for title and message | Both | white
| fontFamily | String  | font for title and messsage | Both | HelveticaNeue
| startDelta | Number  | where view animation starts | Both | -100
| endDelta | Number  | where view animation ends | Both | 0


Inspired by: [RKDropdownAlert](https://github.com/cwRichardKim/RKDropdownAlert)

### License

[MIT](https://raw.github.com/devBrian/react-native-dropdownalert/master/LICENSE)

# react-native-optimized-flatlist

[![Greenkeeper badge](https://badges.greenkeeper.io/stoffern/react-native-optimized-flatlist.svg)](https://greenkeeper.io/)
![](https://img.shields.io/npm/v/react-native-optimized-flatlist.svg)

__Optimization for FlatLists. This is a fix over the FlatList that removed every item that is not inside the viewport. This will give a more stable and faster FlatList as performance dont drop! :)__

Please also read more about the issue here:
https://github.com/facebook/react-native/issues/13413

## Installation
```
npm i -S react-native-optimized-flatlist
```
or
```
yarn add react-native-optimized-flatlist
```


## Usage
Just replace `FlatList` with `OptimizedFlatList` .. thats all! :)

Replace this:
```js
render() {
  return (
  <FlatList
    data={[{name: 'fred', name: 'freddy'}]}
    renderItem={ ({item}) => <View>{item.name}</View>}
    />
...
```
With this:
```js
...
import {OptimizedFlatList} from 'react-native-optimized-flatlist'

...
render() {
  return (
  <OptimizedFlatList
    data={[{name: 'fred', name: 'freddy'}]}
    renderItem={ ({item}) => <View>{item.name}</View>}
    />
...

```
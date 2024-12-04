# React Native FlatList: Non-Unique Keys in keyExtractor

This repository demonstrates a common error in React Native's FlatList component: using a `keyExtractor` function that doesn't provide unique keys for each item. This leads to warnings and potential rendering problems.

## Problem
The `keyExtractor` function in `FlatList` must return a unique key for every item in the data array.  Failure to do so results in a warning and might cause incorrect rendering or unpredictable behavior. 

## Solution
The solution involves ensuring that the `keyExtractor` function generates a unique identifier for each item, even if the data itself contains duplicates.  This can be done using a unique identifier already present in the data or by generating a unique ID using methods like UUIDs.

## How to reproduce
1. Clone this repository.
2. Run `npm install`.
3. Run `npx react-native run-android` or `npx react-native run-ios`
4. Observe the warning in the console. 

## To fix the issue, refer to the corrected code in `bugSolution.js`.
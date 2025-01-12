# React Native FlatList: Inconsistent `keyExtractor`

This repository demonstrates a common bug in React Native's FlatList component: using an inconsistent or invalid `keyExtractor` function.  This can lead to unpredictable rendering, performance issues, and crashes.

The `FlatListBug.js` file shows the problematic code, using an `index` as the key, which is prone to issues when data changes.  `FlatListBugSolution.js` provides a corrected version using a unique identifier from the data itself as the key.

## How to reproduce

1. Clone this repository.
2. Run `npm install`
3. Run the app (using your preferred React Native environment).
4. Observe the incorrect rendering (in the `FlatListBug.js` example) and then correct rendering (in the `FlatListBugSolution.js` example). 

## Solution
Always ensure your `keyExtractor` function provides a unique, stable identifier for each item in your data array.  This should preferably be a unique ID associated with the data item rather than its index. 
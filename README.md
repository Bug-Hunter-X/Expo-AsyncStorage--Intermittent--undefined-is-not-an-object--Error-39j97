# Expo AsyncStorage Intermittent Error

This repository demonstrates a common, yet elusive, error encountered when using AsyncStorage within Expo applications. The error, "undefined is not an object (evaluating 'AsyncStorage.setItem')", manifests intermittently and is often difficult to debug due to its seemingly random nature. This is frequently caused by timing or race conditions in which a component attempts to use AsyncStorage before it's fully initialized.

## Reproducing the Issue

The `bug.js` file contains code that simulates this scenario. Running this code will likely (but not always) result in the error.  The frequency of the error may vary depending on the device and the speed of the device's hardware.

## Solution

The `bugSolution.js` file provides a solution to mitigate this issue. By utilizing promises and proper error handling, we can ensure that `AsyncStorage` is ready before attempting any operations.
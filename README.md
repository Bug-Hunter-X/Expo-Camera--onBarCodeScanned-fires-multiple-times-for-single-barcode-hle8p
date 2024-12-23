# Expo Camera: onBarCodeScanned Fires Multiple Times

This repository demonstrates a bug in the Expo Camera component where the `onBarCodeScanned` function fires multiple times for a single barcode scan. This can lead to unexpected behavior and errors in your application.

## Bug Description

The `onBarCodeScanned` callback is unexpectedly invoked multiple times for each barcode detected. This results in duplicated actions or unintended side effects in the application.

## Reproduction

1. Clone this repository.
2. Run `npm install` to install the necessary dependencies.
3. Run `expo start` to start the development server.
4. Scan a barcode with the app's camera.
5. Observe the console logs to see that the `onBarCodeScanned` function is called multiple times.

## Solution

The solution involves debouncing the `onBarCodeScanned` callback function to prevent multiple calls for a single scan event. See `bugSolution.js` for a working example.
# React useEffect Hook with Missing Dependency

This repository demonstrates a common error in React's `useEffect` hook: omitting dependencies from the dependency array.  This can lead to unexpected behavior and subtle bugs.

## The Problem

The provided `MyComponent` uses `useEffect` to log a message to the console whenever the component renders. However, the dependency array `[]` is empty. This means the effect will only run once after the initial render, regardless of changes to the component's state.

## The Solution

To fix this, include `count` in the dependency array. Now the effect will run whenever `count` changes, ensuring the log message reflects the current count.

## How to reproduce

1. Clone this repo.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.
4. Observe the console output and the behavior of the counter button. Note that the log is not updated after click the button in `bug.js` file
5. Compare the behavior and console logs between files `bug.js` and `bugSolution.js`
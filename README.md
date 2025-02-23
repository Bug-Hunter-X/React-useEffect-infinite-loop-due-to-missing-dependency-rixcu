# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook.  The bug stems from an incorrectly configured dependency array, leading to an infinite rendering loop.

## The Bug

The `bug.js` file contains a component that uses `useEffect` to log the current count to the console. However, the dependency array is missing the `count` variable, causing the effect to run after every render, regardless of whether the `count` value changes.

This creates an infinite loop, as the effect triggers a re-render, which triggers the effect again, and so on.

## The Solution

The `bugSolution.js` file provides the corrected code. By including `count` in the dependency array, the effect only runs when the `count` value changes, resolving the infinite loop.

## How to Reproduce

1. Clone this repository.
2. Navigate to the directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Observe the console output and the component behavior.  The `bug.js` version will cause an infinite loop and high CPU usage; the `bugSolution.js` version will function correctly.
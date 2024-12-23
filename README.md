# React useEffect Dependency Array Bug

This repository demonstrates a common error in React applications related to the `useEffect` hook's dependency array.

## The Problem

The `useEffect` hook is often used to perform side effects based on changes in state variables.  Forgetting to include all relevant state variables in the dependency array can lead to unexpected behavior or infinite render loops.

The `bug.js` file demonstrates this issue. The `useEffect` hook does not include `count` in the dependency array, causing it to run on every render, generating unwanted console output and potentially leading to performance issues or infinite loops in more complex scenarios.

## The Solution

The `bugSolution.js` file shows the corrected code.  By including `count` in the dependency array, the `useEffect` hook only runs when the value of `count` changes.

## How to reproduce the bug

1. Clone this repository.
2. Run `npm install`
3. Run `npm start`
4. Observe the console output and the button behavior in `bug.js`
5. Compare this behavior with `bugSolution.js`
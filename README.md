# Unnecessary Re-renders in React useEffect

This repository demonstrates a common React issue where the `useEffect` hook causes unnecessary re-renders due to missing dependencies in its dependency array. The `useEffect` hook should only run when specified dependencies change; otherwise, it leads to performance issues and unexpected behavior.

## Bug
The `bug.js` file contains a `MyComponent` that uses `useEffect` to log a message after each render.  However, the dependency array is missing the `count` state, leading to the effect running on every render instead of only when `count` changes.

## Solution
The `bugSolution.js` file demonstrates the correct implementation of `useEffect`. By including `count` in the dependency array, the effect now only runs when `count` changes.
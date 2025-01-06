# React 19 useEffect Dependency Array Bug

This repository demonstrates a common error in React 19's `useEffect` hook:  forgetting to include state variables in the dependency array. This leads to unexpected re-renders and potentially performance issues.

The `bug.js` file shows the incorrect implementation. The `bugSolution.js` file shows the corrected code.

## Bug
The initial code omits `count` from the dependency array of the `useEffect` hook.  This causes the effect to run on every render, regardless of whether `count` has actually changed.

## Solution
Adding `count` to the dependency array ensures the effect only runs when `count` changes, fixing the unexpected behavior and improving performance.
# React useEffect Hook Infinite Loop

This repository demonstrates a common error in React applications involving the `useEffect` hook.  The example showcases an infinite loop caused by omitting the dependency array in `useEffect`, leading to the effect running on every render and causing a performance bottleneck and potential crashes.

The `bug.js` file contains the erroneous code, while `bugSolution.js` provides the corrected version.

## Bug Description
The `useEffect` hook without a dependency array runs after every render.  In this case, it logs the current count, but the state update within `setCount` triggers a re-render, leading to a continuous loop.

## Solution
The corrected version uses a dependency array `[count]` to specify that the effect should only run when the value of `count` changes. This ensures the effect is triggered appropriately, resolving the infinite loop.
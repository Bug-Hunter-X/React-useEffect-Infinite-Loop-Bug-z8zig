# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications involving the `useEffect` hook. The bug is caused by an incorrect dependency array, leading to an infinite render loop.

## Bug Description

The `useEffect` hook is used to perform side effects after a component renders. In this example, the effect logs the current count to the console. However, the dependency array is missing `count`, causing the effect to run after every render, regardless of whether `count` has changed. This creates an infinite loop, as each log call triggers a re-render, which triggers the effect again, and so on.

## Solution

The solution is simple: add `count` to the dependency array. This ensures the effect runs only when the `count` value changes.  Check the `bugSolution.js` file to see the corrected code.
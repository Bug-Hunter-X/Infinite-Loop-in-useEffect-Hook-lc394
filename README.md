# React useEffect Hook Bug

This repository demonstrates a common bug in React's `useEffect` hook: an infinite loop caused by a missing dependency in the effect's dependency array. 

## Bug Description

The `MyComponent` component uses the `useEffect` hook to log a message to the console. However, because the dependency array is empty (`[]`), the effect runs after every render.  This leads to an infinite loop, as each log causes a re-render, triggering the effect again.

## Solution

The solution involves correctly specifying the dependencies in the useEffect hook's second argument.  If the effect depends on the `count` state variable, then it should be included in the dependency array.
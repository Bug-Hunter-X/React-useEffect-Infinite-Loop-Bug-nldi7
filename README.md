# React useEffect Infinite Loop Bug

This repository demonstrates a common React bug: an infinite loop caused by incorrect usage of the `useEffect` hook.  The `useEffect` hook's dependency array is incorrectly defined, leading to the component re-rendering constantly. 

The `bug.js` file contains the buggy code, and `bugSolution.js` demonstrates the corrected version.

## Bug Description
The issue arises from adding the `count` state variable to the dependency array of the `useEffect` hook.  Every time `count` changes (which is every render due to the `setCount` call), the `useEffect` runs again, which then changes `count` again, resulting in an infinite loop.
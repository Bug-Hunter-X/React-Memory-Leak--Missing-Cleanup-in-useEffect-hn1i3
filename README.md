# React Memory Leak Bug

This repository demonstrates a common React memory leak caused by forgetting to include a cleanup function in the `useEffect` hook.  The `useEffect` hook adds an event listener but fails to remove it when the component unmounts, leading to memory leaks.  The solution shows how to correctly implement the cleanup function to prevent this issue.

## Bug

The `bug.js` file contains a React component with an event listener added using `useEffect`.  However, it's missing the cleanup function that removes the listener when the component unmounts.

## Solution

The `bugSolution.js` file provides the corrected component with the cleanup function properly implemented. This prevents memory leaks by ensuring the event listener is removed when the component is no longer needed.
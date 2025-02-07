# React Native useEffect Async Operation Cleanup

This repository demonstrates a common error in React Native when using the `useEffect` hook with asynchronous operations.  The problem arises when a component unmounts before the asynchronous operation completes, leading to errors.  The solution involves proper cleanup within the `useEffect` hook to prevent these issues.

## Bug

The `bug.js` file contains the buggy code, showing an asynchronous operation within `useEffect` without proper cleanup.  This can result in errors like `TypeError: Cannot read properties of undefined (reading 'json')` if the component unmounts before the fetch completes.

## Solution

The `bugSolution.js` file provides the corrected code.  The solution uses the return value of `useEffect` to perform cleanup before the component unmounts, preventing errors and improving application stability.
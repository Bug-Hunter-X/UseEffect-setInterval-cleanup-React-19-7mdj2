# React 19 useEffect setInterval Cleanup
This repository demonstrates a common error in React 19 applications involving the `useEffect` hook and `setInterval`.  Specifically, it showcases how to properly handle cleanup for `setInterval` to avoid memory leaks.

The `bug.js` file contains the problematic code, while `bugSolution.js` provides the corrected version.

## Problem
The `setInterval` function is used within a `useEffect` hook without providing a cleanup function. This leads to the interval continuing indefinitely, even after the component unmounts.  This results in memory leaks, which becomes more critical in complex applications.

## Solution
The solution involves adding a cleanup function to the `useEffect` hook to explicitly clear the interval when the component unmounts.  This ensures that no unnecessary interval continues to run in the background.
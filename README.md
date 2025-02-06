# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React's `useEffect` hook: an infinite loop caused by missing dependencies.

The `bug.js` file contains the buggy code. The `bugSolution.js` file shows the corrected version.

## Problem
The original component uses `useEffect` without including `count` in the dependency array.  This leads to an infinite re-render cycle because every render triggers the effect, which changes `count`, leading to another render, and so on.

## Solution
The solution involves adding `count` to the dependency array. This ensures that the effect only runs when `count` changes.
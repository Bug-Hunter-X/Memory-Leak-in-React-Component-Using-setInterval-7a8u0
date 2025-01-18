# React setInterval Memory Leak

This repository demonstrates a common React bug: a memory leak caused by using `setInterval` within a `useEffect` hook without a cleanup function.  The `setInterval` continues running even after the component unmounts, leading to resource exhaustion.

## Bug
The `bug.js` file shows a component that increments a counter every second using `setInterval`.  The problem is that the interval is never stopped, causing a memory leak.

## Solution
The `bugSolution.js` file demonstrates the correct usage of `setInterval` within `useEffect` by including a cleanup function that uses `clearInterval` to stop the interval when the component unmounts.
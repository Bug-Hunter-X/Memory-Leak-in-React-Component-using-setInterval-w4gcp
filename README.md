# React setInterval Memory Leak
This example demonstrates a common error in React: using `setInterval` within a component's `useEffect` hook without proper cleanup. This leads to memory leaks and unexpected behavior.

## Problem
The `setInterval` function starts a timer that continues indefinitely.  Without a cleanup mechanism, when the component unmounts, the timer keeps running, leading to memory leaks and potential performance issues.

## Solution
The solution involves using the return value of `useEffect` to implement a cleanup function. This cleanup function stops the interval when the component unmounts.

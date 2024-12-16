# React: Memory Leak from setInterval in useEffect Hook

This repository demonstrates a common error in React applications involving the `setInterval` function within the `useEffect` hook.  The example component shows how neglecting to properly clean up the interval leads to memory leaks and unexpected behavior.

## Problem

The `setInterval` function, without a cleanup mechanism, creates an interval that continuously updates the state. This results in memory leaks and might cause performance issues. When the component unmounts, the interval keeps running in the background, consuming resources.

## Solution

The solution involves using the cleanup function provided by `useEffect` to `clearInterval` when the component unmounts. This ensures that the interval is stopped, freeing resources and preventing the memory leak.
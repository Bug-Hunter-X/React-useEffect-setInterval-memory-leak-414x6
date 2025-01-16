# React useEffect setInterval memory leak
This repository demonstrates a common mistake when using `setInterval` within a React component's `useEffect` hook.  The issue involves a memory leak because the interval continues to run even after the component is unmounted.  This can lead to unexpected behavior and performance problems.

## Bug Description
The `bug.js` file contains a React component that uses `setInterval` to update a counter every second.  However, it fails to clear the interval when the component is unmounted, causing a memory leak. 

## Solution
The `bugSolution.js` file shows the corrected version of the component. It uses the return value of `useEffect` to clear the interval before the component is unmounted, preventing the memory leak.
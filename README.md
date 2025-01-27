# React setInterval Memory Leak

This repository demonstrates a common error in React applications: using `setInterval` within `useEffect` without a cleanup function. This leads to memory leaks and unexpected behavior.

## Bug

The `bug.js` file contains a React component that uses `setInterval` to update a counter every second. However, it lacks a cleanup function to stop the interval when the component unmounts, resulting in a memory leak.

## Solution

The `bugSolution.js` file provides a corrected version that uses the return value of `useEffect` to implement a cleanup function. This ensures that the interval is cleared when the component is unmounted, preventing the memory leak.

## How to reproduce

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm start` to start the development server.
5. Open your browser and observe the counter.
6. Note that closing the browser tab doesn't stop the counter because of the memory leak in `bug.js`.
# React useEffect Infinite Loop Bug

This repository demonstrates a common bug in React applications: an infinite loop caused by incorrectly updating state within a useEffect hook's dependency array.

## The Bug

The `bug.js` file contains a component that attempts to increment a state variable within its `useEffect` hook.  The dependency array `[]` indicates that the effect should run only once after the initial render. However, updating the state inside the effect triggers a re-render, which, in turn, causes the effect to run again, leading to an infinite loop.

## The Solution

The `bugSolution.js` file provides a corrected version of the component.  The solution avoids the infinite loop by using the functional update approach or by removing the state update from the useEffect function if it is not necessary to update on every render.

## How to Reproduce

1. Clone this repository.
2. Run `npm install` to install dependencies.
3. Run `npm start` to start the development server.  Observe the error messages in the console if the bug is present.

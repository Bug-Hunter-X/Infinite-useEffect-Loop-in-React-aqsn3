# Infinite useEffect Loop in React

This repository demonstrates a common error in React applications: an infinite loop caused by the `useEffect` hook.  The `useEffect` hook, while powerful, can lead to performance problems if not used correctly.

## Problem

The provided `bug.js` file showcases a scenario where the `useEffect` hook runs after every render because it's missing a dependency array. This leads to an infinite loop, as the `console.log` continuously updates the console, impacting application performance and potentially causing it to crash.

## Solution

The `bugSolution.js` file demonstrates the correct way to use the `useEffect` hook. Adding an empty dependency array (`[]`) ensures that the effect runs only once after the initial render.
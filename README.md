# React useEffect Infinite Loop Bug

This repository demonstrates a common error in React applications where an infinite loop is created due to improper usage of the `useEffect` hook.

## Description

The `bug.js` file contains a component that attempts to update its internal state within the `useEffect` hook's callback function without proper dependency management.  This leads to an infinite loop, as each state update triggers a re-render, which then triggers the `useEffect` hook again, and so on.

## Solution

The `bugSolution.js` file provides the corrected code. The solution involves properly managing dependencies to avoid the infinite loop. By adding the `count` variable to the dependency array, useEffect will only run when the value of count changes, which is now controlled outside the useEffect.
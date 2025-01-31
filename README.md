# React useEffect Hook Missing Cleanup Function

This repository demonstrates a common but subtle error in React's `useEffect` hook: forgetting to include a cleanup function.

The `bug.js` file showcases the problematic code. The `useEffect` hook logs a message to the console when the component mounts, but it lacks a return statement to perform cleanup when the component unmounts.  This can lead to memory leaks if the effect has any side effects (e.g., setting intervals or event listeners).

The `bugSolution.js` file provides the corrected code with a proper cleanup function. This ensures that any side effects initiated by the effect are properly cleaned up when the component unmounts, preventing potential memory leaks.
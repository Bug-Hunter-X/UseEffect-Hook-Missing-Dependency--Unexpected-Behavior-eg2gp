# useEffect Hook Missing Dependency: Unexpected Behavior

This example demonstrates a common mistake when using the `useEffect` hook in React: omitting dependencies in the dependency array.  This can lead to unexpected re-renders and potentially subtle bugs that are difficult to track down.  The solution shows how to correctly specify dependencies to control when the effect runs.

## Bug

The provided `bug.js` shows a `useEffect` hook without a dependency array (`[]`). This causes the effect to run after every render, even though the intended behavior was to only run once on mount.

## Solution

The `bugSolution.js` file corrects this by adding an empty dependency array `[]` to ensure that the effect runs only once after the initial render. A cleanup function is also included to provide a controlled unmount scenario.


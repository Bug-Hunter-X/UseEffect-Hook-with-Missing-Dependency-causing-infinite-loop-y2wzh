# React useEffect Hook - Missing Dependency
This example demonstrates a common mistake when using the `useEffect` hook in React.  The `setInterval` function is called repeatedly due to a missing dependency in the effect's dependency array, causing an infinite loop.  The solution shows the correct way to add the dependency and prevent the infinite loop.

## Bug
The `bug.js` file contains the erroneous code that illustrates the incorrect usage of the `useEffect` hook. The `setInterval` function will run repeatedly, updating the state `count` every second, triggering a re-render and subsequently causing the effect to run again, creating an infinite loop. 

## Solution
The `bugSolution.js` file shows the corrected code. The `count` variable is added to the dependency array, causing the effect to only run when `count` changes, and then the interval is correctly cleared in the cleanup function.
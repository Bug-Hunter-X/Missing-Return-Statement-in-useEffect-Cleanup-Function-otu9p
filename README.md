# Missing Return Statement in React useEffect

This repository demonstrates a common error in React's `useEffect` hook: forgetting to include a return statement in the cleanup function.  This can lead to memory leaks and unexpected behavior if the component unmounts before the asynchronous operation completes.

## Bug

The `bug.js` file shows an example of an `useEffect` hook that fetches data from an API.  However, it's missing the necessary `return` statement in the cleanup function.  This means that any cleanup actions (like cancelling network requests or unsubscribing from events) won't be executed when the component unmounts.

## Solution

The `bugSolution.js` file provides the corrected code.  The `return` statement ensures that the cleanup function is properly executed when the component unmounts, preventing potential memory leaks.

## How to reproduce

1. Clone this repository.
2. Navigate to the project directory.
3. Run `npm install` to install the dependencies.
4. Run `npm start` to start the development server.  Observe the console for potential errors/warnings.

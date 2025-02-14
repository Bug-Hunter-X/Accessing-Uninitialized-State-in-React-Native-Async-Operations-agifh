# Accessing Uninitialized State in React Native Async Operations

This repository demonstrates a common error in React Native: attempting to access a state variable before it has been fully initialized. This often occurs when dealing with asynchronous operations like fetching data from an API.

## Problem

The code in `bug.js` shows how accessing `this.state.data.someProperty` before the `setState` call completes causes an error because `this.state.data` is initially `null`.

## Solution

The `bugSolution.js` file provides a solution using optional chaining (`?.`) and nullish coalescing (`??`) operators. This prevents errors by safely handling the case where `this.state.data` is null or undefined.
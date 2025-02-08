# Next.js 15 App Router: Race Condition with fetch in useEffect and Dynamic Routes

This repository demonstrates a potential race condition in Next.js 15's App Router when using `fetch` within a component's `useEffect` hook, particularly when dealing with dynamic routes. The issue arises from the asynchronous nature of data fetching and component re-rendering, leading to stale data or unexpected behavior.

## Problem

The `bug.js` file shows an example where fetching data for a dynamic route might return stale data if the component re-renders before the initial fetch completes. The race condition happens because the route changes faster than the data can be fetched.

## Solution

The `bugSolution.js` file offers a solution involving the use of the `use` hook for loading states and a more robust approach to handling the asynchronous data fetching to resolve the race condition.  This prevents rendering with stale data.
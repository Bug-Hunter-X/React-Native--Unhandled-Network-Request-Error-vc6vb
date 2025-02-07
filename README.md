# React Native Unhandled Network Request

This repository demonstrates a common error in React Native applications: improper error handling during network requests within the `useEffect` hook.  The `DataFetch.js` file contains the buggy code. The application crashes without informative feedback to the user when the network request fails. The solution is provided in `DataFetchSolution.js`.

## Problem

The original code lacks comprehensive error handling and loading state management.  If the network request fails, the application crashes instead of gracefully displaying an error message or loading indicator.

## Solution

The solution introduces a `try...catch` block to handle potential errors during the fetch call.  It also manages loading and error states using the `useState` hook. A loading indicator is shown while fetching data, and an error message is displayed if the request fails.
# React Router v6 Catch-All Route Issue

This repository demonstrates a common issue encountered when using catch-all routes (`/*`) in React Router v6. The problem is that the catch-all route doesn't seem to be catching unmatched routes, even when placed at the end of the route definitions.

The solution involves carefully examining the route order and ensuring that the catch-all route is indeed the last one defined. This ensures that it acts as the fallback for any unmatched paths.

## How to reproduce

1. Clone the repository
2. Run `npm install` to install the necessary dependencies.
3. Run `npm start` to start the development server.
4. Navigate to an invalid route, such as `/invalid`. You'll see that the NotFound component isn't rendering.
5. Review the `AppSolution.js` for the corrected implementation.

## Solution

The solution involves ensuring the catch-all route (`/*`) is the last route defined in the `Routes` component.  This is crucial for React Router to function correctly as the fallback route.
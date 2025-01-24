# React Router Catch-All Route Conflict

This repository demonstrates a common issue in React Router v6 where a catch-all route (`/*`) interferes with other, more specific routes.  The catch-all route, intended to handle 404 scenarios, incorrectly captures all requests, even those matching other defined routes.

## Problem

The provided `App.js` demonstrates this issue. Even though there are specific routes for `/` and `/about`, the catch-all route (`/*`) always matches, causing those specific routes to never render. 

## Solution

The solution in `AppSolution.js` demonstrates how to address this by carefully ordering routes.  By placing the catch-all route *last* in the `Routes` component, it only matches requests that don't match any of the more specific routes.
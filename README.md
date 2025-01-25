# React Router Dom Wildcard Route Issue

This repository demonstrates an uncommon bug in React Router Dom v6 related to the wildcard route (`/*`). The wildcard route is intended to act as a catch-all for any unmatched routes, rendering a 404 page. However, under certain circumstances, it fails to function as expected.

## Bug Description
The provided example shows that even with a wildcard route, React Router may render nothing if no other route matches, instead of rendering the NotFound component as expected. This is not consistent with the documentation and causes navigation problems.

## Solution
The solution involves careful route ordering. Placing the wildcard route (`/*`) at the end of the route definitions ensures that it's only considered after all other routes have been checked.  This is a crucial aspect of how React Router evaluates routes. 
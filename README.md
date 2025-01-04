# React Router Dom Wildcard Route Issue

This repository demonstrates an unexpected behavior in React Router Dom v6 when using the wildcard route (*) to handle 404 (Not Found) errors.  The wildcard route does not correctly catch routes that are not explicitly defined.

## Problem
The provided code uses a wildcard route ("*" ) to render a 404 component when no other route matches. However, even with this wildcard, navigation to an invalid route renders nothing. This is unexpected behavior in React Router v6.

## Solution
The solution involves ensuring that the wildcard route is placed as the last route in the Routes component. This guarantees that the wildcard only matches paths not matched by routes that are defined earlier in the Routes component.
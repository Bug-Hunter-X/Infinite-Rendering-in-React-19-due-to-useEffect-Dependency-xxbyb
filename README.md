# React 19 useEffect Dependency Issue

This repository demonstrates a common issue encountered when using the `useEffect` hook in React 19. The problem arises from an incorrect dependency array, leading to an infinite rendering loop. 

## Bug Description

The `MyComponent` attempts to log the current count in a `useEffect` hook. However, the `count` variable is not included in the dependency array, causing the effect to run on every render, which in turns updates the count, which causes another render. 

## Solution

The solution involves adding `count` to the dependency array of the `useEffect` hook. This ensures that the effect only runs when the `count` value changes.
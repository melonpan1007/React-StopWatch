# React StopWatch

A simple and stylish stopwatch component built with React.

## Features

- Start, stop, and reset the stopwatch
- Display elapsed time in minutes, seconds, and milliseconds
- Stylish UI with gradient backgrounds and animations
- Responsive design suitable for various screen sizes

## Installation

To use this component in your React application, follow these steps:

1. Save the following files into your `src/` folder in your React project directory:

   - `StopWatch.jsx`
   - `App.jsx`
   - `index.css`

2. Ensure you have React set up and configured in your project.

## Explanation

- **useRef**: 
  - `intervalIdRef` and `startTimeRef` are used to store the interval ID and start time respectively. These references are mutable and do not cause a re-render when changed. This helps in:
    - **Maintaining State Between Renders**: `useRef` allows you to persist values between renders without causing re-renders, which is efficient for keeping track of mutable values like the interval ID and start time.
    - **Accessing the Latest Values**: `useRef` ensures that you always have the most up-to-date values for `intervalIdRef` and `startTimeRef`, which is crucial for accurately calculating the elapsed time and managing the interval correctly.

- **useEffect**:
  - The `useEffect` hook is used to handle the interval setup and cleanup. It runs when `isRunning` changes, setting up the interval if the stopwatch is running and clearing it when it stops or the component unmounts. This helps in efficiently managing side effects in the component, ensuring that the interval is only active when needed and properly cleaned up to prevent memory leaks or unexpected behavior..
    
This setup ensures that the stopwatch updates accurately and efficiently without unnecessary re-renders.

## Difference between useEffect & useRef in simple words =>

**useRef**: Think of it as a piece of paper where you write down a value (like a phone number). You can look at it and change it, but the act of writing or changing the value on the paper doesn't affect anything else.

**useEffect**: Think of it as a to-do list that you follow after a certain event happens (like cleaning your room after you wake up). You follow the list when the event occurs, and you can update what’s on the list depending on different conditions (like cleaning your room only if it's a weekend).


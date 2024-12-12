# Clone the MovieLand

## Table of Contents

- [Purpose](#purpose)
- [What did i learn with this project?](#what-did-i-learn-with-this-project)
- [What is useEffect?](#what-is-useeffect)
- [What is useState?](#what-is-usestate)
- [Components](#components)
- [Used Programs](#used-program)
- [Reference](#reference)

## Purpose

[back](#table-of-contents)<br>

The primary objective of this project is to clone the MovieLand application created by JSMastery. This cloning exercise serves as a valuable learning experience for understanding fundamental React concepts, syntax, and the effective us of React hooks.

## What did I learn with this project?

[back](#table-of-contents)<br>

- Core React Concepts:
  - Component-Based Structure: Understanding how to break down a UI into reusable components for better organisation and maintainability.
  - State Management: Using the `useState` hook to mange and update the internal state of components, which is crucial for dynamic UIs.
  - Side Effects with useEffect: Learning how to handle side effects like API calls, DOM manipulations, and subscriptions using the `useEffect` hook.
  - JSX Syntax: Gaining familiarity with JSX, a syntax extension to JavaScript that allows you to write HTML-like code within JavaScript.
- React hooks
  - `useState`, `useEffect`
- Fetching Data
  - Learning how to fetch data from an external API (in this case, a movie API) using the `fetch` API and handle the asynchronous nature of network requests.

## What is useEffect?

[back](#table-of-contents)<br>

The `useEffect` hook provides a way to perform side effects within a React component. Side effects can include fetching data from an API, subscribing to events, or manipulating the DOM.

```jsx
import { useEffect } from 'react';

const App = () => {
  useEffect(() => {
    alert('Hello World');
  }, []);
};
```

> [!TIP]
>
> - The useEffect hook accepts a function as its first argument. This function will be executed after the component renders.
> - The optional second argument is an array of dependencies. If this array is empty (as in the example above), the effect will only run once after the initial render.
> - If the dependencies array includes any values that change, the effect will re-run.

## What is useState?

[back](#table-of-contents)<br>

The useState hook allows you to manage and update the state of a component. It takes an initial value as an argument and returns a pair:

```jsx
import { useState } from 'react';

const App = () => {
  const [movies, setMovies] = useState([]);
  const [searchTerm, setSearchTerm] = useState('');

  const searchMovies = async (title) => {
    const response = await fetch(`${API_KEY}&s=${title}`);
    const data = await response.json();

    setMovies(data.Search);
  };
};
```

> [!TIP]
>
> - State values cannot be directly modified. You must use the provided setter function (e.g., setMovies) to update them.
> - When the state value changes, the component will re-render, causing the UI to reflect the updated data.

## Components

[back](#table-of-contents)<br>

In React, components are reusable building blocks that encapsulate UI logic and presentation. They can be either functional components (as shown in the examples above) or class components.

> [!NOTE]
> This line of code renders a custom `MovieCard` component, which would typically be defined in a separate file.

```jsx
<MovieCard />
```

## Used Program

[back](#table-of-contents)<br>

### React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

## Reference

[back](#table-of-contents)<br>

[JSMastery](https://www.jsmastery.pro)

<a href="https://www.youtube.com/watch?v=b9eMGE7QtTk">
<img src="https://i.ytimg.com/vi/b9eMGE7QtTk/hqdefault.jpg?sqp=-oaymwEjCNACELwBSFryq4qpAxUIARUAAAAAGAElAADIQj0AgKJDeAE=&rs=AOn4CLBUcwkw56zQweD5FMcIeRDWLKpqgQ" alt="React JS Crash Course"></a>

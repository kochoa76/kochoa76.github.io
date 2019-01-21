---
layout: post
title:      "React Hooks "
date:       2019-01-21 04:09:00 +0000
permalink:  react_hooks
---

This week I attended a React meetup where the presenter introduced what was to come in React, with an emphasis on lifecycle hooks. Here was a bit of what we reviewed in the meetup and what's to come with React. 

**What is a hook?**

Hooks are functions that let you “hook into” React state and lifecycle features from function components. Hooks don’t work inside classes — they let you use React without classes. 

React provides a few built-in Hooks like useState. You can also create your own Hooks to reuse stateful behavior between different components. We’ll look at the built-in Hooks first.

Let's go through a few built in Hooks React provides us with. 

Rules of Hooks: 

1. Only call Hooks at the top level. Don’t call Hooks inside loops, conditions, or nested functions.
2. Only call Hooks from React function components. Don’t call Hooks from regular JavaScript functions. 

**Commonly Used Built In Hooks -- useState, useEffect, useContext **

The Effect Hook, useEffect, adds the ability to perform side effects from a function component. It serves the same purpose as componentDidMount, componentDidUpdate, and componentWillUnmount in React classes, but unified into a single API.

```
import { useState, useEffect } from 'react';

function Example() {
  const [count, setCount] = useState(0);

  // Similar to componentDidMount and componentDidUpdate:
  useEffect(() => {
    // Update the document title using the browser API
    document.title = `You clicked ${count} times`;
  });

  return (
    <div>
      <p>You clicked {count} times</p>
      <button onClick={() => setCount(count + 1)}>
        Click me
      </button>
    </div>
  );
}
```

Here, useState is a Hook. We call it inside a function component to add some local state to it. React will preserve this state between re-renders. useState returns a pair: the current state value and a function that lets you update it. You can call this function from an event handler or somewhere else. It’s similar to this.setState in a class, except it doesn’t merge the old and new state together. Here count will increment.

The Effect Hook, useEffect, adds the ability to perform side effects (data fetching) from a function component. It serves the same purpose as componentDidMount, componentDidUpdate, and componentWillUnmount in React classes, but unified into a single API. 

When you call useEffect, you’re telling React to run your “effect” function after flushing changes to the DOM. Effects are declared inside the component so they have access to its props and state. By default, React runs the effects after every render — including the first render.

The other more commonly used hook is useContext. 
```
const context = useContext(Context);

```

Accepts a context object (the value returned from React.createContext) and returns the current context value, as given by the nearest context provider for the given context.

When the provider updates, this Hook will trigger a rerender with the latest context value.


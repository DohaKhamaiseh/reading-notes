## What is React Context, and how does it help in managing state and data sharing in a React application?

### What?
*React context allows us to pass down and use (consume) data in whatever component we need in our React app without using props.*

### How?

*React context helps us avoid the problem of props drilling.*

*Props drilling is a term to describe when you pass props down multiple levels to a nested component, through components that don't need it.*


## Explain the useContext Hook and how it can be used to access data from a React Context within a functional component.


*Instead of using render props, we can pass the entire context object to React.useContext() to consume context at the top of our component.*

   

```
import React from 'react';

export const UserContext = React.createContext();

export default function App() {
  return (
    <UserContext.Provider value="Reed">
      <User />
    </UserContext.Provider>
  )
}

function User() {
  const value = React.useContext(UserContext);  
    
  return <h1>{value}</h1>;
}
```

## Describe the purpose of Next.js, and provide an example from the Vercel Next.js Examples reading on how it can be used to build a scalable web application.

### Purpose:

**1. Universal Server-Rendered React Apps:** Next.js allows us to build server-rendered React applications with no configuration. This means that our web application can render on the server first, then continue rendering on the client side. This improves performance.

**2. Static Site Generation (SSG):** With Next.js, we can generate static websites from dynamic datasets at build time. This makes Next.js a great tool for blog posts, product pages, and more.

**3. Simplified Data Fetching:** Next.js provides a simple and consistent method to fetch data for our components before rendering.

### Example:
**Blog :** 

This portfolio is built with Next.js and a library called Nextra. It allows you to write Markdown and focus on the content of your portfolio. This starter includes:

Automatically configured to handle Markdown/MDX
Generates an RSS feed based on your posts
A beautiful theme included out of the box
Easily categorize posts with tags
Fast, optimized web font loading

https://demo.vercel.blog






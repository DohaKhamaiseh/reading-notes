## Explain the concept of dynamic routes in Next.js and how they differ from static routes.

Dynamic routes are used when we want to serve different content for different paths, but the exact paths are not known in advance and depend on data. Dynamic routing allows us to map an unknown number of paths to a single page component.

In Next.js, we can create a dynamic route by adding brackets [] to a page name in the pages directory. For example, a file named pages/posts/[id].js matches any route like /posts/1, /posts/abc, etc.

Inside our page component, we can access the dynamic part of the route (in this case the id) using the useRouter hook provided by Next.js.

**Static routes** are straightforward and always render the same content for a specific URL. They are ideal for pages where the content is not dependent on specific path parameters, like an About page or a Contact page.

**Dynamic routes** allow for flexibility in handling various URL patterns with a single page component. They are useful when we want to create pages based on data that might not be available at the time of writing our code, such as blog posts.

## Describe the process of deploying a Next.js application. What are the key steps involved, and what are some deployment platforms you can use?

1. Build your Next.js Application
2. Add a start script
3. Choose a Platform(Vercel, Netlify, Heroku, ...)
4. Configure and Deploy
5. Set up Continuous Deployment
   


## How does Next.js handle static file serving? Discuss the default folder structure for storing static assets and explain how to reference them in a Next.js application.

The default folder for storing static assets in Next.js is the **public** directory at the root of our project. Anything we put in the public directory will be accessible by our application from the root URL /.

For instance, if we have an image named logo.png in our public directory, it will be available in our application at /logo.png. Similarly, if we create a subfolder called images in the public directory and add a file named Image.jpg, we can access it in our application at /images/Image.jpg.

```
function Testcomponant() {
  return (
    <div>
      <img src="/images/Image.jpg" alt="Image" />
    </div>
  );
}
```




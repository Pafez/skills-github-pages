---
title: "First-Blogpost"
date: 2026-09-04
---

# Why I Switched from React to Next.js in 2026

When I first started building web applications, a standard Vite + React setup was my go-to choice. It was lightweight, unopinionated, and easy to reason about. However, as my applications grew, I kept hitting the same walls: complex client-side routing, massive bundle sizes, and slow initial page loads. 

That is why I finally migrated my portfolio and side projects to **Next.js**. Here is a quick breakdown of what changed for the better.

---

## ⚡ The Big Wins

* **Server Components:** Fetching data directly on the server means less loading spinners and a much faster time-to-interactive for users.
* **Built-in Routing:** No more configuring `react-router-dom`. Creating a new folder inside the `app/` directory handles everything automatically.
* **Automatic SEO optimization:** Next.js generates static HTML out of the box, making it highly readable for search engine web crawlers.

---

## 🛠️ Code Comparison: Data Fetching

In vanilla React, fetching data usually requires a mix of `useState` and `useEffect` hooks:

```javascript
// The Old Way (Client-Side)
useEffect(() => {
  fetch('/api/data')
    .then(res => res.json())
    .then(data => setData(data));
}, []);
```

With Next.js Server Components, you can fetch data directly inside an `async` function, treating your component like standard backend code:

```javascript
// The Next.js Way (Server-Side)
const res = await fetch('https://data.com');
const data = await res.json();
```

---

## 💡 Final Thought

While raw React is still fantastic for heavily dynamic, authenticated dashboards, a framework like Next.js makes building public-facing websites, blogs, and marketing pages significantly faster and more performant. 

> "Choosing the right tool isn't about finding the 'best' framework—it is about finding the one that removes the most friction from your workflow."

---

### 💬 What do you think?
Are you still using standard React, or have you migrated to a meta-framework? Let's discuss in the comments below or reach out to me on [Twitter](https://x.com)!

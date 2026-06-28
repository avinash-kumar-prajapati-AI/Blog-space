---
id: "eng-001"
title: "Build a REST API with Node.js and Express"
description: "A beginner-friendly guide to building your first REST API using Node.js and Express. Covers routing, middleware, and JSON responses."
tags: ["nodejs", "express", "rest-api", "backend", "javascript", "web-development"]
category: "engineering"
modified_date: "2025-06-01"
thumbnail: "media/images/articles/build-a-rest-api-with-nodejs/thumbnail.png"
external_links:
  - label: "Visit Product"
    url: "https://github.com/avinash-kumar-prajapati/rest-api-demo"
draft: false
---

## Introduction

REST APIs are the backbone of modern web applications. In this article, we'll build a simple but complete REST API using **Node.js** and **Express**.

## Prerequisites

- Basic JavaScript knowledge
- Node.js installed on your machine
- A code editor (VS Code recommended)

## Setting Up the Project

Create a new folder and initialize your project:

```bash
mkdir my-api
cd my-api
npm init -y
npm install express
```

## Creating the Server

Create `index.js`:

```js
const express = require('express');
const app = express();

app.use(express.json());

const posts = [
  { id: 1, title: "Hello World", body: "My first post" },
  { id: 2, title: "Second Post", body: "Another post" }
];

app.get('/posts', (req, res) => {
  res.json(posts);
});

app.get('/posts/:id', (req, res) => {
  const post = posts.find(p => p.id === parseInt(req.params.id));
  if (!post) return res.status(404).json({ error: 'Not found' });
  res.json(post);
});

app.post('/posts', (req, res) => {
  const post = { id: posts.length + 1, ...req.body };
  posts.push(post);
  res.status(201).json(post);
});

app.listen(3000, () => console.log('Server running on port 3000'));
```

## Testing the API

Run the server:

```bash
node index.js
```

Test with curl:

```bash
curl http://localhost:3000/posts
curl http://localhost:3000/posts/1
```

## Conclusion

You now have a working REST API. Next steps: add a database like MongoDB or PostgreSQL, add authentication, and deploy to a cloud platform.

---

*Share this article if it helped you!*

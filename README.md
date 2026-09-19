# Express Store

A small e-commerce-style web app built with Express and Pug: user registration/login (session-based), a product catalog with add/edit/delete, and a shopping cart stored in a cookie.

**Stack:** Node.js · Express · MongoDB (Mongoose) · Pug templates · express-session

## Running

```bash
npm install
npm start
```

Requires a local MongoDB instance (connection is configured for the default local URI).

## Features

- User registration and login (session-based auth)
- Product listing, add, and edit (behind a login check)
- Shopping cart (cookie-based)

## Structure

```
routes/        index, products, users route handlers
models/        Mongoose models (product, user)
middlewares/   session auth checks
views/         Pug templates (products, cart, users, layout)
```

## Note

Passwords are currently compared in plain text against the database. If you revisit this project, swapping in `bcrypt` for password hashing would be the first thing to fix before treating it as production-style code.

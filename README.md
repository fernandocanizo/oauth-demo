# oauth-demo

A Node.js + Express.js server with OAuth demo

## It's a demo!

Of course end-points don't make any sense and it's stupid to change your own role, but this is just a minimum project to show OAuth working.

## API

- GET /
  Landing page explaining demo API (which may prove this README section redundant)
  _public access_

- GET /register
  Lets you register via Google OAuth
  _public access_

- GET /login
  Lets you authenticate via Google OAuth
  _public access_

- GET /user
  Lists users (no pagination as this demo is not meant to register many users)
  _only logged in users_ (authentication example)

- PATCH /user/:id
  payload:
  ```json
  {
    "role": "admin"
  }
  ```
  _only logged in users_ (authentication example)

- GET /role
  Lists roles
  _only logged in users with role "admin"_ (authorization example)

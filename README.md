# [Flask React Berry Dashboard](https://appseed.us/product/flask-react-berry-dashboard)

**Berry** is a creative **React Dashboard** built using the Material-UI. It is meant to be the best User Experience with highly customizable feature-riched pages. It is a complete game-changer **React Dashboard** with an easy and intuitive responsive design as on retina screens or laptops. The product comes with a simple JWT authentication flow: login/register/logout. 

> Features

- Innovative **Material UI** Design - Creafted by [CodedThemes](https://bit.ly/37fF9RT)
- React, Redux, Redux-persist
- Authentication: JWT Login/Register/Logout
- **Full-stack Ready** using a **Flask API Server** (open-source project) - Server Features
  - Flask / Flask-RestX / SQLite3 - a simple, easy to use backend
  - Authentication with JWT (login, logout, register)
  - Docker, Unitary tests

> Links

- [Flask React Berry Dashboard](https://appseed.us/product/flask-react-berry-dashboard) - product page
- [Flask React Berry Dashboard](https://flask-react-berry-dashboard.appseed-srv1.com/) - LIVE Demo
- Free Support via Github (issues tracker) and [Discord](https://discord.gg/fZC6hup).

<br />

## Quick-start in Docker

> Clone/Download the source code

```bash
$ git clone  https://github.com/app-generator/flask-react-berry-dashboard.git
```

<br />

> Start the Flask API

```bash
$ cd flask-api
$ docker-compose pull   # download dependencies 
$ docker-compose build  # local set up
$ docker-compose up     # start the app 
```

At this point, the API should be up & running at `http://localhost:5000`, and we can test the interface using POSTMAN or `curl`.

<br />

> Start the React UI (using another terminal)

```bash
$ cd react-ui
$ docker-compose pull   # download dependencies 
$ docker-compose build  # local set up
$ docker-compose up     # start the app 
```

Once all the above commands are executed, the `React UI` should be visible in the browser. By default, the app redirects the guest users to authenticate. 
After we register a new user and Sign IN, all the private pages become accessible. 

<br />

![Flask React Berry Dashboard - Open-source full-stack product with Flask API Backend.](https://user-images.githubusercontent.com/51070104/142403839-1488457d-0ea6-4b18-8f25-d19a9acf101e.gif)

<br >

## General Information

The product is built using a `two-tier` pattern where the React frontend is decoupled logically and physically from the API backend. How to use the product: 

- `Compile and start` the **Flask API Backend**
  - by default the server starts on port `5000`
- `Compile and start` the **React UI**
  - UI will start on port `3000` and expects a running backend on port `5000`
- `Configuration` (Optional)
  - Change the API port
  - Configure the API port used by the React UI to communicate with the backend 

<br />

## Manual build

### Start the Flask API 

```bash
$ cd flask-api
$ 
$ # Create a virtual environment
$ virtualenv env
$ source env/bin/activate
$
$ # Install modules
$ pip install -r requirements.txt
$
$ # Set up the environment
$ export FLASK_APP=run.py
$ export FLASK_ENV=development
$ 
$ # Start the API
$ flask run
```

<br />

### Compile & start the React UI

```bash
$ cd react-ui
$
$ # Install Modules
$ yarn
$
$ # Start for development (LIVE Reload)
$ yarn start 
```

<br />

### Configuration (Optional)

> Change the port exposed by the Flask API

```bash
$ flask run --port=5001
```

Now, the API starts on port `5001`. 

<br />

> Update the API port used by the React Frontend

**API Server URL** - `src/config.js` 

```javascript
const config = {
    ...
    API_SERVER: 'http://localhost:5000/api/'  // <-- The magic line
};
```

<br />

## API

For a fast set up, use this POSTMAN file: [api_sample](https://github.com/app-generator/api-server-unified/blob/main/api.postman_collection.json)

> **Register** - `api/users/register` (**POST** request)

```
POST api/users/register
Content-Type: application/json

{
    "username":"test",
    "password":"pass", 
    "email":"test@appseed.us"
}
```

<br />

> **Login** - `api/users/login` (**POST** request)

```
POST /api/users/login
Content-Type: application/json

{
    "password":"pass", 
    "email":"test@appseed.us"
}
```

<br />

> **Logout** - `api/users/logout` (**POST** request)

```
POST api/users/logout
Content-Type: application/json
authorization: JWT_TOKEN (returned by Login request)

{
    "token":"JWT_TOKEN"
}
```

<br />

## Product UI

> **Flask React Berry Dashboard** - Login 

![Flask React Berry Dashboard - Login.](https://user-images.githubusercontent.com/51070104/142403942-3a2228e6-c769-4259-8e78-c000056db7c4.png)

<br />

> **Flask React Berry Dashboard** - User Profile

![Flask React Berry Dashboard - User Profile](https://user-images.githubusercontent.com/51070104/142403992-81e86dc5-4d73-4cca-8a1b-300a0f5475a0.png)

<br />

> **Flask React Berry Dashboard** - Billing Page

![Flask React Berry Dashboard - Billing Page.](https://user-images.githubusercontent.com/51070104/142404073-68b96008-fb06-4ff5-98cf-c8e3eca636c9.png)

<br />

## Links & Resources

- Ask for [Support](https://appseed.us/support) on [Discord](https://discord.gg/fZC6hup)
- See for [React Starters](https://appseed.us/apps/react) - index provided by AppSeed

<br />

---
**[Flask React Berry Dashboard](https://appseed.us/product/flask-react-berry-dashboard)** - Full-Stack seed project provided by **AppSeed [App Generator](https://appseed.us/)**

# ePharma-frontend

This is the frontend of ePharma E-commerce website project.

### Tech Used

- [ReactJS]
- [node.js]
- [Stripe]

### How to clone and run this project to your system.

```sh
$ git clone origin git@github.com:skzaffarekbal/ePharma-frontend.git
$ cd ePharma-frontend
$ npm install
$ node app.js
```

### This project has .env file for Environment Variable.

```
REACT_APP_BACKEND=<--Backend URL-->/api
REACT_APP_STRIPEPK="<--Stripe Public Key-->"
```

> This project use stripe as payment gateway so you have to use it's Public key which is present in your [Stripe] dashboard.
> Make a .env file to declare all the above environment variabale.

[reactjs]: https://reactjs.org/
[node.js]: http://nodejs.org
[stripe]: https://www.npmjs.com/package/stripe

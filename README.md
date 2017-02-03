This project was bootstrapped with [Create React App](https://github.com/facebookincubator/create-react-app) and [CRAFT](https://github.com/stoyan/craft).

---

If you are interested in this template - let me know - tweet me [@tuchk4](https://twitter.com/tuchk4) or [file an issue](https://github.com/tuchk4/craft-redux/issues/new) here.

I will add more features and tests.

---

```
npm -g -g craftool
craft MyAppRedux https://github.com/tuchk4/craft-redux/archive/master.zip
```

## General Resources

Please read official Create React App guide and don't try to customize configs because I am sure that all your requirements are reachable in 100% without config customizing or ejecting.

<img src="http://i.imgur.com/ULoeOL4.png" height="16"/> [Why I love Create React App and don't want to eject](https://medium.com/@valeriy.sorokobatko/why-i-love-create-react-app-e63b1be689a3)

* [Create React App GitHub](https://github.com/facebookincubator/create-react-app)
* [User Guide](https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md)
* [Awesome Create React App](https://github.com/tuchk4/awesome-create-react-app)
* [Redux](http://redux.js.org/)
* [React Router](https://reacttraining.com/react-router/)
* [Reselect](https://github.com/reactjs/reselect)

### Redux

* [Redux Logger](https://github.com/evgenyrodionov/redux-logger)
* [Redux Thunk](https://github.com/gaearon/redux-thunk)
* compose with [Redux Chrome extension](https://github.com/zalmoxisus/redux-devtools-extension) for development env.

> [Displaying Map in state #124](https://github.com/zalmoxisus/redux-devtools-extension/issues/124)

>  Import [`set.prototype.tojson`](https://www.npmjs.com/package/set.prototype.tojson) and [`map.prototype.tojson`](https://www.npmjs.com/package/map.prototype.tojson) for correct view of [`Map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Map) and [`Set`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Set) structures at Redux Chrome extension.

---

App | Redux Chrome dev tools
----|---
![CRAFT Redux Screenshot](https://monosnap.com/file/X5rD3u7mubxRHpufXzIACNhzk5zVEs.png) | ![Alt text](https://monosnap.com/file/UWm0dSNy1zhO1dfey7kHtiezhPaZKk.png)

### `npm start`

Runs the app in development mode.<br>
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br>
You will see the build errors and lint warnings in the console.

<img src='https://camo.githubusercontent.com/41678b3254cf583d3186c365528553c7ada53c6e/687474703a2f2f692e696d6775722e636f6d2f466e4c566677362e706e67' width='600' alt='Build errors'>

### `npm test`

Runs the test watcher in an interactive mode.<br>
By default, runs tests related to files changes since the last commit.

[Read more about testing.](https://github.com/facebookincubator/create-react-app/blob/master/packages/react-scripts/template/README.md#running-tests)

### `npm run build`

Builds the app for production to the `build` folder.<br>
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br>
Your app is ready to be deployed!


---

## Troubleshooting

### `scripts/*-env.js`

We need this script because we can not run this

```
{
  "scripts": {
    "test": "node -r dotenv/config ./node_modules/.bin/react-scripts test dotenv_config_path=development.env",    
  }
}
```

Because `jest` will accept `dotenv_config_path=development.env` as [regex for test files](https://facebook.github.io/jest/docs/cli.html#jest-regexfortestfiles).

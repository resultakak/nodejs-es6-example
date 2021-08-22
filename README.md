# Nodejs ES6 Example

```bash
npm init

touch sum.js index.js

npm install --save-dev @babel/core @babel/cli @babel/preset-env @babel/node

npm i --save-dev nodemon

touch .babelrc
```

```json
// .babelrc
{
  "presets": [
    "@babel/preset-env"
  ]
}
```

```javascript
//sum.js

function add(a, b) { 
  return a + b;
}

export default add; // ES6 export
```

```javascript
//index.js

import add from "./sum"; //ES6 import

console.log(add(3, 4)); //This should print 7 in the console
```

```json
// package.json
"scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "start": "nodemon --exec node_modules/.bin/babel-node index.js"
  }
```

```bash
npm start
```

> https://docs.github.com/en/actions/guides/publishing-nodejs-packages
> https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-npm-registry

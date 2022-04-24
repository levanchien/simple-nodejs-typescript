### Basic

`typescript`
get access to the command line TypeScript compiler through the `tsc` command

`@types/node`
contains type definitions for Node.js
get type safety and auto-completion on the Node apis like file, path, process, etc

`tsconfig.json`
define the TypeScript compiler options

`npx`
the Node package executer

`npx tsc`
read the tsconfig.json, apply the configuration against the TypeScript compiler to generate the compiled JavaScript code

`ts-node`
for running TypeScript code directly without having to wait for it be compiled

`nodemon`
 to watch for changes to our code and automatically restart when a file is changed

 `nodemon.json`
 ```js
 {
  "watch": ["src"],
  "ext": ".ts,.js",
  "ignore": [],
  "exec": "ts-node ./src/index.ts"
}
```

`rimraf`
a cross-platform tool that acts like the rm -rf

`npm run start:dev`
Starts the application in development using nodemon and ts-node to do cold reloading.

`npm run build`
Builds the app at build, cleaning the folder first.

`npm run start`
Starts the app in production by first building the project with npm run build, and then executing the compiled JavaScript at build/index.js.

==========================================

### ESLint

- ESLint is a JavaScript linter that enables you to enforce a set of style, formatting, and coding standards for your codebase
- It looks at your code, and tells you when you're not following the standard that you set in place

`npm install --save-dev eslint @typescript-eslint/parser @typescript-eslint/eslint-plugin`
Install all packages

`.eslintrc`
Eslint configuration file

`.eslintignore`
Ignoring files we don't want to lint

`"lint": "eslint . --ext .ts"` & `npm run lint`
It looks at your code, and tells you when you're not following the standard that you set in place

`"rules": { }`
*disallow* statements in our code
- "off" means 0
- "warn" means 1
- "error" means 2
Ex: *disallow* `console.log`
```js
"rules": { 
    "no-console": 1 
  }
```
`Adding a plugin (features)`
Ex: [no-loops](https://github.com/buildo/eslint-plugin-no-loops) - *Disallow* use of loops (for, for-in, while, do-while, for-of)
```js
"rules": {
    ...,
    "no-loops/no-loops": 2
  }
```

`Extending a different base config`
```js
"extends": [
    "plugin:shopify/esnext"
  ],
```

`"lint-and-fix": "eslint . --ext .ts --fix"`
tell Eslint to fix things that it's able to fix at the same time.
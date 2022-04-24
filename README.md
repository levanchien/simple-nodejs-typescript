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
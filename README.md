ecma-script-module-design
# ECMA Script Module Design

Based on "ES modules: A cartoon deep-dive" at https://hacks.mozilla.org/2018/03/es-modules-a-cartoon-deep-dive/

## 100 - Introduction

Based on "CommonJS vs. ES Modules: Modules and Imports in NodeJS" at https://reflectoring.io/nodejs-modules-imports/

*CommonJS*: The Default NodeJS Module System has been CommonJS

**Importing** modules with CommonJS:

```
const foo = require("foo"); // a node module, found in node_modules
const dow = require("./dow"); // a local file, dow.js
```
or importing only specific functions:
```
const * as foo = require("foo"); // a node module, found in node_modules
const { dow } = require("./dow"); // a local file, dow.js
```

We can also import variables and/or classes:

```
const Logger = require("./logger");

Logger.info(`${logger.defaultMessage} printed in blue`);
Logger.error("some error message printed in red");
```

**Exporting** modules with CommonJS:

```
exports.foo = function (bar) {
  console.log(bar);
};
```
or when using arrow functions:
```
exports.foo = (bar) => {
  console.log(bar);
};
```
or using module.exports:
```
function internalFoo(bar) {
  console.log(bar);
}

module.exports {
    foo: internalFoo,
    ...
};
```

We can also export variables and/or classes:

```
const defaultMessage = "Hello World";

class Logger {
  static defaultMessage = "Hello World";

  static info(message) {
    console.log(chalk.blue(message));
  }

  static error(message) {
    console.log(chalk.red(message));
  }
}

module.exports = {
  Logger,
  defaultMessage
};
```

**THE BETTER WAY IS USING ES MODULES**

*ES Module*: 


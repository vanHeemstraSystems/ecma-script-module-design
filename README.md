ecma-script-module-design
# ECMA Script Module Design

Based on "ES modules: A cartoon deep-dive" at https://hacks.mozilla.org/2018/03/es-modules-a-cartoon-deep-dive/

## 100 - Introduction

Based on "CommonJS vs. ES Modules: Modules and Imports in NodeJS" at https://reflectoring.io/nodejs-modules-imports/

*CommonJS*: The Default NodeJS Module System has been CommonJS

Importing modules with CommonJS:

```
const foo = require("foo");
```

Exporting modules with CommonJS:

```
exports.foo = function (bar) {
    console.log(bar);
};
```

**THE BETTER WAY IS USING ES MODULES**

*ES Module*: 


# Common Module Definition / draft

------

This specification addresses how modules should be written in order to be interoperable in **browser-based** environment. By implication, this specification defines the minimum features that a module system must provide in order to support interoperable modules.

* Modules are singletons.
* New free variables within the module scope should not be introduced.
* Execution must be lazy.

## 模块定义

A module is defined with `define` keyword, which is a function.

```js
define(factory);
```

1. The `define` function accepts a single argument, the module factory.
2. The `factory` may be a function or other valid values.
3. If `factory` is a function, the first three parameters of the function, if specified, must be "require","exports", and "module", in that order.

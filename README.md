# Abitbol

[![Lint and Test](https://github.com/wanadev/abitbol/actions/workflows/node-ci.yml/badge.svg)](https://github.com/wanadev/abitbol/actions/workflows/node-ci.yml)
[![NPM Version](http://img.shields.io/npm/v/abitbol.svg?style=flat)](https://www.npmjs.com/package/abitbol)
[![License](http://img.shields.io/npm/l/abitbol.svg?style=flat)](https://github.com/wanadev/abitbol/blob/master/LICENSE)
[![Discord](https://img.shields.io/badge/chat-Discord-8c9eff?logo=discord&logoColor=ffffff)](https://discord.gg/BmUkEdMuFp)


Abitbol is a small Javascript library that provides consistent/easy to use
classes for Node.js and web browsers. It is heavily inspired by  Armin
Ronacher's [Classy][] library, but extends its possibilities.

**Features:**

* Simple inheritance
* Consistent `this` (always points to the current instance)
* Annotations
* Computed properties automatically generated from getters and setters
* Simple way to call a super class method
* Simple way to declare static properties
* Handful mixin

**Exemple class definition:**

```javascript
var Vehicle = Class.$extend({

    __init__: function(color) {
        this.color = color;
        this.speed = 0;
    },

    move: function(speed) {
        this.speed = speed;
    },

    stop: function() {
        this.speed = 0;
    }

});
```

![George Abitbol](./doc/images/george-abitbol.jpg)

> The classiest javascript class library of the world<br />
> -- George Abitbol


## Documentation

* https://wanadev.github.io/abitbol/


## Changelog

* **2.1.0:** Added TypeScript type definitions (@jbghoul, #26)
* **2.0.1:** Optimization of special properties detection (@jbghoul, #23)
* **2.0.0:** New pre/post build hooks that allows to implement new patterns on
  Abitbol Classes.
* **1.2.0:** Support static method/properties in mixin
* **1.1.1**: Updates doc and README
* **1.1.0**: Adds ES2015 support in the annotation parser
* **1.0.4**: Updates dependencies
* **1.0.3**: Allows computed properties' accessors and mutators to be
  monkey-patched.
* **1.0.2**: Do not wrap methods when it is not necessary.
* **1.0.1**: Fixes context issue with nested method calls.
* **1.0.0**: Computed properties generated from accessors and mutators
  (get/set), annotations, proper `this`.
* **0.1.0**: Equivalent to Classy (except `Class.$classyVersion`,
  `Class.$withData()`, `Class.$noConflict()` that are not implemented).


[Classy]: https://github.com/mitsuhiko/classy
[dl-zip]: https://github.com/wanadev/abitbol/archive/master.zip

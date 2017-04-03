# api documentation for  [traverse (v0.6.6)](https://github.com/substack/js-traverse)  [![npm package](https://img.shields.io/npm/v/npmdoc-traverse.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-traverse) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-traverse.svg)](https://travis-ci.org/npmdoc/node-npmdoc-traverse)
#### traverse and transform objects by visiting every node on a recursive walk

[![NPM](https://nodei.co/npm/traverse.png?downloads=true)](https://www.npmjs.com/package/traverse)

[![apidoc](https://npmdoc.github.io/node-npmdoc-traverse/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-traverse_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-traverse/build..beta..travis-ci.org/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-traverse/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-traverse/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "James Halliday",
        "email": "mail@substack.net",
        "url": "http://substack.net"
    },
    "bugs": {
        "url": "https://github.com/substack/js-traverse/issues"
    },
    "dependencies": {},
    "description": "traverse and transform objects by visiting every node on a recursive walk",
    "devDependencies": {
        "tape": "~1.0.4"
    },
    "directories": {
        "example": "example",
        "test": "test"
    },
    "dist": {
        "shasum": "cbdf560fd7b9af632502fed40f918c157ea97137",
        "tarball": "https://registry.npmjs.org/traverse/-/traverse-0.6.6.tgz"
    },
    "homepage": "https://github.com/substack/js-traverse",
    "keywords": [
        "traverse",
        "walk",
        "recursive",
        "map",
        "forEach",
        "deep",
        "clone"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "substack",
            "email": "mail@substack.net"
        }
    ],
    "name": "traverse",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/substack/js-traverse.git"
    },
    "scripts": {
        "test": "tape test/*.js"
    },
    "testling": {
        "files": "test/*.js",
        "browsers": {
            "iexplore": [
                "6.0",
                "7.0",
                "8.0",
                "9.0"
            ],
            "chrome": [
                "10.0",
                "20.0"
            ],
            "firefox": [
                "10.0",
                "15.0"
            ],
            "safari": [
                "5.1"
            ],
            "opera": [
                "12.0"
            ]
        }
    },
    "version": "0.6.6"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module traverse](#apidoc.module.traverse)
1.  [function <span class="apidocSignatureSpan">traverse.</span>clone (obj)](#apidoc.element.traverse.clone)
1.  [function <span class="apidocSignatureSpan">traverse.</span>forEach (obj)](#apidoc.element.traverse.forEach)
1.  [function <span class="apidocSignatureSpan">traverse.</span>get (obj)](#apidoc.element.traverse.get)
1.  [function <span class="apidocSignatureSpan">traverse.</span>has (obj)](#apidoc.element.traverse.has)
1.  [function <span class="apidocSignatureSpan">traverse.</span>map (obj)](#apidoc.element.traverse.map)
1.  [function <span class="apidocSignatureSpan">traverse.</span>nodes (obj)](#apidoc.element.traverse.nodes)
1.  [function <span class="apidocSignatureSpan">traverse.</span>paths (obj)](#apidoc.element.traverse.paths)
1.  [function <span class="apidocSignatureSpan">traverse.</span>reduce (obj)](#apidoc.element.traverse.reduce)
1.  [function <span class="apidocSignatureSpan">traverse.</span>set (obj)](#apidoc.element.traverse.set)



# <a name="apidoc.module.traverse"></a>[module traverse](#apidoc.module.traverse)

#### <a name="apidoc.element.traverse.clone"></a>[function <span class="apidocSignatureSpan">traverse.</span>clone (obj)](#apidoc.element.traverse.clone)
- description and source-code
```javascript
clone = function (obj) {
    var args = [].slice.call(arguments, 1);
    var t = new Traverse(obj);
    return t[key].apply(t, args);
}
```
- example usage
```shell
...
Return an 'Array' of every possible non-cyclic path in the object.
Paths are 'Array's of string keys.

## .nodes()

Return an 'Array' of every node in the object.

## .clone()

Create a deep clone of the object.

## .get(path)

Get the element at the array 'path'.
...
```

#### <a name="apidoc.element.traverse.forEach"></a>[function <span class="apidocSignatureSpan">traverse.</span>forEach (obj)](#apidoc.element.traverse.forEach)
- description and source-code
```javascript
forEach = function (obj) {
    var args = [].slice.call(arguments, 1);
    var t = new Traverse(obj);
    return t[key].apply(t, args);
}
```
- example usage
```shell
...
    this.value = walk(this.value, cb, false);
    return this.value;
};

Traverse.prototype.reduce = function (cb, init) {
    var skip = arguments.length === 1;
    var acc = skip ? this.value : init;
    this.forEach(function (x) {
        if (!this.isRoot || !skip) {
            acc = cb.call(this, acc, x);
        }
    });
    return acc;
};
...
```

#### <a name="apidoc.element.traverse.get"></a>[function <span class="apidocSignatureSpan">traverse.</span>get (obj)](#apidoc.element.traverse.get)
- description and source-code
```javascript
get = function (obj) {
    var args = [].slice.call(arguments, 1);
    var t = new Traverse(obj);
    return t[key].apply(t, args);
}
```
- example usage
```shell
...

Return an 'Array' of every node in the object.

## .clone()

Create a deep clone of the object.

## .get(path)

Get the element at the array 'path'.

## .set(path, value)

Set the element at the array 'path' to 'value'.
...
```

#### <a name="apidoc.element.traverse.has"></a>[function <span class="apidocSignatureSpan">traverse.</span>has (obj)](#apidoc.element.traverse.has)
- description and source-code
```javascript
has = function (obj) {
    var args = [].slice.call(arguments, 1);
    var t = new Traverse(obj);
    return t[key].apply(t, args);
}
```
- example usage
```shell
...

Get the element at the array 'path'.

## .set(path, value)

Set the element at the array 'path' to 'value'.

## .has(path)

Return whether the element at the array 'path' exists.

# context

Each method that takes a callback has a context (its 'this' object) with these
attributes:
...
```

#### <a name="apidoc.element.traverse.map"></a>[function <span class="apidocSignatureSpan">traverse.</span>map (obj)](#apidoc.element.traverse.map)
- description and source-code
```javascript
map = function (obj) {
    var args = [].slice.call(arguments, 1);
    var t = new Traverse(obj);
    return t[key].apply(t, args);
}
```
- example usage
```shell
...

''''javascript
var traverse = require('traverse');

var obj = { a : 1, b : 2, c : [ 3, 4 ] };
obj.c.push(obj);

var scrubbed = traverse(obj).map(function (x) {
    if (this.circular) this.remove()
});
console.dir(scrubbed);
''''

output:
...
```

#### <a name="apidoc.element.traverse.nodes"></a>[function <span class="apidocSignatureSpan">traverse.</span>nodes (obj)](#apidoc.element.traverse.nodes)
- description and source-code
```javascript
nodes = function (obj) {
    var args = [].slice.call(arguments, 1);
    var t = new Traverse(obj);
    return t[key].apply(t, args);
}
```
- example usage
```shell
...
and the root element is skipped.

## .paths()

Return an 'Array' of every possible non-cyclic path in the object.
Paths are 'Array's of string keys.

## .nodes()

Return an 'Array' of every node in the object.

## .clone()

Create a deep clone of the object.
...
```

#### <a name="apidoc.element.traverse.paths"></a>[function <span class="apidocSignatureSpan">traverse.</span>paths (obj)](#apidoc.element.traverse.paths)
- description and source-code
```javascript
paths = function (obj) {
    var args = [].slice.call(arguments, 1);
    var t = new Traverse(obj);
    return t[key].apply(t, args);
}
```
- example usage
```shell
...
For each node in the object, perform a
[left-fold](http://en.wikipedia.org/wiki/Fold_(higher-order_function))
with the return value of 'fn(acc, node)'.

If 'acc' isn't specified, 'acc' is set to the root object for the first step
and the root element is skipped.

## .paths()

Return an 'Array' of every possible non-cyclic path in the object.
Paths are 'Array's of string keys.

## .nodes()

Return an 'Array' of every node in the object.
...
```

#### <a name="apidoc.element.traverse.reduce"></a>[function <span class="apidocSignatureSpan">traverse.</span>reduce (obj)](#apidoc.element.traverse.reduce)
- description and source-code
```javascript
reduce = function (obj) {
    var args = [].slice.call(arguments, 1);
    var t = new Traverse(obj);
    return t[key].apply(t, args);
}
```
- example usage
```shell
...
var obj = {
    a : [1,2,3],
    b : 4,
    c : [5,6],
    d : { e : [7,8], f : 9 },
};

var leaves = traverse(obj).reduce(function (acc, x) {
    if (this.isLeaf) acc.push(x);
    return acc;
}, []);

console.dir(leaves);
''''
...
```

#### <a name="apidoc.element.traverse.set"></a>[function <span class="apidocSignatureSpan">traverse.</span>set (obj)](#apidoc.element.traverse.set)
- description and source-code
```javascript
set = function (obj) {
    var args = [].slice.call(arguments, 1);
    var t = new Traverse(obj);
    return t[key].apply(t, args);
}
```
- example usage
```shell
...

Create a deep clone of the object.

## .get(path)

Get the element at the array 'path'.

## .set(path, value)

Set the element at the array 'path' to 'value'.

## .has(path)

Return whether the element at the array 'path' exists.
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

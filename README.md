# npmdoc-parcelify

#### basic api documentation for  [parcelify (v2.2.0)](https://github.com/rotundasoftware/parcelify)  [![npm package](https://img.shields.io/npm/v/npmdoc-parcelify.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-parcelify) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-parcelify.svg)](https://travis-ci.org/npmdoc/node-npmdoc-parcelify)

#### Create css bundles from npm packages using the browserify dependency graph.

[![NPM](https://nodei.co/npm/parcelify.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/parcelify)

- [https://npmdoc.github.io/node-npmdoc-parcelify/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-parcelify/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-parcelify/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-parcelify/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-parcelify/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-parcelify/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Rotunda Software"
    },
    "bin": {
        "parcelify": "bin/cmd.js"
    },
    "bugs": {
        "url": "https://github.com/rotundasoftware/parcelify/issues"
    },
    "dependencies": {
        "async": "~0.2.10",
        "glob": "~3.2.9",
        "globwatcher": "~1.2.3",
        "inherits": "~2.0.1",
        "minimist": "0.0.8",
        "mkdirp": "~0.3.5",
        "npmlog": "0.0.6",
        "parcel-map": "^3.0.0",
        "resolve": "~0.6.1",
        "shasum": "~1.0.1",
        "stream-combiner": "^0.2.2",
        "through2": "~0.6.3",
        "toposort": "~0.2.10",
        "underscore": "~1.6.0"
    },
    "description": "Create css bundles from npm packages using the browserify dependency graph.",
    "devDependencies": {
        "browserify": "^9.0.8",
        "sass-css-stream": "^0.1.4",
        "tape": "~2.3.2"
    },
    "directories": {},
    "dist": {
        "shasum": "d77be17d13609e05e40f7409e1c4a162672c2391",
        "tarball": "https://registry.npmjs.org/parcelify/-/parcelify-2.2.0.tgz"
    },
    "gitHead": "5400f2a3faa960c712cad864e747ef0a42a0bd5a",
    "homepage": "https://github.com/rotundasoftware/parcelify",
    "keywords": [
        "parcel",
        "asset",
        "css",
        "commonjs",
        "browserify"
    ],
    "licenses": [
        {
            "type": "MIT",
            "url": "https://github.com/rotundasoftware/parcelify/blob/master/LICENSE"
        }
    ],
    "main": "index.js",
    "maintainers": [
        {
            "name": "rotundasoftware"
        },
        {
            "name": "go-oleg"
        },
        {
            "name": "davidbeck"
        },
        {
            "name": "substack"
        }
    ],
    "name": "parcelify",
    "optionalDependencies": {},
    "repository": {
        "type": "git",
        "url": "git://github.com/rotundasoftware/parcelify.git"
    },
    "scripts": {
        "test": "tape test/test.js"
    },
    "version": "2.2.0"
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

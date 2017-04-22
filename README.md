# npmdoc-json-api

#### api documentation for  [json-api (v2.15.7)](https://github.com/ethanresnick/json-api)  [![npm package](https://img.shields.io/npm/v/npmdoc-json-api.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-json-api) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-json-api.svg)](https://travis-ci.org/npmdoc/node-npmdoc-json-api)

#### A library for constructing JSON-API compliant responses

[![NPM](https://nodei.co/npm/json-api.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/json-api)

- [https://npmdoc.github.io/node-npmdoc-json-api/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-json-api/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-json-api/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-json-api/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-json-api/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-json-api/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Ethan Resnick"
    },
    "bugs": {
        "url": "https://github.com/ethanresnick/json-api/issues"
    },
    "dependencies": {
        "babel-runtime": "5.6.17",
        "co": "4.5.x",
        "content-type": "1.x.x",
        "dasherize": "2.0.x",
        "flat": "^1.2.1",
        "immutable": "^3.7.5",
        "jade": "1.11.x",
        "lodash": "^3.10.0",
        "negotiator": "github:ethanresnick/negotiator#full-parse-access",
        "pluralize": "0.0.11",
        "q": "1.4.1",
        "qs": "^5.2.0",
        "raw-body": "1.3.x",
        "url-template": "^2.0.4",
        "vary": "^1.0.0"
    },
    "description": "A library for constructing JSON-API compliant responses",
    "devDependencies": {
        "babel": "5.6.14",
        "babel-eslint": "3.x.x",
        "chai": "^1.9.2",
        "chai-subset": "^1.1.0",
        "coveralls": "^2.11.4",
        "eslint": "0.x.x",
        "express": "4.x.x",
        "gulp": "^3.8.6",
        "istanbul": "0.3.x",
        "mocha": "2.2.x",
        "mongoose": "4.0.x",
        "node-mongoose-fixtures": "^0.2.4",
        "sinon": "1.10.2",
        "superagent": "1.2.x"
    },
    "directories": {},
    "dist": {
        "shasum": "714e6eecd78653a3cf6b24ec3f76dd2b19cb7caa",
        "tarball": "https://registry.npmjs.org/json-api/-/json-api-2.15.7.tgz"
    },
    "gitHead": "1e17547448df762e7b489e9bdf64edb11ca25f77",
    "homepage": "https://github.com/ethanresnick/json-api",
    "keywords": [
        "json-api",
        "jsonapi",
        "api",
        "hypermedia",
        "rest",
        "restful"
    ],
    "license": "LGPL-3.0",
    "main": "index.js",
    "maintainers": [
        {
            "name": "ethanresnick"
        }
    ],
    "name": "json-api",
    "optionalDependencies": {},
    "peerDependencies": {
        "mongoose": "^4.0.0",
        "express": "^4.0.0"
    },
    "repository": {
        "type": "git",
        "url": "git://github.com/ethanresnick/json-api.git"
    },
    "scripts": {
        "cover_ci": "istanbul cover -x **/lib/** --report lcovonly ./node_modules/mocha/bin/_mocha -- -R dot ./build/test/integration/index.js $(find ./build/test/unit -name \"*.js\") && cat ./coverage/lcov.info | ./node_modules/coveralls/bin/coveralls.js && rm -rf ./coverage",
        "cover_local": "istanbul cover -x **/lib/** --report lcovonly ./node_modules/mocha/bin/_mocha -- ./build/test/integration/index.js $(find ./build/test/unit -name \"*.js\") > /dev/null",
        "prepublish": "make compile",
        "test": "./node_modules/mocha/bin/_mocha ./build/test/integration/index.js $(find ./build/test/unit -name \"*.js\")"
    },
    "version": "2.15.7",
    "bin": {}
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

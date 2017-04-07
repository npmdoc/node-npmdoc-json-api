# api documentation for  [json-api (v2.15.7)](https://github.com/ethanresnick/json-api)  [![npm package](https://img.shields.io/npm/v/npmdoc-json-api.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-json-api) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-json-api.svg)](https://travis-ci.org/npmdoc/node-npmdoc-json-api)
#### A library for constructing JSON-API compliant responses

[![NPM](https://nodei.co/npm/json-api.png?downloads=true)](https://www.npmjs.com/package/json-api)

[![apidoc](https://npmdoc.github.io/node-npmdoc-json-api/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-json-api_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-json-api/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-json-api/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-json-api/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Ethan Resnick",
        "email": "ethan.resnick@gmail.com"
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
            "name": "ethanresnick",
            "email": "studip101@gmail.com"
        }
    ],
    "name": "json-api",
    "optionalDependencies": {},
    "peerDependencies": {
        "mongoose": "^4.0.0",
        "express": "^4.0.0"
    },
    "readme": "ERROR: No README data found!",
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
    "version": "2.15.7"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module json-api](#apidoc.module.json-api)
1.  [function <span class="apidocSignatureSpan">json-api.</span>ResourceTypeRegistry ()](#apidoc.element.json-api.ResourceTypeRegistry)
1.  object <span class="apidocSignatureSpan">json-api.</span>ResourceTypeRegistry.prototype
1.  object <span class="apidocSignatureSpan">json-api.</span>controllers
1.  object <span class="apidocSignatureSpan">json-api.</span>dbAdapters
1.  object <span class="apidocSignatureSpan">json-api.</span>httpStrategies
1.  object <span class="apidocSignatureSpan">json-api.</span>types
1.  object <span class="apidocSignatureSpan">json-api.</span>types.Documentation

#### [module json-api.ResourceTypeRegistry](#apidoc.module.json-api.ResourceTypeRegistry)
1.  [function <span class="apidocSignatureSpan">json-api.</span>ResourceTypeRegistry ()](#apidoc.element.json-api.ResourceTypeRegistry.ResourceTypeRegistry)

#### [module json-api.ResourceTypeRegistry.prototype](#apidoc.module.json-api.ResourceTypeRegistry.prototype)
1.  [function <span class="apidocSignatureSpan">json-api.ResourceTypeRegistry.prototype.</span>beforeRender (type)](#apidoc.element.json-api.ResourceTypeRegistry.prototype.beforeRender)
1.  [function <span class="apidocSignatureSpan">json-api.ResourceTypeRegistry.prototype.</span>beforeSave (type)](#apidoc.element.json-api.ResourceTypeRegistry.prototype.beforeSave)
1.  [function <span class="apidocSignatureSpan">json-api.ResourceTypeRegistry.prototype.</span>behaviors (type)](#apidoc.element.json-api.ResourceTypeRegistry.prototype.behaviors)
1.  [function <span class="apidocSignatureSpan">json-api.ResourceTypeRegistry.prototype.</span>dbAdapter (type)](#apidoc.element.json-api.ResourceTypeRegistry.prototype.dbAdapter)
1.  [function <span class="apidocSignatureSpan">json-api.ResourceTypeRegistry.prototype.</span>defaultIncludes (type)](#apidoc.element.json-api.ResourceTypeRegistry.prototype.defaultIncludes)
1.  [function <span class="apidocSignatureSpan">json-api.ResourceTypeRegistry.prototype.</span>info (type)](#apidoc.element.json-api.ResourceTypeRegistry.prototype.info)
1.  [function <span class="apidocSignatureSpan">json-api.ResourceTypeRegistry.prototype.</span>labelMappers (type)](#apidoc.element.json-api.ResourceTypeRegistry.prototype.labelMappers)
1.  [function <span class="apidocSignatureSpan">json-api.ResourceTypeRegistry.prototype.</span>parentType (type)](#apidoc.element.json-api.ResourceTypeRegistry.prototype.parentType)

#### [module json-api.controllers](#apidoc.module.json-api.controllers)
1.  [function <span class="apidocSignatureSpan">json-api.controllers.</span>API (registry)](#apidoc.element.json-api.controllers.API)
1.  [function <span class="apidocSignatureSpan">json-api.controllers.</span>Documentation (registry, apiInfo, templatePath)](#apidoc.element.json-api.controllers.Documentation)

#### [module json-api.dbAdapters](#apidoc.module.json-api.dbAdapters)
1.  [function <span class="apidocSignatureSpan">json-api.dbAdapters.</span>Mongoose (models, inflector, idGenerator)](#apidoc.element.json-api.dbAdapters.Mongoose)

#### [module json-api.httpStrategies](#apidoc.module.json-api.httpStrategies)
1.  [function <span class="apidocSignatureSpan">json-api.httpStrategies.</span>Express (apiController, docsController, options)](#apidoc.element.json-api.httpStrategies.Express)
1.  [function <span class="apidocSignatureSpan">json-api.httpStrategies.</span>Koa (apiController, docsController, options)](#apidoc.element.json-api.httpStrategies.Koa)

#### [module json-api.types](#apidoc.module.json-api.types)
1.  [function <span class="apidocSignatureSpan">json-api.types.</span>Collection ()](#apidoc.element.json-api.types.Collection)
1.  [function <span class="apidocSignatureSpan">json-api.types.</span>Document (primaryOrErrors, included, meta, urlTemplates, reqURI)](#apidoc.element.json-api.types.Document)
1.  [function <span class="apidocSignatureSpan">json-api.types.</span>Error (status, code, title, detail, links, paths)](#apidoc.element.json-api.types.Error)
1.  [function <span class="apidocSignatureSpan">json-api.types.</span>Linkage (value)](#apidoc.element.json-api.types.Linkage)
1.  [function <span class="apidocSignatureSpan">json-api.types.</span>Relationship (linkage, relatedURITemplate, selfURITemplate)](#apidoc.element.json-api.types.Relationship)
1.  [function <span class="apidocSignatureSpan">json-api.types.</span>Resource (type, id)](#apidoc.element.json-api.types.Resource)
1.  object <span class="apidocSignatureSpan">json-api.types.</span>Documentation

#### [module json-api.types.Documentation](#apidoc.module.json-api.types.Documentation)
1.  [function <span class="apidocSignatureSpan">json-api.types.Documentation.</span>Field (name, type, validation, friendlyName, defaultVal)](#apidoc.element.json-api.types.Documentation.Field)
1.  [function <span class="apidocSignatureSpan">json-api.types.Documentation.</span>FieldType (baseType)](#apidoc.element.json-api.types.Documentation.FieldType)



# <a name="apidoc.module.json-api"></a>[module json-api](#apidoc.module.json-api)

#### <a name="apidoc.element.json-api.ResourceTypeRegistry"></a>[function <span class="apidocSignatureSpan">json-api.</span>ResourceTypeRegistry ()](#apidoc.element.json-api.ResourceTypeRegistry)
- description and source-code
```javascript
function ResourceTypeRegistry() {
  var _this = this;

  var typeDescriptions = arguments.length <= 0 || arguments[0] === undefined ? {} : arguments[0];
  var descriptionDefaults = arguments.length <= 1 || arguments[1] === undefined ? {} : arguments[1];

  _classCallCheck(this, ResourceTypeRegistry);

  this[typesKey] = {};
  descriptionDefaults = globalResourceDefaults.mergeDeep(descriptionDefaults);

  // Sort the types so we can register them in an order that respects their
  // parentType. First, we pre-process the typeDescriptions to create edges
  // pointing to each node's children (rather than the links we have by
  // default, which point to the parent). Then we do an abridged topological
  // sort that works in this case. Below, nodes is a list of type names.
  // Roots are nodes with no parents. Edges is a map, with each key being the
  // name of a starting node A, and the value being a set of node names for
  // which there is an edge from A to that node.
  var nodes = [],
      roots = [],
      edges = {};

  for (var typeName in typeDescriptions) {
    var nodeParentType = typeDescriptions[typeName].parentType;
    nodes.push(typeName);

    if (nodeParentType) {
      edges[nodeParentType] = edges[nodeParentType] || {};
      edges[nodeParentType][typeName] = true;
    } else {
      roots.push(typeName);
    }
  }

  var typeRegistrationOrder = (0, _utilMisc.pseudoTopSort)(nodes, edges, roots);

  // register the types, in order
  typeRegistrationOrder.forEach(function (typeName) {
    var parentType = typeDescriptions[typeName].parentType;

    // defaultIncludes need to be made into an object if they came as an array.
    // TODO: Remove support for array format before v3. It's inconsistent.
    var thisDescriptionRaw = _immutable2["default"].fromJS(typeDescriptions[typeName]);
    var thisDescriptionMerged = descriptionDefaults.mergeDeep(thisDescriptionRaw);

    _this[typesKey][typeName] = parentType ?
    // If we have a parentType, we merge in all the parent's fields,
    // BUT we then overwrite labelMappers with just the ones directly
    // from this description. We don't inherit labelMappers because a
    // labelMapper is a kind of filter, and the results of a filter
    // on the parent type may not be instances of the subtype.
    _this[typesKey][parentType].mergeDeep(thisDescriptionRaw).set("labelMappers", thisDescriptionRaw.get("labelMappers")) :

    // If we don't have a parentType, just register
    // the description merged with the universal defaults
    thisDescriptionMerged;
  });
}
```
- example usage
```shell
...

var models = {
  "Person": require('./models/person'),
  "Place": require('./models/place')
};

var adapter = new API.dbAdapters.Mongoose(models);
var registry = new API.ResourceTypeRegistry({
  "people": {
    urlTemplates: {
      "self": "/people/{id}"
    },
    beforeRender: function(resource, req, res) {
      if(!userIsAdmin(req)) resource.removeAttr("password");
      return resource;
...
```



# <a name="apidoc.module.json-api.ResourceTypeRegistry"></a>[module json-api.ResourceTypeRegistry](#apidoc.module.json-api.ResourceTypeRegistry)

#### <a name="apidoc.element.json-api.ResourceTypeRegistry.ResourceTypeRegistry"></a>[function <span class="apidocSignatureSpan">json-api.</span>ResourceTypeRegistry ()](#apidoc.element.json-api.ResourceTypeRegistry.ResourceTypeRegistry)
- description and source-code
```javascript
function ResourceTypeRegistry() {
  var _this = this;

  var typeDescriptions = arguments.length <= 0 || arguments[0] === undefined ? {} : arguments[0];
  var descriptionDefaults = arguments.length <= 1 || arguments[1] === undefined ? {} : arguments[1];

  _classCallCheck(this, ResourceTypeRegistry);

  this[typesKey] = {};
  descriptionDefaults = globalResourceDefaults.mergeDeep(descriptionDefaults);

  // Sort the types so we can register them in an order that respects their
  // parentType. First, we pre-process the typeDescriptions to create edges
  // pointing to each node's children (rather than the links we have by
  // default, which point to the parent). Then we do an abridged topological
  // sort that works in this case. Below, nodes is a list of type names.
  // Roots are nodes with no parents. Edges is a map, with each key being the
  // name of a starting node A, and the value being a set of node names for
  // which there is an edge from A to that node.
  var nodes = [],
      roots = [],
      edges = {};

  for (var typeName in typeDescriptions) {
    var nodeParentType = typeDescriptions[typeName].parentType;
    nodes.push(typeName);

    if (nodeParentType) {
      edges[nodeParentType] = edges[nodeParentType] || {};
      edges[nodeParentType][typeName] = true;
    } else {
      roots.push(typeName);
    }
  }

  var typeRegistrationOrder = (0, _utilMisc.pseudoTopSort)(nodes, edges, roots);

  // register the types, in order
  typeRegistrationOrder.forEach(function (typeName) {
    var parentType = typeDescriptions[typeName].parentType;

    // defaultIncludes need to be made into an object if they came as an array.
    // TODO: Remove support for array format before v3. It's inconsistent.
    var thisDescriptionRaw = _immutable2["default"].fromJS(typeDescriptions[typeName]);
    var thisDescriptionMerged = descriptionDefaults.mergeDeep(thisDescriptionRaw);

    _this[typesKey][typeName] = parentType ?
    // If we have a parentType, we merge in all the parent's fields,
    // BUT we then overwrite labelMappers with just the ones directly
    // from this description. We don't inherit labelMappers because a
    // labelMapper is a kind of filter, and the results of a filter
    // on the parent type may not be instances of the subtype.
    _this[typesKey][parentType].mergeDeep(thisDescriptionRaw).set("labelMappers", thisDescriptionRaw.get("labelMappers")) :

    // If we don't have a parentType, just register
    // the description merged with the universal defaults
    thisDescriptionMerged;
  });
}
```
- example usage
```shell
...

var models = {
  "Person": require('./models/person'),
  "Place": require('./models/place')
};

var adapter = new API.dbAdapters.Mongoose(models);
var registry = new API.ResourceTypeRegistry({
  "people": {
    urlTemplates: {
      "self": "/people/{id}"
    },
    beforeRender: function(resource, req, res) {
      if(!userIsAdmin(req)) resource.removeAttr("password");
      return resource;
...
```



# <a name="apidoc.module.json-api.ResourceTypeRegistry.prototype"></a>[module json-api.ResourceTypeRegistry.prototype](#apidoc.module.json-api.ResourceTypeRegistry.prototype)

#### <a name="apidoc.element.json-api.ResourceTypeRegistry.prototype.beforeRender"></a>[function <span class="apidocSignatureSpan">json-api.ResourceTypeRegistry.prototype.</span>beforeRender (type)](#apidoc.element.json-api.ResourceTypeRegistry.prototype.beforeRender)
- description and source-code
```javascript
beforeRender = function (type) {
  return (0, _utilTypeHandling.Maybe)(this[typesKey][type]).bind(function (it) {
    return it.get(attrName);
  }).bind(function (it) {
    return it instanceof _immutable2["default"].Map || it instanceof _immutable2["default"].List ? it.toJS() : it;
  }).unwrap();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-api.ResourceTypeRegistry.prototype.beforeSave"></a>[function <span class="apidocSignatureSpan">json-api.ResourceTypeRegistry.prototype.</span>beforeSave (type)](#apidoc.element.json-api.ResourceTypeRegistry.prototype.beforeSave)
- description and source-code
```javascript
beforeSave = function (type) {
  return (0, _utilTypeHandling.Maybe)(this[typesKey][type]).bind(function (it) {
    return it.get(attrName);
  }).bind(function (it) {
    return it instanceof _immutable2["default"].Map || it instanceof _immutable2["default"].List ? it.toJS() : it;
  }).unwrap();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-api.ResourceTypeRegistry.prototype.behaviors"></a>[function <span class="apidocSignatureSpan">json-api.ResourceTypeRegistry.prototype.</span>behaviors (type)](#apidoc.element.json-api.ResourceTypeRegistry.prototype.behaviors)
- description and source-code
```javascript
behaviors = function (type) {
  return (0, _utilTypeHandling.Maybe)(this[typesKey][type]).bind(function (it) {
    return it.get(attrName);
  }).bind(function (it) {
    return it instanceof _immutable2["default"].Map || it instanceof _immutable2["default"].List ? it.toJS() : it;
  }).unwrap();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-api.ResourceTypeRegistry.prototype.dbAdapter"></a>[function <span class="apidocSignatureSpan">json-api.ResourceTypeRegistry.prototype.</span>dbAdapter (type)](#apidoc.element.json-api.ResourceTypeRegistry.prototype.dbAdapter)
- description and source-code
```javascript
dbAdapter = function (type) {
  return (0, _utilTypeHandling.Maybe)(this[typesKey][type]).bind(function (it) {
    return it.get(attrName);
  }).bind(function (it) {
    return it instanceof _immutable2["default"].Map || it instanceof _immutable2["default"].List ? it.toJS() : it;
  }).unwrap();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-api.ResourceTypeRegistry.prototype.defaultIncludes"></a>[function <span class="apidocSignatureSpan">json-api.ResourceTypeRegistry.prototype.</span>defaultIncludes (type)](#apidoc.element.json-api.ResourceTypeRegistry.prototype.defaultIncludes)
- description and source-code
```javascript
defaultIncludes = function (type) {
  return (0, _utilTypeHandling.Maybe)(this[typesKey][type]).bind(function (it) {
    return it.get(attrName);
  }).bind(function (it) {
    return it instanceof _immutable2["default"].Map || it instanceof _immutable2["default"].List ? it.toJS() : it;
  }).unwrap();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-api.ResourceTypeRegistry.prototype.info"></a>[function <span class="apidocSignatureSpan">json-api.ResourceTypeRegistry.prototype.</span>info (type)](#apidoc.element.json-api.ResourceTypeRegistry.prototype.info)
- description and source-code
```javascript
info = function (type) {
  return (0, _utilTypeHandling.Maybe)(this[typesKey][type]).bind(function (it) {
    return it.get(attrName);
  }).bind(function (it) {
    return it instanceof _immutable2["default"].Map || it instanceof _immutable2["default"].List ? it.toJS() : it;
  }).unwrap();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-api.ResourceTypeRegistry.prototype.labelMappers"></a>[function <span class="apidocSignatureSpan">json-api.ResourceTypeRegistry.prototype.</span>labelMappers (type)](#apidoc.element.json-api.ResourceTypeRegistry.prototype.labelMappers)
- description and source-code
```javascript
labelMappers = function (type) {
  return (0, _utilTypeHandling.Maybe)(this[typesKey][type]).bind(function (it) {
    return it.get(attrName);
  }).bind(function (it) {
    return it instanceof _immutable2["default"].Map || it instanceof _immutable2["default"].List ? it.toJS() : it;
  }).unwrap();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-api.ResourceTypeRegistry.prototype.parentType"></a>[function <span class="apidocSignatureSpan">json-api.ResourceTypeRegistry.prototype.</span>parentType (type)](#apidoc.element.json-api.ResourceTypeRegistry.prototype.parentType)
- description and source-code
```javascript
parentType = function (type) {
  return (0, _utilTypeHandling.Maybe)(this[typesKey][type]).bind(function (it) {
    return it.get(attrName);
  }).bind(function (it) {
    return it instanceof _immutable2["default"].Map || it instanceof _immutable2["default"].List ? it.toJS() : it;
  }).unwrap();
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-api.controllers"></a>[module json-api.controllers](#apidoc.module.json-api.controllers)

#### <a name="apidoc.element.json-api.controllers.API"></a>[function <span class="apidocSignatureSpan">json-api.controllers.</span>API (registry)](#apidoc.element.json-api.controllers.API)
- description and source-code
```javascript
function APIController(registry) {
  _classCallCheck(this, APIController);

  this.registry = registry;
}
```
- example usage
```shell
...
  "dbAdapter": adapter
});

// Initialize the automatic documentation.
var DocsController = new API.controllers.Documentation(registry, {name: 'Example API'});

// Set up our controllers
var APIController = new API.controllers.API(registry);
var Front = new API.httpStrategies.Express(APIController, DocsController);
var requestHandler = Front.apiRequest.bind(Front);

// Add routes for basic list, read, create, update, delete operations
app.get("/:type(people|places)", requestHandler);
app.get("/:type(people|places)/:id", requestHandler);
app.post("/:type(people|places)", requestHandler);
...
```

#### <a name="apidoc.element.json-api.controllers.Documentation"></a>[function <span class="apidocSignatureSpan">json-api.controllers.</span>Documentation (registry, apiInfo, templatePath)](#apidoc.element.json-api.controllers.Documentation)
- description and source-code
```javascript
function DocumentationController(registry, apiInfo, templatePath) {
  var _this = this;

  var dasherizeJSONKeys = arguments.length <= 3 || arguments[3] === undefined ? true : arguments[3];

  _classCallCheck(this, DocumentationController);

  this.registry = registry;

  var defaultTempPath = "../../../templates/documentation.jade";
  this.template = templatePath || _path2["default"].resolve(__dirname, defaultTempPath);

  this.dasherizeJSONKeys = dasherizeJSONKeys;

  // compute template data on construction
  // (it never changes, so this makes more sense than doing it per request)
  var data = _Object$assign({}, apiInfo);
  data.resourcesMap = {};

  // Store in the resourcesMap the info object about each type,
  // as returned by @getTypeInfo.
  this.registry.typeNames().forEach(function (typeName) {
    data.resourcesMap[typeName] = _this.getTypeInfo(typeName);
  });

  this.templateData = data;
}
```
- example usage
```shell
...
    urlTemplates: {"self": "/places/{id}"}
  }
}, {
  "dbAdapter": adapter
});

// Initialize the automatic documentation.
var DocsController = new API.controllers.Documentation(registry, {name: 'Example API'});

// Set up our controllers
var APIController = new API.controllers.API(registry);
var Front = new API.httpStrategies.Express(APIController, DocsController);
var requestHandler = Front.apiRequest.bind(Front);

// Add routes for basic list, read, create, update, delete operations
...
```



# <a name="apidoc.module.json-api.dbAdapters"></a>[module json-api.dbAdapters](#apidoc.module.json-api.dbAdapters)

#### <a name="apidoc.element.json-api.dbAdapters.Mongoose"></a>[function <span class="apidocSignatureSpan">json-api.dbAdapters.</span>Mongoose (models, inflector, idGenerator)](#apidoc.element.json-api.dbAdapters.Mongoose)
- description and source-code
```javascript
function MongooseAdapter(models, inflector, idGenerator) {
  _classCallCheck(this, MongooseAdapter);

  this.models = models || _mongoose2["default"].models;
  this.inflector = inflector || _pluralize2["default"];
  this.idGenerator = idGenerator;
}
```
- example usage
```shell
...
  , API = require('json-api');

var models = {
  "Person": require('./models/person'),
  "Place": require('./models/place')
};

var adapter = new API.dbAdapters.Mongoose(models);
var registry = new API.ResourceTypeRegistry({
  "people": {
    urlTemplates: {
      "self": "/people/{id}"
    },
    beforeRender: function(resource, req, res) {
      if(!userIsAdmin(req)) resource.removeAttr("password");
...
```



# <a name="apidoc.module.json-api.httpStrategies"></a>[module json-api.httpStrategies](#apidoc.module.json-api.httpStrategies)

#### <a name="apidoc.element.json-api.httpStrategies.Express"></a>[function <span class="apidocSignatureSpan">json-api.httpStrategies.</span>Express (apiController, docsController, options)](#apidoc.element.json-api.httpStrategies.Express)
- description and source-code
```javascript
function ExpressStrategy(apiController, docsController, options) {
  _classCallCheck(this, ExpressStrategy);

  _get(Object.getPrototypeOf(ExpressStrategy.prototype), "constructor", this).call(this, apiController, docsController, options);
}
```
- example usage
```shell
...
});

// Initialize the automatic documentation.
var DocsController = new API.controllers.Documentation(registry, {name: 'Example API'});

// Set up our controllers
var APIController = new API.controllers.API(registry);
var Front = new API.httpStrategies.Express(APIController, DocsController);
var requestHandler = Front.apiRequest.bind(Front);

// Add routes for basic list, read, create, update, delete operations
app.get("/:type(people|places)", requestHandler);
app.get("/:type(people|places)/:id", requestHandler);
app.post("/:type(people|places)", requestHandler);
app.patch("/:type(people|places)/:id", requestHandler);
...
```

#### <a name="apidoc.element.json-api.httpStrategies.Koa"></a>[function <span class="apidocSignatureSpan">json-api.httpStrategies.</span>Koa (apiController, docsController, options)](#apidoc.element.json-api.httpStrategies.Koa)
- description and source-code
```javascript
function KoaStrategy(apiController, docsController, options) {
  _classCallCheck(this, KoaStrategy);

  _get(Object.getPrototypeOf(KoaStrategy.prototype), "constructor", this).call(this, apiController, docsController, options);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-api.types"></a>[module json-api.types](#apidoc.module.json-api.types)

#### <a name="apidoc.element.json-api.types.Collection"></a>[function <span class="apidocSignatureSpan">json-api.types.</span>Collection ()](#apidoc.element.json-api.types.Collection)
- description and source-code
```javascript
function Collection() {
  var resources = arguments.length <= 0 || arguments[0] === undefined ? [] : arguments[0];

  _classCallCheck(this, Collection);

  this.resources = resources;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-api.types.Document"></a>[function <span class="apidocSignatureSpan">json-api.types.</span>Document (primaryOrErrors, included, meta, urlTemplates, reqURI)](#apidoc.element.json-api.types.Document)
- description and source-code
```javascript
function Document(primaryOrErrors, included, meta, urlTemplates, reqURI) {
  _classCallCheck(this, Document);

  // validate meta
  var _ref = [primaryOrErrors, included, reqURI];
  this.primaryOrErrors = _ref[0];
  this.included = _ref[1];
  this.reqURI = _ref[2];
  if (meta !== undefined) {
    if (typeof meta === "object" && !Array.isArray(meta)) {
      this.meta = meta;
    } else {
      throw new Error("Meta information must be an object");
    }
  }

  // parse all the templates once on construction.
  this.urlTemplates = (0, _utilTypeHandling.mapObject)(urlTemplates || {}, function (templatesForType) {
    return (0, _utilTypeHandling.mapObject)(templatesForType, _urlTemplate2["default"].parse.bind(_urlTemplate2["default"]));
  });

  this.reqURI = reqURI;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-api.types.Error"></a>[function <span class="apidocSignatureSpan">json-api.types.</span>Error (status, code, title, detail, links, paths)](#apidoc.element.json-api.types.Error)
- description and source-code
```javascript
function APIError(status, code, title, detail, links, paths) {
  var _this = this;

  _classCallCheck(this, APIError);

  _get(Object.getPrototypeOf(APIError.prototype), "constructor", this).call(this);

  // Hack around lack of proxy support and default non-enumerability
  // of class accessor properties, while still giving us validation.
  Object.defineProperty(this, "_status", nonEnumerable);
  Object.defineProperty(this, "_code", nonEnumerable);
  Object.defineProperty(this, "status", {
    enumerable: true,
    get: function get() {
      return _this._status;
    },
    set: function set(value) {
      if (typeof value !== "undefined" && value !== null) {
        _this._status = String(value).toString();
      } else {
        _this._status = value;
      }
    }
  });
  Object.defineProperty(this, "code", {
    enumerable: true,
    get: function get() {
      return _this._code;
    },
    set: function set(value) {
      if (typeof value !== "undefined" && value !== null) {
        _this._code = String(value).toString();
      } else {
        _this._code = value;
      }
    }
  });

  var _Array$from = _Array$from3(arguments);

  var _Array$from2 = _slicedToArray(_Array$from, 6);

  this.status = _Array$from2[0];
  this.code = _Array$from2[1];
  this.title = _Array$from2[2];
  this.detail = _Array$from2[3];
  this.links = _Array$from2[4];
  this.paths = _Array$from2[5];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-api.types.Linkage"></a>[function <span class="apidocSignatureSpan">json-api.types.</span>Linkage (value)](#apidoc.element.json-api.types.Linkage)
- description and source-code
```javascript
function Linkage(value) {
  _classCallCheck(this, Linkage);

  this.set(value);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-api.types.Relationship"></a>[function <span class="apidocSignatureSpan">json-api.types.</span>Relationship (linkage, relatedURITemplate, selfURITemplate)](#apidoc.element.json-api.types.Relationship)
- description and source-code
```javascript
function Relationship(linkage, relatedURITemplate, selfURITemplate) {
  _classCallCheck(this, Relationship);

  _Object$assign(this, { linkage: linkage, relatedURITemplate: relatedURITemplate, selfURITemplate: selfURITemplate });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-api.types.Resource"></a>[function <span class="apidocSignatureSpan">json-api.types.</span>Resource (type, id)](#apidoc.element.json-api.types.Resource)
- description and source-code
```javascript
function Resource(type, id) {
  var attrs = arguments.length <= 2 || arguments[2] === undefined ? {} : arguments[2];
  var relationships = arguments.length <= 3 || arguments[3] === undefined ? {} : arguments[3];
  var meta = arguments.length <= 4 || arguments[4] === undefined ? {} : arguments[4];

  _classCallCheck(this, Resource);

  var _ref = [type, id, attrs, relationships, meta];
  this.type = _ref[0];
  this.id = _ref[1];
  this.attrs = _ref[2];
  this.relationships = _ref[3];
  this.meta = _ref[4];
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.json-api.types.Documentation"></a>[module json-api.types.Documentation](#apidoc.module.json-api.types.Documentation)

#### <a name="apidoc.element.json-api.types.Documentation.Field"></a>[function <span class="apidocSignatureSpan">json-api.types.Documentation.</span>Field (name, type, validation, friendlyName, defaultVal)](#apidoc.element.json-api.types.Documentation.Field)
- description and source-code
```javascript
function Field(name, type, validation, friendlyName, defaultVal) {
  if (validation === undefined) validation = {};

  _classCallCheck(this, Field);

  // call the property kind to
  // distinguish it from json api type
  this.kind = type;

  this.name = name;
  this.validation = validation;
  this.friendlyName = friendlyName;
  this["default"] = defaultVal;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.json-api.types.Documentation.FieldType"></a>[function <span class="apidocSignatureSpan">json-api.types.Documentation.</span>FieldType (baseType)](#apidoc.element.json-api.types.Documentation.FieldType)
- description and source-code
```javascript
function FieldType(baseType) {
  var isArray = arguments.length <= 1 || arguments[1] === undefined ? false : arguments[1];

  _classCallCheck(this, FieldType);

  var _ref = [baseType, isArray];
  this.baseType = _ref[0];
  this.isArray = _ref[1];
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

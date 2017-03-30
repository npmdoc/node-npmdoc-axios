# api documentation for  [axios (v0.15.3)](https://github.com/mzabriskie/axios)  [![npm package](https://img.shields.io/npm/v/npmdoc-axios.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-axios) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-axios.svg)](https://travis-ci.org/npmdoc/node-npmdoc-axios)
#### Promise based HTTP client for the browser and node.js

[![NPM](https://nodei.co/npm/axios.png?downloads=true)](https://www.npmjs.com/package/axios)

[![apidoc](https://npmdoc.github.io/node-npmdoc-axios/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-axios_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-axios/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-axios/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Matt Zabriskie"
    },
    "browser": {
        "./lib/adapters/http.js": "./lib/adapters/xhr.js"
    },
    "bugs": {
        "url": "https://github.com/mzabriskie/axios/issues"
    },
    "dependencies": {
        "follow-redirects": "1.0.0"
    },
    "description": "Promise based HTTP client for the browser and node.js",
    "devDependencies": {
        "coveralls": "^2.11.9",
        "es6-promise": "^4.0.5",
        "grunt": "^1.0.1",
        "grunt-banner": "^0.6.0",
        "grunt-cli": "^1.2.0",
        "grunt-contrib-clean": "^1.0.0",
        "grunt-contrib-nodeunit": "^1.0.0",
        "grunt-contrib-watch": "^1.0.0",
        "grunt-eslint": "^19.0.0",
        "grunt-karma": "^2.0.0",
        "grunt-ts": "^6.0.0-beta.3",
        "grunt-typings": "^0.1.5",
        "grunt-webpack": "^1.0.18",
        "istanbul-instrumenter-loader": "^1.0.0",
        "jasmine-core": "^2.4.1",
        "karma": "^1.3.0",
        "karma-chrome-launcher": "^2.0.0",
        "karma-coverage": "^1.0.0",
        "karma-firefox-launcher": "^1.0.0",
        "karma-jasmine": "^1.0.2",
        "karma-jasmine-ajax": "^0.1.13",
        "karma-opera-launcher": "^1.0.0",
        "karma-phantomjs-launcher": "^1.0.0",
        "karma-safari-launcher": "^1.0.0",
        "karma-sauce-launcher": "^1.1.0",
        "karma-sinon": "^1.0.5",
        "karma-sourcemap-loader": "^0.3.7",
        "karma-webpack": "^1.7.0",
        "load-grunt-tasks": "^3.5.2",
        "minimist": "^1.2.0",
        "phantomjs-prebuilt": "^2.1.7",
        "sinon": "^1.17.4",
        "typescript": "^2.0.3",
        "url-search-params": "^0.6.1",
        "webpack": "^1.13.1",
        "webpack-dev-server": "^1.14.1"
    },
    "directories": {},
    "dist": {
        "shasum": "2c9d638b2e191a08ea1d6cc988eadd6ba5bdc053",
        "tarball": "https://registry.npmjs.org/axios/-/axios-0.15.3.tgz"
    },
    "gitHead": "4976816808c4e81acad2393c429832afeaf9664d",
    "homepage": "https://github.com/mzabriskie/axios",
    "keywords": [
        "xhr",
        "http",
        "ajax",
        "promise",
        "node"
    ],
    "license": "MIT",
    "main": "index.js",
    "maintainers": [
        {
            "name": "mzabriskie",
            "email": "mzabriskie@gmail.com"
        },
        {
            "name": "nickuraltsev",
            "email": "nick.uraltsev@gmail.com"
        }
    ],
    "name": "axios",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/mzabriskie/axios.git"
    },
    "scripts": {
        "build": "NODE_ENV=production grunt build",
        "coveralls": "cat coverage/lcov.info | ./node_modules/coveralls/bin/coveralls.js",
        "examples": "node ./examples/server.js",
        "postversion": "git push && git push --tags",
        "preversion": "npm test",
        "start": "node ./sandbox/server.js",
        "test": "grunt test",
        "version": "npm run build && grunt version && git add -A dist && git add CHANGELOG.md bower.json package.json"
    },
    "typings": "./index.d.ts",
    "version": "0.15.3"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module axios](#apidoc.module.axios)
1.  [function <span class="apidocSignatureSpan">axios.</span>Axios (instanceConfig)](#apidoc.element.axios.Axios)
1.  [function <span class="apidocSignatureSpan">axios.</span>Cancel (message)](#apidoc.element.axios.Cancel)
1.  [function <span class="apidocSignatureSpan">axios.</span>CancelToken (executor)](#apidoc.element.axios.CancelToken)
1.  [function <span class="apidocSignatureSpan">axios.</span>all (promises)](#apidoc.element.axios.all)
1.  [function <span class="apidocSignatureSpan">axios.</span>create (instanceConfig)](#apidoc.element.axios.create)
1.  [function <span class="apidocSignatureSpan">axios.</span>default ()](#apidoc.element.axios.default)
1.  [function <span class="apidocSignatureSpan">axios.</span>delete ()](#apidoc.element.axios.delete)
1.  [function <span class="apidocSignatureSpan">axios.</span>get ()](#apidoc.element.axios.get)
1.  [function <span class="apidocSignatureSpan">axios.</span>head ()](#apidoc.element.axios.head)
1.  [function <span class="apidocSignatureSpan">axios.</span>isCancel (value)](#apidoc.element.axios.isCancel)
1.  [function <span class="apidocSignatureSpan">axios.</span>patch ()](#apidoc.element.axios.patch)
1.  [function <span class="apidocSignatureSpan">axios.</span>post ()](#apidoc.element.axios.post)
1.  [function <span class="apidocSignatureSpan">axios.</span>put ()](#apidoc.element.axios.put)
1.  [function <span class="apidocSignatureSpan">axios.</span>request ()](#apidoc.element.axios.request)
1.  [function <span class="apidocSignatureSpan">axios.</span>spread (callback)](#apidoc.element.axios.spread)
1.  object <span class="apidocSignatureSpan">axios.</span>Axios.prototype
1.  object <span class="apidocSignatureSpan">axios.</span>Cancel.prototype
1.  object <span class="apidocSignatureSpan">axios.</span>CancelToken.prototype
1.  object <span class="apidocSignatureSpan">axios.</span>defaults
1.  object <span class="apidocSignatureSpan">axios.</span>defaults.transformRequest
1.  object <span class="apidocSignatureSpan">axios.</span>defaults.transformResponse
1.  object <span class="apidocSignatureSpan">axios.</span>interceptors
1.  object <span class="apidocSignatureSpan">axios.</span>utils

#### [module axios.Axios](#apidoc.module.axios.Axios)
1.  [function <span class="apidocSignatureSpan">axios.</span>Axios (instanceConfig)](#apidoc.element.axios.Axios.Axios)

#### [module axios.Axios.prototype](#apidoc.module.axios.Axios.prototype)
1.  [function <span class="apidocSignatureSpan">axios.Axios.prototype.</span>delete (url, config)](#apidoc.element.axios.Axios.prototype.delete)
1.  [function <span class="apidocSignatureSpan">axios.Axios.prototype.</span>get (url, config)](#apidoc.element.axios.Axios.prototype.get)
1.  [function <span class="apidocSignatureSpan">axios.Axios.prototype.</span>head (url, config)](#apidoc.element.axios.Axios.prototype.head)
1.  [function <span class="apidocSignatureSpan">axios.Axios.prototype.</span>patch (url, data, config)](#apidoc.element.axios.Axios.prototype.patch)
1.  [function <span class="apidocSignatureSpan">axios.Axios.prototype.</span>post (url, data, config)](#apidoc.element.axios.Axios.prototype.post)
1.  [function <span class="apidocSignatureSpan">axios.Axios.prototype.</span>put (url, data, config)](#apidoc.element.axios.Axios.prototype.put)
1.  [function <span class="apidocSignatureSpan">axios.Axios.prototype.</span>request (config)](#apidoc.element.axios.Axios.prototype.request)

#### [module axios.Cancel](#apidoc.module.axios.Cancel)
1.  [function <span class="apidocSignatureSpan">axios.</span>Cancel (message)](#apidoc.element.axios.Cancel.Cancel)

#### [module axios.Cancel.prototype](#apidoc.module.axios.Cancel.prototype)
1.  boolean <span class="apidocSignatureSpan">axios.Cancel.prototype.</span>__CANCEL__
1.  [function <span class="apidocSignatureSpan">axios.Cancel.prototype.</span>toString ()](#apidoc.element.axios.Cancel.prototype.toString)

#### [module axios.CancelToken](#apidoc.module.axios.CancelToken)
1.  [function <span class="apidocSignatureSpan">axios.</span>CancelToken (executor)](#apidoc.element.axios.CancelToken.CancelToken)
1.  [function <span class="apidocSignatureSpan">axios.CancelToken.</span>source ()](#apidoc.element.axios.CancelToken.source)

#### [module axios.CancelToken.prototype](#apidoc.module.axios.CancelToken.prototype)
1.  [function <span class="apidocSignatureSpan">axios.CancelToken.prototype.</span>throwIfRequested ()](#apidoc.element.axios.CancelToken.prototype.throwIfRequested)

#### [module axios.defaults](#apidoc.module.axios.defaults)
1.  [function <span class="apidocSignatureSpan">axios.defaults.</span>adapter (config)](#apidoc.element.axios.defaults.adapter)
1.  [function <span class="apidocSignatureSpan">axios.defaults.</span>validateStatus (status)](#apidoc.element.axios.defaults.validateStatus)
1.  number <span class="apidocSignatureSpan">axios.defaults.</span>maxContentLength
1.  number <span class="apidocSignatureSpan">axios.defaults.</span>timeout
1.  object <span class="apidocSignatureSpan">axios.defaults.</span>headers
1.  object <span class="apidocSignatureSpan">axios.defaults.</span>transformRequest
1.  object <span class="apidocSignatureSpan">axios.defaults.</span>transformResponse
1.  string <span class="apidocSignatureSpan">axios.defaults.</span>xsrfCookieName
1.  string <span class="apidocSignatureSpan">axios.defaults.</span>xsrfHeaderName

#### [module axios.defaults.transformRequest](#apidoc.module.axios.defaults.transformRequest)
1.  [function <span class="apidocSignatureSpan">axios.defaults.transformRequest.</span>0 (data, headers)](#apidoc.element.axios.defaults.transformRequest.0)

#### [module axios.defaults.transformResponse](#apidoc.module.axios.defaults.transformResponse)
1.  [function <span class="apidocSignatureSpan">axios.defaults.transformResponse.</span>0 (data)](#apidoc.element.axios.defaults.transformResponse.0)

#### [module axios.utils](#apidoc.module.axios.utils)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>extend (a, b, thisArg)](#apidoc.element.axios.utils.extend)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>forEach (obj, fn)](#apidoc.element.axios.utils.forEach)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>isArray (val)](#apidoc.element.axios.utils.isArray)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>isArrayBuffer (val)](#apidoc.element.axios.utils.isArrayBuffer)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>isArrayBufferView (val)](#apidoc.element.axios.utils.isArrayBufferView)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>isBlob (val)](#apidoc.element.axios.utils.isBlob)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>isDate (val)](#apidoc.element.axios.utils.isDate)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>isFile (val)](#apidoc.element.axios.utils.isFile)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>isFormData (val)](#apidoc.element.axios.utils.isFormData)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>isFunction (val)](#apidoc.element.axios.utils.isFunction)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>isNumber (val)](#apidoc.element.axios.utils.isNumber)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>isObject (val)](#apidoc.element.axios.utils.isObject)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>isStandardBrowserEnv ()](#apidoc.element.axios.utils.isStandardBrowserEnv)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>isStream (val)](#apidoc.element.axios.utils.isStream)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>isString (val)](#apidoc.element.axios.utils.isString)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>isURLSearchParams (val)](#apidoc.element.axios.utils.isURLSearchParams)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>isUndefined (val)](#apidoc.element.axios.utils.isUndefined)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>merge ()](#apidoc.element.axios.utils.merge)
1.  [function <span class="apidocSignatureSpan">axios.utils.</span>trim (str)](#apidoc.element.axios.utils.trim)



# <a name="apidoc.module.axios"></a>[module axios](#apidoc.module.axios)

#### <a name="apidoc.element.axios.Axios"></a>[function <span class="apidocSignatureSpan">axios.</span>Axios (instanceConfig)](#apidoc.element.axios.Axios)
- description and source-code
```javascript
function Axios(instanceConfig) {
  this.defaults = instanceConfig;
  this.interceptors = {
    request: new InterceptorManager(),
    response: new InterceptorManager()
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.Cancel"></a>[function <span class="apidocSignatureSpan">axios.</span>Cancel (message)](#apidoc.element.axios.Cancel)
- description and source-code
```javascript
function Cancel(message) {
  this.message = message;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.CancelToken"></a>[function <span class="apidocSignatureSpan">axios.</span>CancelToken (executor)](#apidoc.element.axios.CancelToken)
- description and source-code
```javascript
function CancelToken(executor) {
  if (typeof executor !== 'function') {
    throw new TypeError('executor must be a function.');
  }

  var resolvePromise;
  this.promise = new Promise(function promiseExecutor(resolve) {
    resolvePromise = resolve;
  });

  var token = this;
  executor(function cancel(message) {
    if (token.reason) {
      // Cancellation has already been requested
      return;
    }

    token.reason = new Cancel(message);
    resolvePromise(token.reason);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.all"></a>[function <span class="apidocSignatureSpan">axios.</span>all (promises)](#apidoc.element.axios.all)
- description and source-code
```javascript
function all(promises) {
  return Promise.all(promises);
}
```
- example usage
```shell
...
  return axios.get('/user/12345');
}

function getUserPermissions() {
  return axios.get('/user/12345/permissions');
}

axios.all([getUserAccount(), getUserPermissions()])
  .then(axios.spread(function (acct, perms) {
    // Both requests are now complete
  }));
'''

## axios API
...
```

#### <a name="apidoc.element.axios.create"></a>[function <span class="apidocSignatureSpan">axios.</span>create (instanceConfig)](#apidoc.element.axios.create)
- description and source-code
```javascript
function create(instanceConfig) {
  return createInstance(utils.merge(defaults, instanceConfig));
}
```
- example usage
```shell
...
##### axios.all(iterable)
##### axios.spread(callback)

### Creating an instance

You can create a new instance of axios with a custom config.

##### axios.create([config])

'''js
var instance = axios.create({
  baseURL: 'https://some-domain.com/api/',
  timeout: 1000,
  headers: {'X-Custom-Header': 'foobar'}
});
...
```

#### <a name="apidoc.element.axios.default"></a>[function <span class="apidocSignatureSpan">axios.</span>default ()](#apidoc.element.axios.default)
- description and source-code
```javascript
function wrap() {
  var args = new Array(arguments.length);
  for (var i = 0; i < args.length; i++) {
    args[i] = arguments[i];
  }
  return fn.apply(thisArg, args);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.delete"></a>[function <span class="apidocSignatureSpan">axios.</span>delete ()](#apidoc.element.axios.delete)
- description and source-code
```javascript
function wrap() {
  var args = new Array(arguments.length);
  for (var i = 0; i < args.length; i++) {
    args[i] = arguments[i];
  }
  return fn.apply(thisArg, args);
}
```
- example usage
```shell
...

### Request method aliases

For convenience aliases have been provided for all supported request methods.

##### axios.request(config)
##### axios.get(url[, config])
##### axios.delete(url[, config])
##### axios.head(url[, config])
##### axios.post(url[, data[, config]])
##### axios.put(url[, data[, config]])
##### axios.patch(url[, data[, config]])

###### NOTE
When using the alias methods 'url', 'method', and 'data' properties don't need to be specified in config.
...
```

#### <a name="apidoc.element.axios.get"></a>[function <span class="apidocSignatureSpan">axios.</span>get ()](#apidoc.element.axios.get)
- description and source-code
```javascript
function wrap() {
  var args = new Array(arguments.length);
  for (var i = 0; i < args.length; i++) {
    args[i] = arguments[i];
  }
  return fn.apply(thisArg, args);
}
```
- example usage
```shell
...

## Example

Performing a 'GET' request

'''js
// Make a request for a user with a given ID
axios.get('/user?ID=12345')
.then(function (response) {
  console.log(response);
})
.catch(function (error) {
  console.log(error);
});
...
```

#### <a name="apidoc.element.axios.head"></a>[function <span class="apidocSignatureSpan">axios.</span>head ()](#apidoc.element.axios.head)
- description and source-code
```javascript
function wrap() {
  var args = new Array(arguments.length);
  for (var i = 0; i < args.length; i++) {
    args[i] = arguments[i];
  }
  return fn.apply(thisArg, args);
}
```
- example usage
```shell
...
### Request method aliases

For convenience aliases have been provided for all supported request methods.

##### axios.request(config)
##### axios.get(url[, config])
##### axios.delete(url[, config])
##### axios.head(url[, config])
##### axios.post(url[, data[, config]])
##### axios.put(url[, data[, config]])
##### axios.patch(url[, data[, config]])

###### NOTE
When using the alias methods 'url', 'method', and 'data' properties don't need to be specified in config.
...
```

#### <a name="apidoc.element.axios.isCancel"></a>[function <span class="apidocSignatureSpan">axios.</span>isCancel (value)](#apidoc.element.axios.isCancel)
- description and source-code
```javascript
function isCancel(value) {
  return !!(value && value.__CANCEL__);
}
```
- example usage
```shell
...
'''js
var CancelToken = axios.CancelToken;
var source = CancelToken.source();

axios.get('/user/12345', {
  cancelToken: source.token
}).catch(function(thrown) {
  if (axios.isCancel(thrown)) {
    console.log('Request canceled', thrown.message);
  } else {
    // handle error
  }
});

// cancel the request (the message parameter is optional)
...
```

#### <a name="apidoc.element.axios.patch"></a>[function <span class="apidocSignatureSpan">axios.</span>patch ()](#apidoc.element.axios.patch)
- description and source-code
```javascript
function wrap() {
  var args = new Array(arguments.length);
  for (var i = 0; i < args.length; i++) {
    args[i] = arguments[i];
  }
  return fn.apply(thisArg, args);
}
```
- example usage
```shell
...

##### axios.request(config)
##### axios.get(url[, config])
##### axios.delete(url[, config])
##### axios.head(url[, config])
##### axios.post(url[, data[, config]])
##### axios.put(url[, data[, config]])
##### axios.patch(url[, data[, config]])

###### NOTE
When using the alias methods 'url', 'method', and 'data' properties don't need to be specified in config.

### Concurrency

Helper functions for dealing with concurrent requests.
...
```

#### <a name="apidoc.element.axios.post"></a>[function <span class="apidocSignatureSpan">axios.</span>post ()](#apidoc.element.axios.post)
- description and source-code
```javascript
function wrap() {
  var args = new Array(arguments.length);
  for (var i = 0; i < args.length; i++) {
    args[i] = arguments[i];
  }
  return fn.apply(thisArg, args);
}
```
- example usage
```shell
...
  console.log(error);
});
'''

Performing a 'POST' request

'''js
axios.post('/user', {
  firstName: 'Fred',
  lastName: 'Flintstone'
})
.then(function (response) {
  console.log(response);
})
.catch(function (error) {
...
```

#### <a name="apidoc.element.axios.put"></a>[function <span class="apidocSignatureSpan">axios.</span>put ()](#apidoc.element.axios.put)
- description and source-code
```javascript
function wrap() {
  var args = new Array(arguments.length);
  for (var i = 0; i < args.length; i++) {
    args[i] = arguments[i];
  }
  return fn.apply(thisArg, args);
}
```
- example usage
```shell
...
For convenience aliases have been provided for all supported request methods.

##### axios.request(config)
##### axios.get(url[, config])
##### axios.delete(url[, config])
##### axios.head(url[, config])
##### axios.post(url[, data[, config]])
##### axios.put(url[, data[, config]])
##### axios.patch(url[, data[, config]])

###### NOTE
When using the alias methods 'url', 'method', and 'data' properties don't need to be specified in config.

### Concurrency
...
```

#### <a name="apidoc.element.axios.request"></a>[function <span class="apidocSignatureSpan">axios.</span>request ()](#apidoc.element.axios.request)
- description and source-code
```javascript
function wrap() {
  var args = new Array(arguments.length);
  for (var i = 0; i < args.length; i++) {
    args[i] = arguments[i];
  }
  return fn.apply(thisArg, args);
}
```
- example usage
```shell
...
axios('/user/12345');
'''

### Request method aliases

For convenience aliases have been provided for all supported request methods.

##### axios.request(config)
##### axios.get(url[, config])
##### axios.delete(url[, config])
##### axios.head(url[, config])
##### axios.post(url[, data[, config]])
##### axios.put(url[, data[, config]])
##### axios.patch(url[, data[, config]])
...
```

#### <a name="apidoc.element.axios.spread"></a>[function <span class="apidocSignatureSpan">axios.</span>spread (callback)](#apidoc.element.axios.spread)
- description and source-code
```javascript
function spread(callback) {
  return function wrap(arr) {
    return callback.apply(null, arr);
  };
}
```
- example usage
```shell
...
}

function getUserPermissions() {
  return axios.get('/user/12345/permissions');
}

axios.all([getUserAccount(), getUserPermissions()])
  .then(axios.spread(function (acct, perms) {
    // Both requests are now complete
  }));
'''

## axios API

Requests can be made by passing the relevant config to 'axios'.
...
```



# <a name="apidoc.module.axios.Axios"></a>[module axios.Axios](#apidoc.module.axios.Axios)

#### <a name="apidoc.element.axios.Axios.Axios"></a>[function <span class="apidocSignatureSpan">axios.</span>Axios (instanceConfig)](#apidoc.element.axios.Axios.Axios)
- description and source-code
```javascript
function Axios(instanceConfig) {
  this.defaults = instanceConfig;
  this.interceptors = {
    request: new InterceptorManager(),
    response: new InterceptorManager()
  };
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.axios.Axios.prototype"></a>[module axios.Axios.prototype](#apidoc.module.axios.Axios.prototype)

#### <a name="apidoc.element.axios.Axios.prototype.delete"></a>[function <span class="apidocSignatureSpan">axios.Axios.prototype.</span>delete (url, config)](#apidoc.element.axios.Axios.prototype.delete)
- description and source-code
```javascript
delete = function (url, config) {
  return this.request(utils.merge(config || {}, {
    method: method,
    url: url
  }));
}
```
- example usage
```shell
...

### Request method aliases

For convenience aliases have been provided for all supported request methods.

##### axios.request(config)
##### axios.get(url[, config])
##### axios.delete(url[, config])
##### axios.head(url[, config])
##### axios.post(url[, data[, config]])
##### axios.put(url[, data[, config]])
##### axios.patch(url[, data[, config]])

###### NOTE
When using the alias methods 'url', 'method', and 'data' properties don't need to be specified in config.
...
```

#### <a name="apidoc.element.axios.Axios.prototype.get"></a>[function <span class="apidocSignatureSpan">axios.Axios.prototype.</span>get (url, config)](#apidoc.element.axios.Axios.prototype.get)
- description and source-code
```javascript
get = function (url, config) {
  return this.request(utils.merge(config || {}, {
    method: method,
    url: url
  }));
}
```
- example usage
```shell
...

## Example

Performing a 'GET' request

'''js
// Make a request for a user with a given ID
axios.get('/user?ID=12345')
.then(function (response) {
  console.log(response);
})
.catch(function (error) {
  console.log(error);
});
...
```

#### <a name="apidoc.element.axios.Axios.prototype.head"></a>[function <span class="apidocSignatureSpan">axios.Axios.prototype.</span>head (url, config)](#apidoc.element.axios.Axios.prototype.head)
- description and source-code
```javascript
head = function (url, config) {
  return this.request(utils.merge(config || {}, {
    method: method,
    url: url
  }));
}
```
- example usage
```shell
...
### Request method aliases

For convenience aliases have been provided for all supported request methods.

##### axios.request(config)
##### axios.get(url[, config])
##### axios.delete(url[, config])
##### axios.head(url[, config])
##### axios.post(url[, data[, config]])
##### axios.put(url[, data[, config]])
##### axios.patch(url[, data[, config]])

###### NOTE
When using the alias methods 'url', 'method', and 'data' properties don't need to be specified in config.
...
```

#### <a name="apidoc.element.axios.Axios.prototype.patch"></a>[function <span class="apidocSignatureSpan">axios.Axios.prototype.</span>patch (url, data, config)](#apidoc.element.axios.Axios.prototype.patch)
- description and source-code
```javascript
patch = function (url, data, config) {
  return this.request(utils.merge(config || {}, {
    method: method,
    url: url,
    data: data
  }));
}
```
- example usage
```shell
...

##### axios.request(config)
##### axios.get(url[, config])
##### axios.delete(url[, config])
##### axios.head(url[, config])
##### axios.post(url[, data[, config]])
##### axios.put(url[, data[, config]])
##### axios.patch(url[, data[, config]])

###### NOTE
When using the alias methods 'url', 'method', and 'data' properties don't need to be specified in config.

### Concurrency

Helper functions for dealing with concurrent requests.
...
```

#### <a name="apidoc.element.axios.Axios.prototype.post"></a>[function <span class="apidocSignatureSpan">axios.Axios.prototype.</span>post (url, data, config)](#apidoc.element.axios.Axios.prototype.post)
- description and source-code
```javascript
post = function (url, data, config) {
  return this.request(utils.merge(config || {}, {
    method: method,
    url: url,
    data: data
  }));
}
```
- example usage
```shell
...
  console.log(error);
});
'''

Performing a 'POST' request

'''js
axios.post('/user', {
  firstName: 'Fred',
  lastName: 'Flintstone'
})
.then(function (response) {
  console.log(response);
})
.catch(function (error) {
...
```

#### <a name="apidoc.element.axios.Axios.prototype.put"></a>[function <span class="apidocSignatureSpan">axios.Axios.prototype.</span>put (url, data, config)](#apidoc.element.axios.Axios.prototype.put)
- description and source-code
```javascript
put = function (url, data, config) {
  return this.request(utils.merge(config || {}, {
    method: method,
    url: url,
    data: data
  }));
}
```
- example usage
```shell
...
For convenience aliases have been provided for all supported request methods.

##### axios.request(config)
##### axios.get(url[, config])
##### axios.delete(url[, config])
##### axios.head(url[, config])
##### axios.post(url[, data[, config]])
##### axios.put(url[, data[, config]])
##### axios.patch(url[, data[, config]])

###### NOTE
When using the alias methods 'url', 'method', and 'data' properties don't need to be specified in config.

### Concurrency
...
```

#### <a name="apidoc.element.axios.Axios.prototype.request"></a>[function <span class="apidocSignatureSpan">axios.Axios.prototype.</span>request (config)](#apidoc.element.axios.Axios.prototype.request)
- description and source-code
```javascript
function request(config) {
<span class="apidocCodeCommentSpan">  /*eslint no-param-reassign:0*/
</span>  // Allow for axios('example/url'[, config]) a la fetch API
  if (typeof config === 'string') {
    config = utils.merge({
      url: arguments[0]
    }, arguments[1]);
  }

  config = utils.merge(defaults, this.defaults, { method: 'get' }, config);

  // Support baseURL config
  if (config.baseURL && !isAbsoluteURL(config.url)) {
    config.url = combineURLs(config.baseURL, config.url);
  }

  // Hook up interceptors middleware
  var chain = [dispatchRequest, undefined];
  var promise = Promise.resolve(config);

  this.interceptors.request.forEach(function unshiftRequestInterceptors(interceptor) {
    chain.unshift(interceptor.fulfilled, interceptor.rejected);
  });

  this.interceptors.response.forEach(function pushResponseInterceptors(interceptor) {
    chain.push(interceptor.fulfilled, interceptor.rejected);
  });

  while (chain.length) {
    promise = promise.then(chain.shift(), chain.shift());
  }

  return promise;
}
```
- example usage
```shell
...
axios('/user/12345');
'''

### Request method aliases

For convenience aliases have been provided for all supported request methods.

##### axios.request(config)
##### axios.get(url[, config])
##### axios.delete(url[, config])
##### axios.head(url[, config])
##### axios.post(url[, data[, config]])
##### axios.put(url[, data[, config]])
##### axios.patch(url[, data[, config]])
...
```



# <a name="apidoc.module.axios.Cancel"></a>[module axios.Cancel](#apidoc.module.axios.Cancel)

#### <a name="apidoc.element.axios.Cancel.Cancel"></a>[function <span class="apidocSignatureSpan">axios.</span>Cancel (message)](#apidoc.element.axios.Cancel.Cancel)
- description and source-code
```javascript
function Cancel(message) {
  this.message = message;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.axios.Cancel.prototype"></a>[module axios.Cancel.prototype](#apidoc.module.axios.Cancel.prototype)

#### <a name="apidoc.element.axios.Cancel.prototype.toString"></a>[function <span class="apidocSignatureSpan">axios.Cancel.prototype.</span>toString ()](#apidoc.element.axios.Cancel.prototype.toString)
- description and source-code
```javascript
function toString() {
  return 'Cancel' + (this.message ? ': ' + this.message : '');
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.axios.CancelToken"></a>[module axios.CancelToken](#apidoc.module.axios.CancelToken)

#### <a name="apidoc.element.axios.CancelToken.CancelToken"></a>[function <span class="apidocSignatureSpan">axios.</span>CancelToken (executor)](#apidoc.element.axios.CancelToken.CancelToken)
- description and source-code
```javascript
function CancelToken(executor) {
  if (typeof executor !== 'function') {
    throw new TypeError('executor must be a function.');
  }

  var resolvePromise;
  this.promise = new Promise(function promiseExecutor(resolve) {
    resolvePromise = resolve;
  });

  var token = this;
  executor(function cancel(message) {
    if (token.reason) {
      // Cancellation has already been requested
      return;
    }

    token.reason = new Cancel(message);
    resolvePromise(token.reason);
  });
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.CancelToken.source"></a>[function <span class="apidocSignatureSpan">axios.CancelToken.</span>source ()](#apidoc.element.axios.CancelToken.source)
- description and source-code
```javascript
function source() {
  var cancel;
  var token = new CancelToken(function executor(c) {
    cancel = c;
  });
  return {
    token: token,
    cancel: cancel
  };
}
```
- example usage
```shell
...

> The axios cancel token API is based on the [cancelable promises proposal](https://github.com/tc39/proposal-cancelable-promises
), which is currently at Stage 1.

You can create a cancel token using the 'CancelToken.source' factory as shown below:

'''js
var CancelToken = axios.CancelToken;
var source = CancelToken.source();

axios.get('/user/12345', {
cancelToken: source.token
}).catch(function(thrown) {
if (axios.isCancel(thrown)) {
  console.log('Request canceled', thrown.message);
} else {
...
```



# <a name="apidoc.module.axios.CancelToken.prototype"></a>[module axios.CancelToken.prototype](#apidoc.module.axios.CancelToken.prototype)

#### <a name="apidoc.element.axios.CancelToken.prototype.throwIfRequested"></a>[function <span class="apidocSignatureSpan">axios.CancelToken.prototype.</span>throwIfRequested ()](#apidoc.element.axios.CancelToken.prototype.throwIfRequested)
- description and source-code
```javascript
function throwIfRequested() {
  if (this.reason) {
    throw this.reason;
  }
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.axios.defaults"></a>[module axios.defaults](#apidoc.module.axios.defaults)

#### <a name="apidoc.element.axios.defaults.adapter"></a>[function <span class="apidocSignatureSpan">axios.defaults.</span>adapter (config)](#apidoc.element.axios.defaults.adapter)
- description and source-code
```javascript
function httpAdapter(config) {
  return new Promise(function dispatchHttpRequest(resolve, reject) {
    var data = config.data;
    var headers = config.headers;
    var timer;
    var aborted = false;

    // Set User-Agent (required by some servers)
    // Only set header if it hasn't been set in config
    // See https://github.com/mzabriskie/axios/issues/69
    if (!headers['User-Agent'] && !headers['user-agent']) {
      headers['User-Agent'] = 'axios/' + pkg.version;
    }

    if (data && !utils.isStream(data)) {
      if (utils.isArrayBuffer(data)) {
        data = new Buffer(new Uint8Array(data));
      } else if (utils.isString(data)) {
        data = new Buffer(data, 'utf-8');
      } else {
        return reject(createError(
          'Data after transformation must be a string, an ArrayBuffer, or a Stream',
          config
        ));
      }

      // Add Content-Length header if data exists
      headers['Content-Length'] = data.length;
    }

    // HTTP basic authentication
    var auth = undefined;
    if (config.auth) {
      var username = config.auth.username || '';
      var password = config.auth.password || '';
      auth = username + ':' + password;
    }

    // Parse url
    var parsed = url.parse(config.url);
    var protocol = parsed.protocol || 'http:';

    if (!auth && parsed.auth) {
      var urlAuth = parsed.auth.split(':');
      var urlUsername = urlAuth[0] || '';
      var urlPassword = urlAuth[1] || '';
      auth = urlUsername + ':' + urlPassword;
    }

    if (auth) {
      delete headers.Authorization;
    }

    var isHttps = protocol === 'https:';
    var agent = isHttps ? config.httpsAgent : config.httpAgent;

    var options = {
      hostname: parsed.hostname,
      port: parsed.port,
      path: buildURL(parsed.path, config.params, config.paramsSerializer).replace(/^\?/, ''),
      method: config.method,
      headers: headers,
      agent: agent,
      auth: auth
    };

    var proxy = config.proxy;
    if (!proxy) {
      var proxyEnv = protocol.slice(0, -1) + '_proxy';
      var proxyUrl = process.env[proxyEnv] || process.env[proxyEnv.toUpperCase()];
      if (proxyUrl) {
        var parsedProxyUrl = url.parse(proxyUrl);
        proxy = {
          host: parsedProxyUrl.hostname,
          port: parsedProxyUrl.port
        };

        if (parsedProxyUrl.auth) {
          var proxyUrlAuth = parsedProxyUrl.auth.split(':');
          proxy.auth = {
            username: proxyUrlAuth[0],
            password: proxyUrlAuth[1]
          };
        }
      }
    }

    if (proxy) {
      options.hostname = proxy.host;
      options.host = proxy.host;
      options.headers.host = parsed.hostname + (parsed.port ? ':' + parsed.port : '');
      options.port = proxy.port;
      options.path = protocol + '//' + parsed.hostname + (parsed.port ? ':' + parsed.port : '') + options.path;

      // Basic proxy authorization
      if (proxy.auth) {
        var base64 = new Buffer(proxy.auth.username + ':' + proxy.auth.password, 'utf8').toString('base64');
        options.headers['Proxy-Authorization'] = 'Basic ' + base64;
      }
    }

    var transport;
    if (config.maxRedirects === 0) {
      transport = isHttps ? https : http;
    } else {
      if (config.maxRedirects) {
        options.maxRedirects = config.maxRedirects;
      }
      transport = isHttps ? httpsFollow : httpFollow;
    }

    // Create the request
    var req = transport.request(options, function handleResponse(res) {
      if (aborted) return;

      // Response has been received so kill timer that handles request timeout
      clearTimeout(timer);
      timer = null;

      // uncompress the response body transparently if required
      var stream = res;
      switch (res.headers['content-encoding']) {
<span class="apidocCodeCommentSpan">      /*eslint default-case:0*/
</span>      case 'gzip':
      case 'compress':
      case 'deflate':
        // add the unzipper to the body stream processing pipeline
        stream = stream.pipe(zlib.createUnzip());

        // remove the content-encoding in order to not confuse downstream operations
        delete r ...
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.defaults.validateStatus"></a>[function <span class="apidocSignatureSpan">axios.defaults.</span>validateStatus (status)](#apidoc.element.axios.defaults.validateStatus)
- description and source-code
```javascript
function validateStatus(status) {
  return status >= 200 && status < 300;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.axios.defaults.transformRequest"></a>[module axios.defaults.transformRequest](#apidoc.module.axios.defaults.transformRequest)

#### <a name="apidoc.element.axios.defaults.transformRequest.0"></a>[function <span class="apidocSignatureSpan">axios.defaults.transformRequest.</span>0 (data, headers)](#apidoc.element.axios.defaults.transformRequest.0)
- description and source-code
```javascript
function transformRequest(data, headers) {
  normalizeHeaderName(headers, 'Content-Type');
  if (utils.isFormData(data) ||
    utils.isArrayBuffer(data) ||
    utils.isStream(data) ||
    utils.isFile(data) ||
    utils.isBlob(data)
  ) {
    return data;
  }
  if (utils.isArrayBufferView(data)) {
    return data.buffer;
  }
  if (utils.isURLSearchParams(data)) {
    setContentTypeIfUnset(headers, 'application/x-www-form-urlencoded;charset=utf-8');
    return data.toString();
  }
  if (utils.isObject(data)) {
    setContentTypeIfUnset(headers, 'application/json;charset=utf-8');
    return JSON.stringify(data);
  }
  return data;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.axios.defaults.transformResponse"></a>[module axios.defaults.transformResponse](#apidoc.module.axios.defaults.transformResponse)

#### <a name="apidoc.element.axios.defaults.transformResponse.0"></a>[function <span class="apidocSignatureSpan">axios.defaults.transformResponse.</span>0 (data)](#apidoc.element.axios.defaults.transformResponse.0)
- description and source-code
```javascript
function transformResponse(data) {
<span class="apidocCodeCommentSpan">  /*eslint no-param-reassign:0*/
</span>  if (typeof data === 'string') {
    data = data.replace(PROTECTION_PREFIX, '');
    try {
      data = JSON.parse(data);
    } catch (e) { /* Ignore */ }
  }
  return data;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.axios.utils"></a>[module axios.utils](#apidoc.module.axios.utils)

#### <a name="apidoc.element.axios.utils.extend"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>extend (a, b, thisArg)](#apidoc.element.axios.utils.extend)
- description and source-code
```javascript
function extend(a, b, thisArg) {
  forEach(b, function assignValue(val, key) {
    if (thisArg && typeof val === 'function') {
      a[key] = bind(val, thisArg);
    } else {
      a[key] = val;
    }
  });
  return a;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.forEach"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>forEach (obj, fn)](#apidoc.element.axios.utils.forEach)
- description and source-code
```javascript
function forEach(obj, fn) {
  // Don't bother if no value provided
  if (obj === null || typeof obj === 'undefined') {
    return;
  }

  // Force an array if not already something iterable
  if (typeof obj !== 'object' && !isArray(obj)) {
<span class="apidocCodeCommentSpan">    /*eslint no-param-reassign:0*/
</span>    obj = [obj];
  }

  if (isArray(obj)) {
    // Iterate over array values
    for (var i = 0, l = obj.length; i < l; i++) {
      fn.call(null, obj[i], i, obj);
    }
  } else {
    // Iterate over object keys
    for (var key in obj) {
      if (Object.prototype.hasOwnProperty.call(obj, key)) {
        fn.call(null, obj[key], key, obj);
      }
    }
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.isArray"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>isArray (val)](#apidoc.element.axios.utils.isArray)
- description and source-code
```javascript
function isArray(val) {
  return toString.call(val) === '[object Array]';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.isArrayBuffer"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>isArrayBuffer (val)](#apidoc.element.axios.utils.isArrayBuffer)
- description and source-code
```javascript
function isArrayBuffer(val) {
  return toString.call(val) === '[object ArrayBuffer]';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.isArrayBufferView"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>isArrayBufferView (val)](#apidoc.element.axios.utils.isArrayBufferView)
- description and source-code
```javascript
function isArrayBufferView(val) {
  var result;
  if ((typeof ArrayBuffer !== 'undefined') && (ArrayBuffer.isView)) {
    result = ArrayBuffer.isView(val);
  } else {
    result = (val) && (val.buffer) && (val.buffer instanceof ArrayBuffer);
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.isBlob"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>isBlob (val)](#apidoc.element.axios.utils.isBlob)
- description and source-code
```javascript
function isBlob(val) {
  return toString.call(val) === '[object Blob]';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.isDate"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>isDate (val)](#apidoc.element.axios.utils.isDate)
- description and source-code
```javascript
function isDate(val) {
  return toString.call(val) === '[object Date]';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.isFile"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>isFile (val)](#apidoc.element.axios.utils.isFile)
- description and source-code
```javascript
function isFile(val) {
  return toString.call(val) === '[object File]';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.isFormData"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>isFormData (val)](#apidoc.element.axios.utils.isFormData)
- description and source-code
```javascript
function isFormData(val) {
  return (typeof FormData !== 'undefined') && (val instanceof FormData);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.isFunction"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>isFunction (val)](#apidoc.element.axios.utils.isFunction)
- description and source-code
```javascript
function isFunction(val) {
  return toString.call(val) === '[object Function]';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.isNumber"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>isNumber (val)](#apidoc.element.axios.utils.isNumber)
- description and source-code
```javascript
function isNumber(val) {
  return typeof val === 'number';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.isObject"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>isObject (val)](#apidoc.element.axios.utils.isObject)
- description and source-code
```javascript
function isObject(val) {
  return val !== null && typeof val === 'object';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.isStandardBrowserEnv"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>isStandardBrowserEnv ()](#apidoc.element.axios.utils.isStandardBrowserEnv)
- description and source-code
```javascript
function isStandardBrowserEnv() {
  return (
    typeof window !== 'undefined' &&
    typeof document !== 'undefined' &&
    typeof document.createElement === 'function'
  );
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.isStream"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>isStream (val)](#apidoc.element.axios.utils.isStream)
- description and source-code
```javascript
function isStream(val) {
  return isObject(val) && isFunction(val.pipe);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.isString"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>isString (val)](#apidoc.element.axios.utils.isString)
- description and source-code
```javascript
function isString(val) {
  return typeof val === 'string';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.isURLSearchParams"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>isURLSearchParams (val)](#apidoc.element.axios.utils.isURLSearchParams)
- description and source-code
```javascript
function isURLSearchParams(val) {
  return typeof URLSearchParams !== 'undefined' && val instanceof URLSearchParams;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.isUndefined"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>isUndefined (val)](#apidoc.element.axios.utils.isUndefined)
- description and source-code
```javascript
function isUndefined(val) {
  return typeof val === 'undefined';
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.merge"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>merge ()](#apidoc.element.axios.utils.merge)
- description and source-code
```javascript
function merge() {
  var result = {};
  function assignValue(val, key) {
    if (typeof result[key] === 'object' && typeof val === 'object') {
      result[key] = merge(result[key], val);
    } else {
      result[key] = val;
    }
  }

  for (var i = 0, l = arguments.length; i < l; i++) {
    forEach(arguments[i], assignValue);
  }
  return result;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.axios.utils.trim"></a>[function <span class="apidocSignatureSpan">axios.utils.</span>trim (str)](#apidoc.element.axios.utils.trim)
- description and source-code
```javascript
function trim(str) {
  return str.replace(/^\s*/, '').replace(/\s*$/, '');
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

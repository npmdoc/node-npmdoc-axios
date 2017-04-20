# npmdoc-axios

#### api documentation for  [axios (v0.16.1)](https://github.com/mzabriskie/axios)  [![npm package](https://img.shields.io/npm/v/npmdoc-axios.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-axios) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-axios.svg)](https://travis-ci.org/npmdoc/node-npmdoc-axios)

#### Promise based HTTP client for the browser and node.js

[![NPM](https://nodei.co/npm/axios.png?downloads=true&downloadRank=true&stars=true)](https://www.npmjs.com/package/axios)

- [https://npmdoc.github.io/node-npmdoc-axios/build/apidoc.html](https://npmdoc.github.io/node-npmdoc-axios/build/apidoc.html)

[![apidoc](https://npmdoc.github.io/node-npmdoc-axios/build/screenCapture.buildCi.browser.%252Ftmp%252Fbuild%252Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-axios/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-axios/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-axios/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "name": "axios",
    "version": "0.16.1",
    "description": "Promise based HTTP client for the browser and node.js",
    "main": "index.js",
    "scripts": {
        "test": "grunt test",
        "start": "node ./sandbox/server.js",
        "build": "NODE_ENV=production grunt build",
        "preversion": "npm test",
        "version": "npm run build && grunt version && git add -A dist && git add CHANGELOG.md bower.json package.json",
        "postversion": "git push && git push --tags",
        "examples": "node ./examples/server.js",
        "coveralls": "cat coverage/lcov.info | ./node_modules/coveralls/bin/coveralls.js"
    },
    "repository": {
        "type": "git",
        "url": "https://github.com/mzabriskie/axios.git"
    },
    "keywords": [
        "xhr",
        "http",
        "ajax",
        "promise",
        "node"
    ],
    "author": "Matt Zabriskie",
    "license": "MIT",
    "bugs": {
        "url": "https://github.com/mzabriskie/axios/issues"
    },
    "homepage": "https://github.com/mzabriskie/axios",
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
        "webpack": "^1.13.1",
        "webpack-dev-server": "^1.14.1",
        "url-search-params": "^0.6.1",
        "typescript": "^2.0.3"
    },
    "browser": {
        "./lib/adapters/http.js": "./lib/adapters/xhr.js"
    },
    "typings": "./index.d.ts",
    "dependencies": {
        "follow-redirects": "^1.2.3"
    }
}
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

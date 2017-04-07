# api documentation for  [js-csp (v0.9.2)](https://github.com/ubolonton/js-csp#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-js-csp.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-js-csp) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-js-csp.svg)](https://travis-ci.org/npmdoc/node-npmdoc-js-csp)
#### CSP channels with ES6 generators, inspired by Clojurescript's core.async and Go

[![NPM](https://nodei.co/npm/js-csp.png?downloads=true)](https://www.npmjs.com/package/js-csp)

[![apidoc](https://npmdoc.github.io/node-npmdoc-js-csp/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-js-csp_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-js-csp/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-js-csp/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-js-csp/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Nguyễn Tuấn Anh",
        "email": "ubolonton@gmail.com"
    },
    "browserify": {
        "transform": [
            "loose-envify"
        ]
    },
    "bugs": {
        "url": "https://github.com/ubolonton/js-csp/issues",
        "email": "ubolonton@gmail.com"
    },
    "dependencies": {
        "babel-runtime": "^6.22.0",
        "lodash": "^4.17.4"
    },
    "description": "CSP channels with ES6 generators, inspired by Clojurescript's core.async and Go",
    "devDependencies": {
        "babel-cli": "^6.22.2",
        "babel-core": "^6.22.1",
        "babel-eslint": "^7.1.1",
        "babel-loader": "^6.2.10",
        "babel-plugin-rewire": "^1.0.0",
        "babel-plugin-transform-flow-strip-types": "^6.22.0",
        "babel-plugin-transform-runtime": "^6.22.0",
        "babel-preset-es2015": "^6.22.0",
        "babel-preset-stage-0": "^6.22.0",
        "babel-template": "^6.22.0",
        "babel-types": "^6.22.0",
        "chai": "^3.5.0",
        "chokidar-cli": "^1.2.0",
        "cross-env": "^3.1.4",
        "eslint": "^3.15.0",
        "eslint-config-airbnb": "^14.1.0",
        "eslint-import-resolver-webpack": "^0.8.1",
        "eslint-loader": "^1.6.1",
        "eslint-plugin-babel": "^4.0.1",
        "eslint-plugin-flowtype": "^2.30.0",
        "eslint-plugin-import": "^2.2.0",
        "eslint-plugin-jsx-a11y": "^4.0.0",
        "eslint-plugin-mocha": "^4.8.0",
        "eslint-plugin-react": "^6.9.0",
        "eslint-watch": "^2.1.14",
        "flow-bin": "^0.38.0",
        "istanbul": "^1.1.0-alpha.1",
        "jsdom": "^9.10.0",
        "jsdom-global": "^2.1.1",
        "mocha": "^3.2.0",
        "ncp": "^2.0.0",
        "rimraf": "^2.5.4",
        "transducers.js": "^0.3.2",
        "webpack": "^2.2.1"
    },
    "directories": {},
    "dist": {
        "shasum": "19dd97965942694098db095beb632b2a95139214",
        "tarball": "https://registry.npmjs.org/js-csp/-/js-csp-0.9.2.tgz"
    },
    "engines": {
        "node": ">= 4.1.0",
        "npm": ">=3.0.0"
    },
    "files": [
        "lib",
        "es",
        "build",
        "src",
        "CHANGELOG.md",
        "README.md"
    ],
    "gitHead": "0388e5e6b1455bdfc60d8f68f4f6f30e37f7afb0",
    "homepage": "https://github.com/ubolonton/js-csp#readme",
    "jsnext:main": "./es/csp.js",
    "keywords": [
        "async",
        "channel",
        "clojure",
        "clojurescript",
        "concurrency",
        "core.async",
        "coroutines",
        "csp",
        "es6",
        "generators",
        "go",
        "yield"
    ],
    "license": {
        "type": "MIT",
        "url": "https://github.com/ubolonton/js-csp/raw/master/LICENSE"
    },
    "main": "./lib/csp.js",
    "maintainers": [
        {
            "name": "colorvisa",
            "email": "colorvisavn@gmail.com"
        },
        {
            "name": "ubolonton",
            "email": "ubolonton@gmail.com"
        }
    ],
    "module": "./es/csp.js",
    "name": "js-csp",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/ubolonton/js-csp.git"
    },
    "scripts": {
        "babel:es": "babel -d es src",
        "babel:node": "babel -d lib src",
        "build": "npm run build:node && npm run build:es && npm run build:browser",
        "build:browser": "webpack --config webpack.config.js",
        "build:es": "node -e \"require('ncp').ncp('./src', './es')\" && cross-env ES_PRESETS=true BABEL_ENV=production npm run babel:es",
        "build:node": "node -e \"require('ncp').ncp('./src', './lib')\" && cross-env BABEL_ENV=production npm run babel:node",
        "clean": "rimraf lib build",
        "flow:status": "flow status; test $? -eq 0 -o $? -eq 2",
        "flow:stop": "flow stop",
        "flow:watch": "npm run flow:status && chokidar './src/**/*.js' './test/**/*.js' -c 'npm run flow:status'",
        "lint": "esw -w './src/**/*.js' './test/**/*.js'",
        "prepublish": "npm run build",
        "test": "mocha",
        "test:coverage": "istanbul cover node_modules/mocha/bin/_mocha",
        "test:watch": "mocha --watch --reporter progress"
    },
    "version": "0.9.2"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module js-csp](#apidoc.module.js-csp)
1.  [function <span class="apidocSignatureSpan">js-csp.</span>alts (operations, options)](#apidoc.element.js-csp.alts)
1.  [function <span class="apidocSignatureSpan">js-csp.</span>chan (bufferOrNumber, xform, exHandler)](#apidoc.element.js-csp.chan)
1.  [function <span class="apidocSignatureSpan">js-csp.</span>go (f)](#apidoc.element.js-csp.go)
1.  [function <span class="apidocSignatureSpan">js-csp.</span>offer (channel, value)](#apidoc.element.js-csp.offer)
1.  [function <span class="apidocSignatureSpan">js-csp.</span>operations.mix (out)](#apidoc.element.js-csp.operations.mix)
1.  [function <span class="apidocSignatureSpan">js-csp.</span>operations.mult (ch)](#apidoc.element.js-csp.operations.mult)
1.  [function <span class="apidocSignatureSpan">js-csp.</span>operations.pub (ch, topicFn)](#apidoc.element.js-csp.operations.pub)
1.  [function <span class="apidocSignatureSpan">js-csp.</span>poll (channel)](#apidoc.element.js-csp.poll)
1.  [function <span class="apidocSignatureSpan">js-csp.</span>promiseChan (xform, exHandler)](#apidoc.element.js-csp.promiseChan)
1.  [function <span class="apidocSignatureSpan">js-csp.</span>put (channel, value)](#apidoc.element.js-csp.put)
1.  [function <span class="apidocSignatureSpan">js-csp.</span>putAsync (channel, value, callback)](#apidoc.element.js-csp.putAsync)
1.  [function <span class="apidocSignatureSpan">js-csp.</span>sleep (msecs)](#apidoc.element.js-csp.sleep)
1.  [function <span class="apidocSignatureSpan">js-csp.</span>spawn (gen)](#apidoc.element.js-csp.spawn)
1.  [function <span class="apidocSignatureSpan">js-csp.</span>take (channel)](#apidoc.element.js-csp.take)
1.  [function <span class="apidocSignatureSpan">js-csp.</span>takeAsync (channel, callback)](#apidoc.element.js-csp.takeAsync)
1.  [function <span class="apidocSignatureSpan">js-csp.</span>timeout (msecs)](#apidoc.element.js-csp.timeout)
1.  object <span class="apidocSignatureSpan">js-csp.</span>CLOSED
1.  object <span class="apidocSignatureSpan">js-csp.</span>DEFAULT
1.  object <span class="apidocSignatureSpan">js-csp.</span>buffers
1.  object <span class="apidocSignatureSpan">js-csp.</span>csp_core
1.  object <span class="apidocSignatureSpan">js-csp.</span>csp_operations
1.  object <span class="apidocSignatureSpan">js-csp.</span>operations
1.  string <span class="apidocSignatureSpan">js-csp.</span>NO_VALUE

#### [module js-csp.DEFAULT](#apidoc.module.js-csp.DEFAULT)
1.  [function <span class="apidocSignatureSpan">js-csp.DEFAULT.</span>toString ()](#apidoc.element.js-csp.DEFAULT.toString)

#### [module js-csp.buffers](#apidoc.module.js-csp.buffers)
1.  [function <span class="apidocSignatureSpan">js-csp.buffers.</span>dropping (n)](#apidoc.element.js-csp.buffers.dropping)
1.  [function <span class="apidocSignatureSpan">js-csp.buffers.</span>fixed (n)](#apidoc.element.js-csp.buffers.fixed)
1.  [function <span class="apidocSignatureSpan">js-csp.buffers.</span>promise ()](#apidoc.element.js-csp.buffers.promise)
1.  [function <span class="apidocSignatureSpan">js-csp.buffers.</span>sliding (n)](#apidoc.element.js-csp.buffers.sliding)

#### [module js-csp.csp_core](#apidoc.module.js-csp.csp_core)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_core.</span>chan (bufferOrNumber, xform, exHandler)](#apidoc.element.js-csp.csp_core.chan)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_core.</span>go (f)](#apidoc.element.js-csp.csp_core.go)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_core.</span>promiseChan (xform, exHandler)](#apidoc.element.js-csp.csp_core.promiseChan)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_core.</span>spawn (gen)](#apidoc.element.js-csp.csp_core.spawn)

#### [module js-csp.csp_operations](#apidoc.module.js-csp.csp_operations)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>filterFrom (p, ch, bufferOrN)](#apidoc.element.js-csp.csp_operations.filterFrom)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>filterInto (p, ch)](#apidoc.element.js-csp.csp_operations.filterInto)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>fromColl (coll)](#apidoc.element.js-csp.csp_operations.fromColl)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>into (coll, ch)](#apidoc.element.js-csp.csp_operations.into)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>map (f, chs, bufferOrN)](#apidoc.element.js-csp.csp_operations.map)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>mapFrom (f, ch)](#apidoc.element.js-csp.csp_operations.mapFrom)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>mapInto (f, ch)](#apidoc.element.js-csp.csp_operations.mapInto)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>mapcatFrom (f, ch, bufferOrN)](#apidoc.element.js-csp.csp_operations.mapcatFrom)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>mapcatInto (f, ch, bufferOrN)](#apidoc.element.js-csp.csp_operations.mapcatInto)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>merge (chs, bufferOrN)](#apidoc.element.js-csp.csp_operations.merge)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>mix (out)](#apidoc.element.js-csp.csp_operations.mix)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>mult (ch)](#apidoc.element.js-csp.csp_operations.mult)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>onto (ch, coll, keepOpen)](#apidoc.element.js-csp.csp_operations.onto)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>partition (n, ch, bufferOrN)](#apidoc.element.js-csp.csp_operations.partition)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>partitionBy (f, ch, bufferOrN)](#apidoc.element.js-csp.csp_operations.partitionBy)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>pipe (src, dst, keepOpen)](#apidoc.element.js-csp.csp_operations.pipe)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>pipeline (to, xf, from, keepOpen, exHandler)](#apidoc.element.js-csp.csp_operations.pipeline)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>pipelineAsync (n, to, af, from, keepOpen)](#apidoc.element.js-csp.csp_operations.pipelineAsync)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>pub (ch, topicFn)](#apidoc.element.js-csp.csp_operations.pub)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>reduce (f, init, ch)](#apidoc.element.js-csp.csp_operations.reduce)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>removeFrom (p, ch)](#apidoc.element.js-csp.csp_operations.removeFrom)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>removeInto (p, ch)](#apidoc.element.js-csp.csp_operations.removeInto)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>split (p, ch, trueBufferOrN, falseBufferOrN)](#apidoc.element.js-csp.csp_operations.split)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>take (n, ch, bufferOrN)](#apidoc.element.js-csp.csp_operations.take)
1.  [function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>unique (ch, bufferOrN)](#apidoc.element.js-csp.csp_operations.unique)

#### [module js-csp.operations](#apidoc.module.js-csp.operations)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>filterFrom (p, ch, bufferOrN)](#apidoc.element.js-csp.operations.filterFrom)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>filterInto (p, ch)](#apidoc.element.js-csp.operations.filterInto)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>fromColl (coll)](#apidoc.element.js-csp.operations.fromColl)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>into (coll, ch)](#apidoc.element.js-csp.operations.into)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>map (f, chs, bufferOrN)](#apidoc.element.js-csp.operations.map)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>mapFrom (f, ch)](#apidoc.element.js-csp.operations.mapFrom)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>mapInto (f, ch)](#apidoc.element.js-csp.operations.mapInto)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>mapcatFrom (f, ch, bufferOrN)](#apidoc.element.js-csp.operations.mapcatFrom)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>mapcatInto (f, ch, bufferOrN)](#apidoc.element.js-csp.operations.mapcatInto)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>merge (chs, bufferOrN)](#apidoc.element.js-csp.operations.merge)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>mix (out)](#apidoc.element.js-csp.operations.mix)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>mult (ch)](#apidoc.element.js-csp.operations.mult)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>onto (ch, coll, keepOpen)](#apidoc.element.js-csp.operations.onto)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>partition (n, ch, bufferOrN)](#apidoc.element.js-csp.operations.partition)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>partitionBy (f, ch, bufferOrN)](#apidoc.element.js-csp.operations.partitionBy)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>pipe (src, dst, keepOpen)](#apidoc.element.js-csp.operations.pipe)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>pipeline (to, xf, from, keepOpen, exHandler)](#apidoc.element.js-csp.operations.pipeline)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>pipelineAsync (n, to, af, from, keepOpen)](#apidoc.element.js-csp.operations.pipelineAsync)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>pub (ch, topicFn)](#apidoc.element.js-csp.operations.pub)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>reduce (f, init, ch)](#apidoc.element.js-csp.operations.reduce)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>removeFrom (p, ch)](#apidoc.element.js-csp.operations.removeFrom)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>removeInto (p, ch)](#apidoc.element.js-csp.operations.removeInto)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>split (p, ch, trueBufferOrN, falseBufferOrN)](#apidoc.element.js-csp.operations.split)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>take (n, ch, bufferOrN)](#apidoc.element.js-csp.operations.take)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>unique (ch, bufferOrN)](#apidoc.element.js-csp.operations.unique)

#### [module js-csp.operations.mix](#apidoc.module.js-csp.operations.mix)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>mix (out)](#apidoc.element.js-csp.operations.mix.mix)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.mix.</span>add (m, ch)](#apidoc.element.js-csp.operations.mix.add)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.mix.</span>remove (m, ch)](#apidoc.element.js-csp.operations.mix.remove)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.mix.</span>removeAll (m)](#apidoc.element.js-csp.operations.mix.removeAll)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.mix.</span>setSoloMode (m, mode)](#apidoc.element.js-csp.operations.mix.setSoloMode)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.mix.</span>toggle (m, updateStateList)](#apidoc.element.js-csp.operations.mix.toggle)

#### [module js-csp.operations.mult](#apidoc.module.js-csp.operations.mult)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>mult (ch)](#apidoc.element.js-csp.operations.mult.mult)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.mult.</span>tap (m, ch, keepOpen)](#apidoc.element.js-csp.operations.mult.tap)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.mult.</span>untap (m, ch)](#apidoc.element.js-csp.operations.mult.untap)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.mult.</span>untapAll (m)](#apidoc.element.js-csp.operations.mult.untapAll)

#### [module js-csp.operations.pub](#apidoc.module.js-csp.operations.pub)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.</span>pub (ch, topicFn)](#apidoc.element.js-csp.operations.pub.pub)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.pub.</span>sub (p, topic, ch, keepOpen)](#apidoc.element.js-csp.operations.pub.sub)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.pub.</span>unsub (p, topic, ch)](#apidoc.element.js-csp.operations.pub.unsub)
1.  [function <span class="apidocSignatureSpan">js-csp.operations.pub.</span>unsubAll (p, topic)](#apidoc.element.js-csp.operations.pub.unsubAll)



# <a name="apidoc.module.js-csp"></a>[module js-csp](#apidoc.module.js-csp)

#### <a name="apidoc.element.js-csp.alts"></a>[function <span class="apidocSignatureSpan">js-csp.</span>alts (operations, options)](#apidoc.element.js-csp.alts)
- description and source-code
```javascript
function alts(operations, options) {
  return new _instruction.AltsInstruction(operations, options);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.chan"></a>[function <span class="apidocSignatureSpan">js-csp.</span>chan (bufferOrNumber, xform, exHandler)](#apidoc.element.js-csp.chan)
- description and source-code
```javascript
function chan(bufferOrNumber, xform, exHandler) {
  if (typeof bufferOrNumber === 'number') {
    return (0, _channels.chan)(bufferOrNumber === 0 ? null : (0, _buffers.fixed)(bufferOrNumber), xform, exHandler);
  }

  return (0, _channels.chan)(bufferOrNumber, xform, exHandler);
}
```
- example usage
```shell
...

  yield csp.timeout(100);
  yield csp.put(table, ball);
}
}

csp.go(function* () {
const table = csp.chan();

csp.go(player, ["ping", table]);
csp.go(player, ["pong", table]);

yield csp.put(table, {hits: 0});
yield csp.timeout(1000);
...
```

#### <a name="apidoc.element.js-csp.go"></a>[function <span class="apidocSignatureSpan">js-csp.</span>go (f)](#apidoc.element.js-csp.go)
- description and source-code
```javascript
function go(f) {
  var args = arguments.length > 1 && arguments[1] !== undefined ? arguments[1] : [];

  return spawn(f.apply(undefined, (0, _toConsumableArray3.default)(args)));
}
```
- example usage
```shell
...
  console.log('${name} ${ball.hits}');

  yield csp.timeout(100);
  yield csp.put(table, ball);
}
}

csp.go(function* () {
const table = csp.chan();

csp.go(player, ["ping", table]);
csp.go(player, ["pong", table]);

yield csp.put(table, {hits: 0});
yield csp.timeout(1000);
...
```

#### <a name="apidoc.element.js-csp.offer"></a>[function <span class="apidocSignatureSpan">js-csp.</span>offer (channel, value)](#apidoc.element.js-csp.offer)
- description and source-code
```javascript
function offer(channel, value) {
  if (channel.closed) {
    return false;
  }

  var result = channel.put(value, new _handlers.FnHandler(false));

  return result instanceof _boxes.Box;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.mix"></a>[function <span class="apidocSignatureSpan">js-csp.</span>operations.mix (out)](#apidoc.element.js-csp.operations.mix)
- description and source-code
```javascript
function mix(out) {
  var m = new Mix(out);
  (0, _csp.go)(_regenerator2.default.mark(function _callee13() {
    var state, result, _value, channel, solos, stillOpen;

    return _regenerator2.default.wrap(function _callee13$(_context15) {
      while (1) {
        switch (_context15.prev = _context15.next) {
          case 0:
            state = m._getAllState();

          case 1:
            _context15.next = 3;
            return (0, _process.alts)(state.reads);

          case 3:
            result = _context15.sent;
            _value = result.value;
            channel = result.channel;

            if (!(_value === _channels.CLOSED)) {
              _context15.next = 11;
              break;
            }

            delete m.stateMap[chanId(channel)];
            state = m._getAllState();
            _context15.next = 22;
            break;

          case 11:
            if (!(channel === m.change)) {
              _context15.next = 15;
              break;
            }

            state = m._getAllState();
            _context15.next = 22;
            break;

          case 15:
            solos = state.solos;

            if (!(solos.indexOf(channel) > -1 || solos.length === 0 && !(state.mutes.indexOf(channel) > -1))) {
              _context15.next = 22;
              break;
            }

            _context15.next = 19;
            return (0, _process.put)(out, _value);

          case 19:
            stillOpen = _context15.sent;

            if (stillOpen) {
              _context15.next = 22;
              break;
            }

            return _context15.abrupt('break', 24);

          case 22:
            _context15.next = 1;
            break;

          case 24:
          case 'end':
            return _context15.stop();
        }
      }
    }, _callee13, this);
  }));
  return m;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.mult"></a>[function <span class="apidocSignatureSpan">js-csp.</span>operations.mult (ch)](#apidoc.element.js-csp.operations.mult)
- description and source-code
```javascript
function mult(ch) {
  var m = new Mult(ch);
  var dchan = (0, _csp.chan)(1);
  var dcount = void 0;

  function makeDoneCallback(tap) {
    return function (stillOpen) {
      dcount -= 1;
      if (dcount === 0) {
        (0, _process.putThenCallback)(dchan, true);
      }
      if (!stillOpen) {
        m.untap(tap.channel);
      }
    };
  }

  (0, _csp.go)(_regenerator2.default.mark(function _callee12() {
    var _this = this;

    var _loop, _ret;

    return _regenerator2.default.wrap(function _callee12$(_context14) {
      while (1) {
        switch (_context14.prev = _context14.next) {
          case 0:
            _loop = _regenerator2.default.mark(function _loop() {
              var value, taps, t, initDcount;
              return _regenerator2.default.wrap(function _loop$(_context13) {
                while (1) {
                  switch (_context13.prev = _context13.next) {
                    case 0:
                      _context13.next = 2;
                      return (0, _process.take)(ch);

                    case 2:
                      value = _context13.sent;
                      taps = m.taps;
                      t = void 0;

                      if (!(value === _channels.CLOSED)) {
                        _context13.next = 9;
                        break;
                      }

                      (0, _keys2.default)(taps).forEach(function (id) {
                        t = taps[id];
                        if (!t.keepOpen) {
                          t.channel.close();
                        }
                      });

                      // TODO: Is this necessary?
                      m.untapAll();
                      return _context13.abrupt('return', 'break');

                    case 9:
                      dcount = (0, _keys2.default)(taps).length;
                      // XXX: This is because putAsync can actually call back
                      // immediately. Fix that
                      initDcount = dcount;
                      // Put value on tapping channels...

                      (0, _keys2.default)(taps).forEach(function (id) {
                        t = taps[id];
                        (0, _process.putThenCallback)(t.channel, value, makeDoneCallback(t));
                      });
                      // ... waiting for all puts to complete

                      if (!(initDcount > 0)) {
                        _context13.next = 15;
                        break;
                      }

                      _context13.next = 15;
                      return (0, _process.take)(dchan);

                    case 15:
                    case 'end':
                      return _context13.stop();
                  }
                }
              }, _loop, _this);
            });

          case 1:
            return _context14.delegateYield(_loop(), 't0', 2);

          case 2:
            _ret = _context14.t0;

            if (!(_ret === 'break')) {
              _context14.next = 5;
              break;
            }

            return _context14.abrupt('break', 7);

          case 5:
            _context14.next = 1;
            break;

          case 7:
          case 'end':
            return _context14.stop();
        }
      }
    }, _callee12, this);
  }));
  return m;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.pub"></a>[function <span class="apidocSignatureSpan">js-csp.</span>operations.pub (ch, topicFn)](#apidoc.element.js-csp.operations.pub)
- description and source-code
```javascript
function pub(ch, topicFn) {
  var bufferFn = arguments.length > 2 && arguments[2] !== undefined ? arguments[2] : constantlyNull;

  var p = new Pub(ch, topicFn, bufferFn);
  (0, _csp.go)(_regenerator2.default.mark(function _callee14() {
    var _this3 = this;

    var _loop3, _ret3;

    return _regenerator2.default.wrap(function _callee14$(_context17) {
      while (1) {
        switch (_context17.prev = _context17.next) {
          case 0:
            _loop3 = _regenerator2.default.mark(function _loop3() {
              var value, mults, topic, m, stillOpen;
              return _regenerator2.default.wrap(function _loop3$(_context16) {
                while (1) {
                  switch (_context16.prev = _context16.next) {
                    case 0:
                      _context16.next = 2;
                      return (0, _process.take)(ch);

                    case 2:
                      value = _context16.sent;
                      mults = p.mults;

                      if (!(value === _channels.CLOSED)) {
                        _context16.next = 7;
                        break;
                      }

                      (0, _keys2.default)(mults).forEach(function (topic) {
                        mults[topic].muxch().close();
                      });
                      return _context16.abrupt('return', 'break');

                    case 7:
                      // TODO: Somehow ensure/document that this must return a string
                      // (otherwise use proper (hash)maps)
                      topic = topicFn(value);
                      m = mults[topic];

                      if (!m) {
                        _context16.next = 14;
                        break;
                      }

                      _context16.next = 12;
                      return (0, _process.put)(m.muxch(), value);

                    case 12:
                      stillOpen = _context16.sent;

                      if (!stillOpen) {
                        delete mults[topic];
                      }

                    case 14:
                    case 'end':
                      return _context16.stop();
                  }
                }
              }, _loop3, _this3);
            });

          case 1:
            return _context17.delegateYield(_loop3(), 't0', 2);

          case 2:
            _ret3 = _context17.t0;

            if (!(_ret3 === 'break')) {
              _context17.next = 5;
              break;
            }

            return _context17.abrupt('break', 7);

          case 5:
            _context17.next = 1;
            break;

          case 7:
          case 'end':
            return _context17.stop();
        }
      }
    }, _callee14, this);
  }));
  return p;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.poll"></a>[function <span class="apidocSignatureSpan">js-csp.</span>poll (channel)](#apidoc.element.js-csp.poll)
- description and source-code
```javascript
function poll(channel) {
  if (channel.closed) {
    return NO_VALUE;
  }

  var result = channel.take(new _handlers.FnHandler(false));

  return result ? result.value : NO_VALUE;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.promiseChan"></a>[function <span class="apidocSignatureSpan">js-csp.</span>promiseChan (xform, exHandler)](#apidoc.element.js-csp.promiseChan)
- description and source-code
```javascript
function promiseChan(xform, exHandler) {
  return (0, _channels.chan)((0, _buffers.promise)(), xform, exHandler);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.put"></a>[function <span class="apidocSignatureSpan">js-csp.</span>put (channel, value)](#apidoc.element.js-csp.put)
- description and source-code
```javascript
function put(channel, value) {
  return new _instruction.PutInstruction(channel, value);
}
```
- example usage
```shell
...
    return;
  }

  ball.hits += 1;
  console.log('${name} ${ball.hits}');

  yield csp.timeout(100);
  yield csp.put(table, ball);
}
}

csp.go(function* () {
const table = csp.chan();

csp.go(player, ["ping", table]);
...
```

#### <a name="apidoc.element.js-csp.putAsync"></a>[function <span class="apidocSignatureSpan">js-csp.</span>putAsync (channel, value, callback)](#apidoc.element.js-csp.putAsync)
- description and source-code
```javascript
function putThenCallback(channel, value, callback) {
  var result = channel.put(value, new _handlers.FnHandler(true, callback));

  if (result && callback) {
    callback(result.value);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.sleep"></a>[function <span class="apidocSignatureSpan">js-csp.</span>sleep (msecs)](#apidoc.element.js-csp.sleep)
- description and source-code
```javascript
function sleep(msecs) {
  return new _instruction.SleepInstruction(msecs);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.spawn"></a>[function <span class="apidocSignatureSpan">js-csp.</span>spawn (gen)](#apidoc.element.js-csp.spawn)
- description and source-code
```javascript
function spawn(gen) {
  var ch = (0, _channels.chan)((0, _buffers.fixed)(1));
  var process = new _process.Process(gen, function (value) {
    if (value === _channels.CLOSED) {
      ch.close();
    } else {
      (0, _process.putThenCallback)(ch, value, function () {
        return ch.close();
      });
    }
  });

  process.run();
  return ch;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.take"></a>[function <span class="apidocSignatureSpan">js-csp.</span>take (channel)](#apidoc.element.js-csp.take)
- description and source-code
```javascript
function take(channel) {
  return new _instruction.TakeInstruction(channel);
}
```
- example usage
```shell
...
'''

Pingpong (ported from [Go](http://talks.golang.org/2013/advconc.slide#6)).

'''javascript
function* player(name, table) {
  while (true) {
let ball = yield csp.take(table);

if (ball === csp.CLOSED) {
  console.log(name + ": table's gone");
  return;
}

ball.hits += 1;
...
```

#### <a name="apidoc.element.js-csp.takeAsync"></a>[function <span class="apidocSignatureSpan">js-csp.</span>takeAsync (channel, callback)](#apidoc.element.js-csp.takeAsync)
- description and source-code
```javascript
function takeThenCallback(channel, callback) {
  var result = channel.take(new _handlers.FnHandler(true, callback));

  if (result && callback) {
    callback(result.value);
  }
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.timeout"></a>[function <span class="apidocSignatureSpan">js-csp.</span>timeout (msecs)](#apidoc.element.js-csp.timeout)
- description and source-code
```javascript
function timeout(msecs) {
  // eslint-disable-line
  var ch = (0, _channels.chan)();

  (0, _dispatch.queueDelay)(function () {
    return ch.close();
  }, msecs);

  return ch;
}
```
- example usage
```shell
...
    console.log(name + ": table's gone");
    return;
  }

  ball.hits += 1;
  console.log('${name} ${ball.hits}');

  yield csp.timeout(100);
  yield csp.put(table, ball);
}
}

csp.go(function* () {
const table = csp.chan();
...
```



# <a name="apidoc.module.js-csp.DEFAULT"></a>[module js-csp.DEFAULT](#apidoc.module.js-csp.DEFAULT)

#### <a name="apidoc.element.js-csp.DEFAULT.toString"></a>[function <span class="apidocSignatureSpan">js-csp.DEFAULT.</span>toString ()](#apidoc.element.js-csp.DEFAULT.toString)
- description and source-code
```javascript
function toString() {
  return '[object DEFAULT]';
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.js-csp.buffers"></a>[module js-csp.buffers](#apidoc.module.js-csp.buffers)

#### <a name="apidoc.element.js-csp.buffers.dropping"></a>[function <span class="apidocSignatureSpan">js-csp.buffers.</span>dropping (n)](#apidoc.element.js-csp.buffers.dropping)
- description and source-code
```javascript
function dropping(n) {
  return new DroppingBuffer(ring(n), n);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.buffers.fixed"></a>[function <span class="apidocSignatureSpan">js-csp.buffers.</span>fixed (n)](#apidoc.element.js-csp.buffers.fixed)
- description and source-code
```javascript
function fixed(n) {
  return new FixedBuffer(ring(n), n);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.buffers.promise"></a>[function <span class="apidocSignatureSpan">js-csp.buffers.</span>promise ()](#apidoc.element.js-csp.buffers.promise)
- description and source-code
```javascript
function promise() {
  return new PromiseBuffer(PromiseBuffer.NO_VALUE);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.buffers.sliding"></a>[function <span class="apidocSignatureSpan">js-csp.buffers.</span>sliding (n)](#apidoc.element.js-csp.buffers.sliding)
- description and source-code
```javascript
function sliding(n) {
  return new SlidingBuffer(ring(n), n);
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.js-csp.csp_core"></a>[module js-csp.csp_core](#apidoc.module.js-csp.csp_core)

#### <a name="apidoc.element.js-csp.csp_core.chan"></a>[function <span class="apidocSignatureSpan">js-csp.csp_core.</span>chan (bufferOrNumber, xform, exHandler)](#apidoc.element.js-csp.csp_core.chan)
- description and source-code
```javascript
function chan(bufferOrNumber, xform, exHandler) {
  if (typeof bufferOrNumber === 'number') {
    return (0, _channels.chan)(bufferOrNumber === 0 ? null : (0, _buffers.fixed)(bufferOrNumber), xform, exHandler);
  }

  return (0, _channels.chan)(bufferOrNumber, xform, exHandler);
}
```
- example usage
```shell
...

  yield csp.timeout(100);
  yield csp.put(table, ball);
}
}

csp.go(function* () {
const table = csp.chan();

csp.go(player, ["ping", table]);
csp.go(player, ["pong", table]);

yield csp.put(table, {hits: 0});
yield csp.timeout(1000);
...
```

#### <a name="apidoc.element.js-csp.csp_core.go"></a>[function <span class="apidocSignatureSpan">js-csp.csp_core.</span>go (f)](#apidoc.element.js-csp.csp_core.go)
- description and source-code
```javascript
function go(f) {
  var args = arguments.length > 1 && arguments[1] !== undefined ? arguments[1] : [];

  return spawn(f.apply(undefined, (0, _toConsumableArray3.default)(args)));
}
```
- example usage
```shell
...
  console.log('${name} ${ball.hits}');

  yield csp.timeout(100);
  yield csp.put(table, ball);
}
}

csp.go(function* () {
const table = csp.chan();

csp.go(player, ["ping", table]);
csp.go(player, ["pong", table]);

yield csp.put(table, {hits: 0});
yield csp.timeout(1000);
...
```

#### <a name="apidoc.element.js-csp.csp_core.promiseChan"></a>[function <span class="apidocSignatureSpan">js-csp.csp_core.</span>promiseChan (xform, exHandler)](#apidoc.element.js-csp.csp_core.promiseChan)
- description and source-code
```javascript
function promiseChan(xform, exHandler) {
  return (0, _channels.chan)((0, _buffers.promise)(), xform, exHandler);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_core.spawn"></a>[function <span class="apidocSignatureSpan">js-csp.csp_core.</span>spawn (gen)](#apidoc.element.js-csp.csp_core.spawn)
- description and source-code
```javascript
function spawn(gen) {
  var ch = (0, _channels.chan)((0, _buffers.fixed)(1));
  var process = new _process.Process(gen, function (value) {
    if (value === _channels.CLOSED) {
      ch.close();
    } else {
      (0, _process.putThenCallback)(ch, value, function () {
        return ch.close();
      });
    }
  });

  process.run();
  return ch;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.js-csp.csp_operations"></a>[module js-csp.csp_operations](#apidoc.module.js-csp.csp_operations)

#### <a name="apidoc.element.js-csp.csp_operations.filterFrom"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>filterFrom (p, ch, bufferOrN)](#apidoc.element.js-csp.csp_operations.filterFrom)
- description and source-code
```javascript
function filterFrom(p, ch, bufferOrN) {
  var out = (0, _csp.chan)(bufferOrN);

  (0, _csp.go)(_regenerator2.default.mark(function _callee() {
    var value;
    return _regenerator2.default.wrap(function _callee$(_context) {
      while (1) {
        switch (_context.prev = _context.next) {
          case 0:
            _context.next = 2;
            return (0, _process.take)(ch);

          case 2:
            value = _context.sent;

            if (!(value === _channels.CLOSED)) {
              _context.next = 6;
              break;
            }

            out.close();
            return _context.abrupt('break', 11);

          case 6:
            if (!p(value)) {
              _context.next = 9;
              break;
            }

            _context.next = 9;
            return (0, _process.put)(out, value);

          case 9:
            _context.next = 0;
            break;

          case 11:
          case 'end':
            return _context.stop();
        }
      }
    }, _callee, this);
  }));
  return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.filterInto"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>filterInto (p, ch)](#apidoc.element.js-csp.csp_operations.filterInto)
- description and source-code
```javascript
function filterInto(p, ch) {
  return {
    isClosed: function isClosed() {
      return ch.isClosed();
    },
    close: function close() {
      ch.close();
    },
    put: function put(value, handler) {
      if (p(value)) {
        return ch.put(value, handler);
      }

      return new _boxes.Box(!ch.isClosed());
    },
    take: function take(handler) {
      return ch.take(handler);
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.fromColl"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>fromColl (coll)](#apidoc.element.js-csp.csp_operations.fromColl)
- description and source-code
```javascript
function fromColl(coll) {
  var ch = (0, _csp.chan)(coll.length);
  onto(ch, coll);
  return ch;
}
```
- example usage
```shell
...
// thread(
//   [fromColl, [1, 2, 3, 4]],
//   [mapFrom, inc, _],
//   [into, [], _]
// )

// wrap()
//   .fromColl([1, 2, 3, 4])
//   .mapFrom(inc)
//   .into([])
//   .unwrap();
...
```

#### <a name="apidoc.element.js-csp.csp_operations.into"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>into (coll, ch)](#apidoc.element.js-csp.csp_operations.into)
- description and source-code
```javascript
function into(coll, ch) {
  var result = coll.slice(0);
  return reduce(function (_result, item) {
    _result.push(item);
    return _result;
  }, result, ch);
}
```
- example usage
```shell
...
//   [mapFrom, inc, _],
//   [into, [], _]
// )

// wrap()
//   .fromColl([1, 2, 3, 4])
//   .mapFrom(inc)
//   .into([])
//   .unwrap();
...
```

#### <a name="apidoc.element.js-csp.csp_operations.map"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>map (f, chs, bufferOrN)](#apidoc.element.js-csp.csp_operations.map)
- description and source-code
```javascript
function map(f, chs, bufferOrN) {
  var out = (0, _csp.chan)(bufferOrN);
  var length = chs.length;
  // Array holding 1 round of values
  var values = new Array(length);
  // TODO: Not sure why we need a size-1 buffer here
  var dchan = (0, _csp.chan)(1);
  // How many more items this round
  var dcount = void 0;
  // put callbacks for each channel
  var dcallbacks = new Array(length);
  var callback = function callback(i) {
    return function (value) {
      values[i] = value;
      dcount -= 1;
      if (dcount === 0) {
        (0, _process.putThenCallback)(dchan, values.slice(0));
      }
    };
  };

  for (var i = 0; i < length; i += 1) {
    dcallbacks[i] = callback(i);
  }

  (0, _csp.go)(_regenerator2.default.mark(function _callee6() {
    var _i, _values, _i2;

    return _regenerator2.default.wrap(function _callee6$(_context7) {
      while (1) {
        switch (_context7.prev = _context7.next) {
          case 0:
            dcount = length;
            // We could just launch n goroutines here, but for effciency we
            // don't
            for (_i = 0; _i < length; _i += 1) {
              try {
                (0, _process.takeThenCallback)(chs[_i], dcallbacks[_i]);
              } catch (e) {
                // FIX: Hmm why catching here?
                dcount -= 1;
              }
            }

            _context7.next = 4;
            return (0, _process.take)(dchan);

          case 4:
            _values = _context7.sent;
            _i2 = 0;

          case 6:
            if (!(_i2 < length)) {
              _context7.next = 13;
              break;
            }

            if (!(_values[_i2] === _channels.CLOSED)) {
              _context7.next = 10;
              break;
            }

            out.close();
            return _context7.abrupt('return');

          case 10:
            _i2 += 1;
            _context7.next = 6;
            break;

          case 13:
            _context7.next = 15;
            return (0, _process.put)(out, f.apply(undefined, (0, _toConsumableArray3.default)(_values)));

          case 15:
            _context7.next = 0;
            break;

          case 17:
          case 'end':
            return _context7.stop();
        }
      }
    }, _callee6, this);
  }));
  return out;
}
```
- example usage
```shell
...

var _process = require('./impl/process');

var _csp = require('./csp.core');

function _interopRequireDefault(obj) { return obj && obj.__esModule ? obj : { default: obj }; }

var _marked = [mapcat].map(_regenerator2.default.mark);

function mapFrom(f, ch) {
return {
  isClosed: function isClosed() {
    return ch.isClosed();
  },
  close: function close() {
...
```

#### <a name="apidoc.element.js-csp.csp_operations.mapFrom"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>mapFrom (f, ch)](#apidoc.element.js-csp.csp_operations.mapFrom)
- description and source-code
```javascript
function mapFrom(f, ch) {
  return {
    isClosed: function isClosed() {
      return ch.isClosed();
    },
    close: function close() {
      ch.close();
    },
    put: function put(value, handler) {
      return ch.put(value, handler);
    },
    take: function take(handler) {
      var result = ch.take({
        isActive: function isActive() {
          return handler.isActive();
        },
        commit: function commit() {
          var takeCallback = handler.commit();
          return function (value) {
            return takeCallback(value === _channels.CLOSED ? _channels.CLOSED : f(value));
          };
        }
      });

      if (result) {
        var value = result.value;
        return new _boxes.Box(value === _channels.CLOSED ? _channels.CLOSED : f(value));
      }

      return null;
    }
  };
}
```
- example usage
```shell
...
//   [fromColl, [1, 2, 3, 4]],
//   [mapFrom, inc, _],
//   [into, [], _]
// )

// wrap()
//   .fromColl([1, 2, 3, 4])
//   .mapFrom(inc)
//   .into([])
//   .unwrap();
...
```

#### <a name="apidoc.element.js-csp.csp_operations.mapInto"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>mapInto (f, ch)](#apidoc.element.js-csp.csp_operations.mapInto)
- description and source-code
```javascript
function mapInto(f, ch) {
  return {
    isClosed: function isClosed() {
      return ch.isClosed();
    },
    close: function close() {
      ch.close();
    },
    put: function put(value, handler) {
      return ch.put(f(value), handler);
    },
    take: function take(handler) {
      return ch.take(handler);
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.mapcatFrom"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>mapcatFrom (f, ch, bufferOrN)](#apidoc.element.js-csp.csp_operations.mapcatFrom)
- description and source-code
```javascript
function mapcatFrom(f, ch, bufferOrN) {
  var out = (0, _csp.chan)(bufferOrN);
  (0, _csp.go)(mapcat, [f, ch, out]);
  return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.mapcatInto"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>mapcatInto (f, ch, bufferOrN)](#apidoc.element.js-csp.csp_operations.mapcatInto)
- description and source-code
```javascript
function mapcatInto(f, ch, bufferOrN) {
  var src = (0, _csp.chan)(bufferOrN);
  (0, _csp.go)(mapcat, [f, src, ch]);
  return src;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.merge"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>merge (chs, bufferOrN)](#apidoc.element.js-csp.csp_operations.merge)
- description and source-code
```javascript
function merge(chs, bufferOrN) {
  var out = (0, _csp.chan)(bufferOrN);
  var actives = chs.slice(0);
  (0, _csp.go)(_regenerator2.default.mark(function _callee7() {
    var r, value, i;
    return _regenerator2.default.wrap(function _callee7$(_context8) {
      while (1) {
        switch (_context8.prev = _context8.next) {
          case 0:
            if (!(actives.length === 0)) {
              _context8.next = 2;
              break;
            }

            return _context8.abrupt('break', 15);

          case 2:
            _context8.next = 4;
            return (0, _process.alts)(actives);

          case 4:
            r = _context8.sent;
            value = r.value;

            if (!(value === _channels.CLOSED)) {
              _context8.next = 11;
              break;
            }

            // Remove closed channel
            i = actives.indexOf(r.channel);

            actives.splice(i, 1);
            _context8.next = 13;
            break;

          case 11:
            _context8.next = 13;
            return (0, _process.put)(out, value);

          case 13:
            _context8.next = 0;
            break;

          case 15:
            out.close();

          case 16:
          case 'end':
            return _context8.stop();
        }
      }
    }, _callee7, this);
  }));
  return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.mix"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>mix (out)](#apidoc.element.js-csp.csp_operations.mix)
- description and source-code
```javascript
function mix(out) {
  var m = new Mix(out);
  (0, _csp.go)(_regenerator2.default.mark(function _callee13() {
    var state, result, _value, channel, solos, stillOpen;

    return _regenerator2.default.wrap(function _callee13$(_context15) {
      while (1) {
        switch (_context15.prev = _context15.next) {
          case 0:
            state = m._getAllState();

          case 1:
            _context15.next = 3;
            return (0, _process.alts)(state.reads);

          case 3:
            result = _context15.sent;
            _value = result.value;
            channel = result.channel;

            if (!(_value === _channels.CLOSED)) {
              _context15.next = 11;
              break;
            }

            delete m.stateMap[chanId(channel)];
            state = m._getAllState();
            _context15.next = 22;
            break;

          case 11:
            if (!(channel === m.change)) {
              _context15.next = 15;
              break;
            }

            state = m._getAllState();
            _context15.next = 22;
            break;

          case 15:
            solos = state.solos;

            if (!(solos.indexOf(channel) > -1 || solos.length === 0 && !(state.mutes.indexOf(channel) > -1))) {
              _context15.next = 22;
              break;
            }

            _context15.next = 19;
            return (0, _process.put)(out, _value);

          case 19:
            stillOpen = _context15.sent;

            if (stillOpen) {
              _context15.next = 22;
              break;
            }

            return _context15.abrupt('break', 24);

          case 22:
            _context15.next = 1;
            break;

          case 24:
          case 'end':
            return _context15.stop();
        }
      }
    }, _callee13, this);
  }));
  return m;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.mult"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>mult (ch)](#apidoc.element.js-csp.csp_operations.mult)
- description and source-code
```javascript
function mult(ch) {
  var m = new Mult(ch);
  var dchan = (0, _csp.chan)(1);
  var dcount = void 0;

  function makeDoneCallback(tap) {
    return function (stillOpen) {
      dcount -= 1;
      if (dcount === 0) {
        (0, _process.putThenCallback)(dchan, true);
      }
      if (!stillOpen) {
        m.untap(tap.channel);
      }
    };
  }

  (0, _csp.go)(_regenerator2.default.mark(function _callee12() {
    var _this = this;

    var _loop, _ret;

    return _regenerator2.default.wrap(function _callee12$(_context14) {
      while (1) {
        switch (_context14.prev = _context14.next) {
          case 0:
            _loop = _regenerator2.default.mark(function _loop() {
              var value, taps, t, initDcount;
              return _regenerator2.default.wrap(function _loop$(_context13) {
                while (1) {
                  switch (_context13.prev = _context13.next) {
                    case 0:
                      _context13.next = 2;
                      return (0, _process.take)(ch);

                    case 2:
                      value = _context13.sent;
                      taps = m.taps;
                      t = void 0;

                      if (!(value === _channels.CLOSED)) {
                        _context13.next = 9;
                        break;
                      }

                      (0, _keys2.default)(taps).forEach(function (id) {
                        t = taps[id];
                        if (!t.keepOpen) {
                          t.channel.close();
                        }
                      });

                      // TODO: Is this necessary?
                      m.untapAll();
                      return _context13.abrupt('return', 'break');

                    case 9:
                      dcount = (0, _keys2.default)(taps).length;
                      // XXX: This is because putAsync can actually call back
                      // immediately. Fix that
                      initDcount = dcount;
                      // Put value on tapping channels...

                      (0, _keys2.default)(taps).forEach(function (id) {
                        t = taps[id];
                        (0, _process.putThenCallback)(t.channel, value, makeDoneCallback(t));
                      });
                      // ... waiting for all puts to complete

                      if (!(initDcount > 0)) {
                        _context13.next = 15;
                        break;
                      }

                      _context13.next = 15;
                      return (0, _process.take)(dchan);

                    case 15:
                    case 'end':
                      return _context13.stop();
                  }
                }
              }, _loop, _this);
            });

          case 1:
            return _context14.delegateYield(_loop(), 't0', 2);

          case 2:
            _ret = _context14.t0;

            if (!(_ret === 'break')) {
              _context14.next = 5;
              break;
            }

            return _context14.abrupt('break', 7);

          case 5:
            _context14.next = 1;
            break;

          case 7:
          case 'end':
            return _context14.stop();
        }
      }
    }, _callee12, this);
  }));
  return m;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.onto"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>onto (ch, coll, keepOpen)](#apidoc.element.js-csp.csp_operations.onto)
- description and source-code
```javascript
function onto(ch, coll, keepOpen) {
  return (0, _csp.go)(_regenerator2.default.mark(function _callee5() {
    var length, i;
    return _regenerator2.default.wrap(function _callee5$(_context6) {
      while (1) {
        switch (_context6.prev = _context6.next) {
          case 0:
            length = coll.length;
            // FIX: Should be a generic looping interface (for...in?)

            i = 0;

          case 2:
            if (!(i < length)) {
              _context6.next = 8;
              break;
            }

            _context6.next = 5;
            return (0, _process.put)(ch, coll[i]);

          case 5:
            i += 1;
            _context6.next = 2;
            break;

          case 8:
            if (!keepOpen) {
              ch.close();
            }

          case 9:
          case 'end':
            return _context6.stop();
        }
      }
    }, _callee5, this);
  }));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.partition"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>partition (n, ch, bufferOrN)](#apidoc.element.js-csp.csp_operations.partition)
- description and source-code
```javascript
function partition(n, ch, bufferOrN) {
  var out = (0, _csp.chan)(bufferOrN);
  (0, _csp.go)(_regenerator2.default.mark(function _callee11() {
    var part, i, value;
    return _regenerator2.default.wrap(function _callee11$(_context12) {
      while (1) {
        switch (_context12.prev = _context12.next) {
          case 0:
            part = new Array(n);
            i = 0;

          case 2:
            if (!(i < n)) {
              _context12.next = 16;
              break;
            }

            _context12.next = 5;
            return (0, _process.take)(ch);

          case 5:
            value = _context12.sent;

            if (!(value === _channels.CLOSED)) {
              _context12.next = 12;
              break;
            }

            if (!(i > 0)) {
              _context12.next = 10;
              break;
            }

            _context12.next = 10;
            return (0, _process.put)(out, part.slice(0, i));

          case 10:
            out.close();
            return _context12.abrupt('return');

          case 12:
            part[i] = value;

          case 13:
            i += 1;
            _context12.next = 2;
            break;

          case 16:
            _context12.next = 18;
            return (0, _process.put)(out, part);

          case 18:
            _context12.next = 0;
            break;

          case 20:
          case 'end':
            return _context12.stop();
        }
      }
    }, _callee11, this);
  }));
  return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.partitionBy"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>partitionBy (f, ch, bufferOrN)](#apidoc.element.js-csp.csp_operations.partitionBy)
- description and source-code
```javascript
function partitionBy(f, ch, bufferOrN) {
  var out = (0, _csp.chan)(bufferOrN);
  var part = [];
  var last = NOTHING;
  (0, _csp.go)(_regenerator2.default.mark(function _callee10() {
    var value, newItem;
    return _regenerator2.default.wrap(function _callee10$(_context11) {
      while (1) {
        switch (_context11.prev = _context11.next) {
          case 0:
            _context11.next = 2;
            return (0, _process.take)(ch);

          case 2:
            value = _context11.sent;

            if (!(value === _channels.CLOSED)) {
              _context11.next = 11;
              break;
            }

            if (!(part.length > 0)) {
              _context11.next = 7;
              break;
            }

            _context11.next = 7;
            return (0, _process.put)(out, part);

          case 7:
            out.close();
            return _context11.abrupt('break', 22);

          case 11:
            newItem = f(value);

            if (!(newItem === last || last === NOTHING)) {
              _context11.next = 16;
              break;
            }

            part.push(value);
            _context11.next = 19;
            break;

          case 16:
            _context11.next = 18;
            return (0, _process.put)(out, part);

          case 18:
            part = [value];

          case 19:
            last = newItem;

          case 20:
            _context11.next = 0;
            break;

          case 22:
          case 'end':
            return _context11.stop();
        }
      }
    }, _callee10, this);
  }));
  return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.pipe"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>pipe (src, dst, keepOpen)](#apidoc.element.js-csp.csp_operations.pipe)
- description and source-code
```javascript
function pipe(src, dst, keepOpen) {
  (0, _csp.go)(_regenerator2.default.mark(function _callee2() {
    var value;
    return _regenerator2.default.wrap(function _callee2$(_context3) {
      while (1) {
        switch (_context3.prev = _context3.next) {
          case 0:
            _context3.next = 2;
            return (0, _process.take)(src);

          case 2:
            value = _context3.sent;

            if (!(value === _channels.CLOSED)) {
              _context3.next = 6;
              break;
            }

            if (!keepOpen) {
              dst.close();
            }
            return _context3.abrupt('break', 12);

          case 6:
            _context3.next = 8;
            return (0, _process.put)(dst, value);

          case 8:
            if (_context3.sent) {
              _context3.next = 10;
              break;
            }

            return _context3.abrupt('break', 12);

          case 10:
            _context3.next = 0;
            break;

          case 12:
          case 'end':
            return _context3.stop();
        }
      }
    }, _callee2, this);
  }));
  return dst;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.pipeline"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>pipeline (to, xf, from, keepOpen, exHandler)](#apidoc.element.js-csp.csp_operations.pipeline)
- description and source-code
```javascript
function pipeline(to, xf, from, keepOpen, exHandler) {
  function taskFn(job) {
    if (job === _channels.CLOSED) {
      return null;
    }

    var _job = (0, _slicedToArray3.default)(job, 2),
        v = _job[0],
        p = _job[1];

    var res = (0, _csp.chan)(1, xf, exHandler);

    (0, _csp.go)(_regenerator2.default.mark(function _callee18(ch, value) {
      return _regenerator2.default.wrap(function _callee18$(_context21) {
        while (1) {
          switch (_context21.prev = _context21.next) {
            case 0:
              _context21.next = 2;
              return (0, _process.put)(ch, value);

            case 2:
              res.close();

            case 3:
            case 'end':
              return _context21.stop();
          }
        }
      }, _callee18, this);
    }), [res, v]);

    (0, _process.putThenCallback)(p, res);

    return true;
  }

  return pipelineInternal(1, to, from, !keepOpen, taskFn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.pipelineAsync"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>pipelineAsync (n, to, af, from, keepOpen)](#apidoc.element.js-csp.csp_operations.pipelineAsync)
- description and source-code
```javascript
function pipelineAsync(n, to, af, from, keepOpen) {
  function taskFn(job) {
    if (job === _channels.CLOSED) {
      return null;
    }

    var _job2 = (0, _slicedToArray3.default)(job, 2),
        v = _job2[0],
        p = _job2[1];

    var res = (0, _csp.chan)(1);
    af(v, res);
    (0, _process.putThenCallback)(p, res);

    return true;
  }

  return pipelineInternal(n, to, from, !keepOpen, taskFn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.pub"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>pub (ch, topicFn)](#apidoc.element.js-csp.csp_operations.pub)
- description and source-code
```javascript
function pub(ch, topicFn) {
  var bufferFn = arguments.length > 2 && arguments[2] !== undefined ? arguments[2] : constantlyNull;

  var p = new Pub(ch, topicFn, bufferFn);
  (0, _csp.go)(_regenerator2.default.mark(function _callee14() {
    var _this3 = this;

    var _loop3, _ret3;

    return _regenerator2.default.wrap(function _callee14$(_context17) {
      while (1) {
        switch (_context17.prev = _context17.next) {
          case 0:
            _loop3 = _regenerator2.default.mark(function _loop3() {
              var value, mults, topic, m, stillOpen;
              return _regenerator2.default.wrap(function _loop3$(_context16) {
                while (1) {
                  switch (_context16.prev = _context16.next) {
                    case 0:
                      _context16.next = 2;
                      return (0, _process.take)(ch);

                    case 2:
                      value = _context16.sent;
                      mults = p.mults;

                      if (!(value === _channels.CLOSED)) {
                        _context16.next = 7;
                        break;
                      }

                      (0, _keys2.default)(mults).forEach(function (topic) {
                        mults[topic].muxch().close();
                      });
                      return _context16.abrupt('return', 'break');

                    case 7:
                      // TODO: Somehow ensure/document that this must return a string
                      // (otherwise use proper (hash)maps)
                      topic = topicFn(value);
                      m = mults[topic];

                      if (!m) {
                        _context16.next = 14;
                        break;
                      }

                      _context16.next = 12;
                      return (0, _process.put)(m.muxch(), value);

                    case 12:
                      stillOpen = _context16.sent;

                      if (!stillOpen) {
                        delete mults[topic];
                      }

                    case 14:
                    case 'end':
                      return _context16.stop();
                  }
                }
              }, _loop3, _this3);
            });

          case 1:
            return _context17.delegateYield(_loop3(), 't0', 2);

          case 2:
            _ret3 = _context17.t0;

            if (!(_ret3 === 'break')) {
              _context17.next = 5;
              break;
            }

            return _context17.abrupt('break', 7);

          case 5:
            _context17.next = 1;
            break;

          case 7:
          case 'end':
            return _context17.stop();
        }
      }
    }, _callee14, this);
  }));
  return p;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.reduce"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>reduce (f, init, ch)](#apidoc.element.js-csp.csp_operations.reduce)
- description and source-code
```javascript
function reduce(f, init, ch) {
  return (0, _csp.go)(_regenerator2.default.mark(function _callee4() {
    var result, value;
    return _regenerator2.default.wrap(function _callee4$(_context5) {
      while (1) {
        switch (_context5.prev = _context5.next) {
          case 0:
            result = init;

          case 1:
            _context5.next = 3;
            return (0, _process.take)(ch);

          case 3:
            value = _context5.sent;

            if (!(value === _channels.CLOSED)) {
              _context5.next = 6;
              break;
            }

            return _context5.abrupt('return', result);

          case 6:

            result = f(result, value);

          case 7:
            _context5.next = 1;
            break;

          case 9:
          case 'end':
            return _context5.stop();
        }
      }
    }, _callee4, this);
  }), [], true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.removeFrom"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>removeFrom (p, ch)](#apidoc.element.js-csp.csp_operations.removeFrom)
- description and source-code
```javascript
function removeFrom(p, ch) {
  return filterFrom(function (value) {
    return !p(value);
  }, ch);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.removeInto"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>removeInto (p, ch)](#apidoc.element.js-csp.csp_operations.removeInto)
- description and source-code
```javascript
function removeInto(p, ch) {
  return filterInto(function (value) {
    return !p(value);
  }, ch);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.split"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>split (p, ch, trueBufferOrN, falseBufferOrN)](#apidoc.element.js-csp.csp_operations.split)
- description and source-code
```javascript
function split(p, ch, trueBufferOrN, falseBufferOrN) {
  var tch = (0, _csp.chan)(trueBufferOrN);
  var fch = (0, _csp.chan)(falseBufferOrN);
  (0, _csp.go)(_regenerator2.default.mark(function _callee3() {
    var value;
    return _regenerator2.default.wrap(function _callee3$(_context4) {
      while (1) {
        switch (_context4.prev = _context4.next) {
          case 0:
            _context4.next = 2;
            return (0, _process.take)(ch);

          case 2:
            value = _context4.sent;

            if (!(value === _channels.CLOSED)) {
              _context4.next = 7;
              break;
            }

            tch.close();
            fch.close();
            return _context4.abrupt('break', 11);

          case 7:
            _context4.next = 9;
            return (0, _process.put)(p(value) ? tch : fch, value);

          case 9:
            _context4.next = 0;
            break;

          case 11:
          case 'end':
            return _context4.stop();
        }
      }
    }, _callee3, this);
  }));
  return [tch, fch];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.csp_operations.take"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>take (n, ch, bufferOrN)](#apidoc.element.js-csp.csp_operations.take)
- description and source-code
```javascript
function take(n, ch, bufferOrN) {
  var out = (0, _csp.chan)(bufferOrN);
  (0, _csp.go)(_regenerator2.default.mark(function _callee8() {
    var i, value;
    return _regenerator2.default.wrap(function _callee8$(_context9) {
      while (1) {
        switch (_context9.prev = _context9.next) {
          case 0:
            i = 0;

          case 1:
            if (!(i < n)) {
              _context9.next = 12;
              break;
            }

            _context9.next = 4;
            return (0, _process.take)(ch);

          case 4:
            value = _context9.sent;

            if (!(value === _channels.CLOSED)) {
              _context9.next = 7;
              break;
            }

            return _context9.abrupt('break', 12);

          case 7:
            _context9.next = 9;
            return (0, _process.put)(out, value);

          case 9:
            i += 1;
            _context9.next = 1;
            break;

          case 12:
            out.close();

          case 13:
          case 'end':
            return _context9.stop();
        }
      }
    }, _callee8, this);
  }));
  return out;
}
```
- example usage
```shell
...
'''

Pingpong (ported from [Go](http://talks.golang.org/2013/advconc.slide#6)).

'''javascript
function* player(name, table) {
  while (true) {
let ball = yield csp.take(table);

if (ball === csp.CLOSED) {
  console.log(name + ": table's gone");
  return;
}

ball.hits += 1;
...
```

#### <a name="apidoc.element.js-csp.csp_operations.unique"></a>[function <span class="apidocSignatureSpan">js-csp.csp_operations.</span>unique (ch, bufferOrN)](#apidoc.element.js-csp.csp_operations.unique)
- description and source-code
```javascript
function unique(ch, bufferOrN) {
  var out = (0, _csp.chan)(bufferOrN);
  var last = NOTHING;
  (0, _csp.go)(_regenerator2.default.mark(function _callee9() {
    var value;
    return _regenerator2.default.wrap(function _callee9$(_context10) {
      while (1) {
        switch (_context10.prev = _context10.next) {
          case 0:
            _context10.next = 2;
            return (0, _process.take)(ch);

          case 2:
            value = _context10.sent;

            if (!(value === _channels.CLOSED)) {
              _context10.next = 5;
              break;
            }

            return _context10.abrupt('break', 11);

          case 5:
            if (!(value !== last)) {
              _context10.next = 9;
              break;
            }

            last = value;
            _context10.next = 9;
            return (0, _process.put)(out, value);

          case 9:
            _context10.next = 0;
            break;

          case 11:
            out.close();

          case 12:
          case 'end':
            return _context10.stop();
        }
      }
    }, _callee9, this);
  }));
  return out;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.js-csp.operations"></a>[module js-csp.operations](#apidoc.module.js-csp.operations)

#### <a name="apidoc.element.js-csp.operations.filterFrom"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>filterFrom (p, ch, bufferOrN)](#apidoc.element.js-csp.operations.filterFrom)
- description and source-code
```javascript
function filterFrom(p, ch, bufferOrN) {
  var out = (0, _csp.chan)(bufferOrN);

  (0, _csp.go)(_regenerator2.default.mark(function _callee() {
    var value;
    return _regenerator2.default.wrap(function _callee$(_context) {
      while (1) {
        switch (_context.prev = _context.next) {
          case 0:
            _context.next = 2;
            return (0, _process.take)(ch);

          case 2:
            value = _context.sent;

            if (!(value === _channels.CLOSED)) {
              _context.next = 6;
              break;
            }

            out.close();
            return _context.abrupt('break', 11);

          case 6:
            if (!p(value)) {
              _context.next = 9;
              break;
            }

            _context.next = 9;
            return (0, _process.put)(out, value);

          case 9:
            _context.next = 0;
            break;

          case 11:
          case 'end':
            return _context.stop();
        }
      }
    }, _callee, this);
  }));
  return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.filterInto"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>filterInto (p, ch)](#apidoc.element.js-csp.operations.filterInto)
- description and source-code
```javascript
function filterInto(p, ch) {
  return {
    isClosed: function isClosed() {
      return ch.isClosed();
    },
    close: function close() {
      ch.close();
    },
    put: function put(value, handler) {
      if (p(value)) {
        return ch.put(value, handler);
      }

      return new _boxes.Box(!ch.isClosed());
    },
    take: function take(handler) {
      return ch.take(handler);
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.fromColl"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>fromColl (coll)](#apidoc.element.js-csp.operations.fromColl)
- description and source-code
```javascript
function fromColl(coll) {
  var ch = (0, _csp.chan)(coll.length);
  onto(ch, coll);
  return ch;
}
```
- example usage
```shell
...
// thread(
//   [fromColl, [1, 2, 3, 4]],
//   [mapFrom, inc, _],
//   [into, [], _]
// )

// wrap()
//   .fromColl([1, 2, 3, 4])
//   .mapFrom(inc)
//   .into([])
//   .unwrap();
...
```

#### <a name="apidoc.element.js-csp.operations.into"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>into (coll, ch)](#apidoc.element.js-csp.operations.into)
- description and source-code
```javascript
function into(coll, ch) {
  var result = coll.slice(0);
  return reduce(function (_result, item) {
    _result.push(item);
    return _result;
  }, result, ch);
}
```
- example usage
```shell
...
//   [mapFrom, inc, _],
//   [into, [], _]
// )

// wrap()
//   .fromColl([1, 2, 3, 4])
//   .mapFrom(inc)
//   .into([])
//   .unwrap();
...
```

#### <a name="apidoc.element.js-csp.operations.map"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>map (f, chs, bufferOrN)](#apidoc.element.js-csp.operations.map)
- description and source-code
```javascript
function map(f, chs, bufferOrN) {
  var out = (0, _csp.chan)(bufferOrN);
  var length = chs.length;
  // Array holding 1 round of values
  var values = new Array(length);
  // TODO: Not sure why we need a size-1 buffer here
  var dchan = (0, _csp.chan)(1);
  // How many more items this round
  var dcount = void 0;
  // put callbacks for each channel
  var dcallbacks = new Array(length);
  var callback = function callback(i) {
    return function (value) {
      values[i] = value;
      dcount -= 1;
      if (dcount === 0) {
        (0, _process.putThenCallback)(dchan, values.slice(0));
      }
    };
  };

  for (var i = 0; i < length; i += 1) {
    dcallbacks[i] = callback(i);
  }

  (0, _csp.go)(_regenerator2.default.mark(function _callee6() {
    var _i, _values, _i2;

    return _regenerator2.default.wrap(function _callee6$(_context7) {
      while (1) {
        switch (_context7.prev = _context7.next) {
          case 0:
            dcount = length;
            // We could just launch n goroutines here, but for effciency we
            // don't
            for (_i = 0; _i < length; _i += 1) {
              try {
                (0, _process.takeThenCallback)(chs[_i], dcallbacks[_i]);
              } catch (e) {
                // FIX: Hmm why catching here?
                dcount -= 1;
              }
            }

            _context7.next = 4;
            return (0, _process.take)(dchan);

          case 4:
            _values = _context7.sent;
            _i2 = 0;

          case 6:
            if (!(_i2 < length)) {
              _context7.next = 13;
              break;
            }

            if (!(_values[_i2] === _channels.CLOSED)) {
              _context7.next = 10;
              break;
            }

            out.close();
            return _context7.abrupt('return');

          case 10:
            _i2 += 1;
            _context7.next = 6;
            break;

          case 13:
            _context7.next = 15;
            return (0, _process.put)(out, f.apply(undefined, (0, _toConsumableArray3.default)(_values)));

          case 15:
            _context7.next = 0;
            break;

          case 17:
          case 'end':
            return _context7.stop();
        }
      }
    }, _callee6, this);
  }));
  return out;
}
```
- example usage
```shell
...

var _process = require('./impl/process');

var _csp = require('./csp.core');

function _interopRequireDefault(obj) { return obj && obj.__esModule ? obj : { default: obj }; }

var _marked = [mapcat].map(_regenerator2.default.mark);

function mapFrom(f, ch) {
return {
  isClosed: function isClosed() {
    return ch.isClosed();
  },
  close: function close() {
...
```

#### <a name="apidoc.element.js-csp.operations.mapFrom"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>mapFrom (f, ch)](#apidoc.element.js-csp.operations.mapFrom)
- description and source-code
```javascript
function mapFrom(f, ch) {
  return {
    isClosed: function isClosed() {
      return ch.isClosed();
    },
    close: function close() {
      ch.close();
    },
    put: function put(value, handler) {
      return ch.put(value, handler);
    },
    take: function take(handler) {
      var result = ch.take({
        isActive: function isActive() {
          return handler.isActive();
        },
        commit: function commit() {
          var takeCallback = handler.commit();
          return function (value) {
            return takeCallback(value === _channels.CLOSED ? _channels.CLOSED : f(value));
          };
        }
      });

      if (result) {
        var value = result.value;
        return new _boxes.Box(value === _channels.CLOSED ? _channels.CLOSED : f(value));
      }

      return null;
    }
  };
}
```
- example usage
```shell
...
//   [fromColl, [1, 2, 3, 4]],
//   [mapFrom, inc, _],
//   [into, [], _]
// )

// wrap()
//   .fromColl([1, 2, 3, 4])
//   .mapFrom(inc)
//   .into([])
//   .unwrap();
...
```

#### <a name="apidoc.element.js-csp.operations.mapInto"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>mapInto (f, ch)](#apidoc.element.js-csp.operations.mapInto)
- description and source-code
```javascript
function mapInto(f, ch) {
  return {
    isClosed: function isClosed() {
      return ch.isClosed();
    },
    close: function close() {
      ch.close();
    },
    put: function put(value, handler) {
      return ch.put(f(value), handler);
    },
    take: function take(handler) {
      return ch.take(handler);
    }
  };
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.mapcatFrom"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>mapcatFrom (f, ch, bufferOrN)](#apidoc.element.js-csp.operations.mapcatFrom)
- description and source-code
```javascript
function mapcatFrom(f, ch, bufferOrN) {
  var out = (0, _csp.chan)(bufferOrN);
  (0, _csp.go)(mapcat, [f, ch, out]);
  return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.mapcatInto"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>mapcatInto (f, ch, bufferOrN)](#apidoc.element.js-csp.operations.mapcatInto)
- description and source-code
```javascript
function mapcatInto(f, ch, bufferOrN) {
  var src = (0, _csp.chan)(bufferOrN);
  (0, _csp.go)(mapcat, [f, src, ch]);
  return src;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.merge"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>merge (chs, bufferOrN)](#apidoc.element.js-csp.operations.merge)
- description and source-code
```javascript
function merge(chs, bufferOrN) {
  var out = (0, _csp.chan)(bufferOrN);
  var actives = chs.slice(0);
  (0, _csp.go)(_regenerator2.default.mark(function _callee7() {
    var r, value, i;
    return _regenerator2.default.wrap(function _callee7$(_context8) {
      while (1) {
        switch (_context8.prev = _context8.next) {
          case 0:
            if (!(actives.length === 0)) {
              _context8.next = 2;
              break;
            }

            return _context8.abrupt('break', 15);

          case 2:
            _context8.next = 4;
            return (0, _process.alts)(actives);

          case 4:
            r = _context8.sent;
            value = r.value;

            if (!(value === _channels.CLOSED)) {
              _context8.next = 11;
              break;
            }

            // Remove closed channel
            i = actives.indexOf(r.channel);

            actives.splice(i, 1);
            _context8.next = 13;
            break;

          case 11:
            _context8.next = 13;
            return (0, _process.put)(out, value);

          case 13:
            _context8.next = 0;
            break;

          case 15:
            out.close();

          case 16:
          case 'end':
            return _context8.stop();
        }
      }
    }, _callee7, this);
  }));
  return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.mix"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>mix (out)](#apidoc.element.js-csp.operations.mix)
- description and source-code
```javascript
function mix(out) {
  var m = new Mix(out);
  (0, _csp.go)(_regenerator2.default.mark(function _callee13() {
    var state, result, _value, channel, solos, stillOpen;

    return _regenerator2.default.wrap(function _callee13$(_context15) {
      while (1) {
        switch (_context15.prev = _context15.next) {
          case 0:
            state = m._getAllState();

          case 1:
            _context15.next = 3;
            return (0, _process.alts)(state.reads);

          case 3:
            result = _context15.sent;
            _value = result.value;
            channel = result.channel;

            if (!(_value === _channels.CLOSED)) {
              _context15.next = 11;
              break;
            }

            delete m.stateMap[chanId(channel)];
            state = m._getAllState();
            _context15.next = 22;
            break;

          case 11:
            if (!(channel === m.change)) {
              _context15.next = 15;
              break;
            }

            state = m._getAllState();
            _context15.next = 22;
            break;

          case 15:
            solos = state.solos;

            if (!(solos.indexOf(channel) > -1 || solos.length === 0 && !(state.mutes.indexOf(channel) > -1))) {
              _context15.next = 22;
              break;
            }

            _context15.next = 19;
            return (0, _process.put)(out, _value);

          case 19:
            stillOpen = _context15.sent;

            if (stillOpen) {
              _context15.next = 22;
              break;
            }

            return _context15.abrupt('break', 24);

          case 22:
            _context15.next = 1;
            break;

          case 24:
          case 'end':
            return _context15.stop();
        }
      }
    }, _callee13, this);
  }));
  return m;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.mult"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>mult (ch)](#apidoc.element.js-csp.operations.mult)
- description and source-code
```javascript
function mult(ch) {
  var m = new Mult(ch);
  var dchan = (0, _csp.chan)(1);
  var dcount = void 0;

  function makeDoneCallback(tap) {
    return function (stillOpen) {
      dcount -= 1;
      if (dcount === 0) {
        (0, _process.putThenCallback)(dchan, true);
      }
      if (!stillOpen) {
        m.untap(tap.channel);
      }
    };
  }

  (0, _csp.go)(_regenerator2.default.mark(function _callee12() {
    var _this = this;

    var _loop, _ret;

    return _regenerator2.default.wrap(function _callee12$(_context14) {
      while (1) {
        switch (_context14.prev = _context14.next) {
          case 0:
            _loop = _regenerator2.default.mark(function _loop() {
              var value, taps, t, initDcount;
              return _regenerator2.default.wrap(function _loop$(_context13) {
                while (1) {
                  switch (_context13.prev = _context13.next) {
                    case 0:
                      _context13.next = 2;
                      return (0, _process.take)(ch);

                    case 2:
                      value = _context13.sent;
                      taps = m.taps;
                      t = void 0;

                      if (!(value === _channels.CLOSED)) {
                        _context13.next = 9;
                        break;
                      }

                      (0, _keys2.default)(taps).forEach(function (id) {
                        t = taps[id];
                        if (!t.keepOpen) {
                          t.channel.close();
                        }
                      });

                      // TODO: Is this necessary?
                      m.untapAll();
                      return _context13.abrupt('return', 'break');

                    case 9:
                      dcount = (0, _keys2.default)(taps).length;
                      // XXX: This is because putAsync can actually call back
                      // immediately. Fix that
                      initDcount = dcount;
                      // Put value on tapping channels...

                      (0, _keys2.default)(taps).forEach(function (id) {
                        t = taps[id];
                        (0, _process.putThenCallback)(t.channel, value, makeDoneCallback(t));
                      });
                      // ... waiting for all puts to complete

                      if (!(initDcount > 0)) {
                        _context13.next = 15;
                        break;
                      }

                      _context13.next = 15;
                      return (0, _process.take)(dchan);

                    case 15:
                    case 'end':
                      return _context13.stop();
                  }
                }
              }, _loop, _this);
            });

          case 1:
            return _context14.delegateYield(_loop(), 't0', 2);

          case 2:
            _ret = _context14.t0;

            if (!(_ret === 'break')) {
              _context14.next = 5;
              break;
            }

            return _context14.abrupt('break', 7);

          case 5:
            _context14.next = 1;
            break;

          case 7:
          case 'end':
            return _context14.stop();
        }
      }
    }, _callee12, this);
  }));
  return m;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.onto"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>onto (ch, coll, keepOpen)](#apidoc.element.js-csp.operations.onto)
- description and source-code
```javascript
function onto(ch, coll, keepOpen) {
  return (0, _csp.go)(_regenerator2.default.mark(function _callee5() {
    var length, i;
    return _regenerator2.default.wrap(function _callee5$(_context6) {
      while (1) {
        switch (_context6.prev = _context6.next) {
          case 0:
            length = coll.length;
            // FIX: Should be a generic looping interface (for...in?)

            i = 0;

          case 2:
            if (!(i < length)) {
              _context6.next = 8;
              break;
            }

            _context6.next = 5;
            return (0, _process.put)(ch, coll[i]);

          case 5:
            i += 1;
            _context6.next = 2;
            break;

          case 8:
            if (!keepOpen) {
              ch.close();
            }

          case 9:
          case 'end':
            return _context6.stop();
        }
      }
    }, _callee5, this);
  }));
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.partition"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>partition (n, ch, bufferOrN)](#apidoc.element.js-csp.operations.partition)
- description and source-code
```javascript
function partition(n, ch, bufferOrN) {
  var out = (0, _csp.chan)(bufferOrN);
  (0, _csp.go)(_regenerator2.default.mark(function _callee11() {
    var part, i, value;
    return _regenerator2.default.wrap(function _callee11$(_context12) {
      while (1) {
        switch (_context12.prev = _context12.next) {
          case 0:
            part = new Array(n);
            i = 0;

          case 2:
            if (!(i < n)) {
              _context12.next = 16;
              break;
            }

            _context12.next = 5;
            return (0, _process.take)(ch);

          case 5:
            value = _context12.sent;

            if (!(value === _channels.CLOSED)) {
              _context12.next = 12;
              break;
            }

            if (!(i > 0)) {
              _context12.next = 10;
              break;
            }

            _context12.next = 10;
            return (0, _process.put)(out, part.slice(0, i));

          case 10:
            out.close();
            return _context12.abrupt('return');

          case 12:
            part[i] = value;

          case 13:
            i += 1;
            _context12.next = 2;
            break;

          case 16:
            _context12.next = 18;
            return (0, _process.put)(out, part);

          case 18:
            _context12.next = 0;
            break;

          case 20:
          case 'end':
            return _context12.stop();
        }
      }
    }, _callee11, this);
  }));
  return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.partitionBy"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>partitionBy (f, ch, bufferOrN)](#apidoc.element.js-csp.operations.partitionBy)
- description and source-code
```javascript
function partitionBy(f, ch, bufferOrN) {
  var out = (0, _csp.chan)(bufferOrN);
  var part = [];
  var last = NOTHING;
  (0, _csp.go)(_regenerator2.default.mark(function _callee10() {
    var value, newItem;
    return _regenerator2.default.wrap(function _callee10$(_context11) {
      while (1) {
        switch (_context11.prev = _context11.next) {
          case 0:
            _context11.next = 2;
            return (0, _process.take)(ch);

          case 2:
            value = _context11.sent;

            if (!(value === _channels.CLOSED)) {
              _context11.next = 11;
              break;
            }

            if (!(part.length > 0)) {
              _context11.next = 7;
              break;
            }

            _context11.next = 7;
            return (0, _process.put)(out, part);

          case 7:
            out.close();
            return _context11.abrupt('break', 22);

          case 11:
            newItem = f(value);

            if (!(newItem === last || last === NOTHING)) {
              _context11.next = 16;
              break;
            }

            part.push(value);
            _context11.next = 19;
            break;

          case 16:
            _context11.next = 18;
            return (0, _process.put)(out, part);

          case 18:
            part = [value];

          case 19:
            last = newItem;

          case 20:
            _context11.next = 0;
            break;

          case 22:
          case 'end':
            return _context11.stop();
        }
      }
    }, _callee10, this);
  }));
  return out;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.pipe"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>pipe (src, dst, keepOpen)](#apidoc.element.js-csp.operations.pipe)
- description and source-code
```javascript
function pipe(src, dst, keepOpen) {
  (0, _csp.go)(_regenerator2.default.mark(function _callee2() {
    var value;
    return _regenerator2.default.wrap(function _callee2$(_context3) {
      while (1) {
        switch (_context3.prev = _context3.next) {
          case 0:
            _context3.next = 2;
            return (0, _process.take)(src);

          case 2:
            value = _context3.sent;

            if (!(value === _channels.CLOSED)) {
              _context3.next = 6;
              break;
            }

            if (!keepOpen) {
              dst.close();
            }
            return _context3.abrupt('break', 12);

          case 6:
            _context3.next = 8;
            return (0, _process.put)(dst, value);

          case 8:
            if (_context3.sent) {
              _context3.next = 10;
              break;
            }

            return _context3.abrupt('break', 12);

          case 10:
            _context3.next = 0;
            break;

          case 12:
          case 'end':
            return _context3.stop();
        }
      }
    }, _callee2, this);
  }));
  return dst;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.pipeline"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>pipeline (to, xf, from, keepOpen, exHandler)](#apidoc.element.js-csp.operations.pipeline)
- description and source-code
```javascript
function pipeline(to, xf, from, keepOpen, exHandler) {
  function taskFn(job) {
    if (job === _channels.CLOSED) {
      return null;
    }

    var _job = (0, _slicedToArray3.default)(job, 2),
        v = _job[0],
        p = _job[1];

    var res = (0, _csp.chan)(1, xf, exHandler);

    (0, _csp.go)(_regenerator2.default.mark(function _callee18(ch, value) {
      return _regenerator2.default.wrap(function _callee18$(_context21) {
        while (1) {
          switch (_context21.prev = _context21.next) {
            case 0:
              _context21.next = 2;
              return (0, _process.put)(ch, value);

            case 2:
              res.close();

            case 3:
            case 'end':
              return _context21.stop();
          }
        }
      }, _callee18, this);
    }), [res, v]);

    (0, _process.putThenCallback)(p, res);

    return true;
  }

  return pipelineInternal(1, to, from, !keepOpen, taskFn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.pipelineAsync"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>pipelineAsync (n, to, af, from, keepOpen)](#apidoc.element.js-csp.operations.pipelineAsync)
- description and source-code
```javascript
function pipelineAsync(n, to, af, from, keepOpen) {
  function taskFn(job) {
    if (job === _channels.CLOSED) {
      return null;
    }

    var _job2 = (0, _slicedToArray3.default)(job, 2),
        v = _job2[0],
        p = _job2[1];

    var res = (0, _csp.chan)(1);
    af(v, res);
    (0, _process.putThenCallback)(p, res);

    return true;
  }

  return pipelineInternal(n, to, from, !keepOpen, taskFn);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.pub"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>pub (ch, topicFn)](#apidoc.element.js-csp.operations.pub)
- description and source-code
```javascript
function pub(ch, topicFn) {
  var bufferFn = arguments.length > 2 && arguments[2] !== undefined ? arguments[2] : constantlyNull;

  var p = new Pub(ch, topicFn, bufferFn);
  (0, _csp.go)(_regenerator2.default.mark(function _callee14() {
    var _this3 = this;

    var _loop3, _ret3;

    return _regenerator2.default.wrap(function _callee14$(_context17) {
      while (1) {
        switch (_context17.prev = _context17.next) {
          case 0:
            _loop3 = _regenerator2.default.mark(function _loop3() {
              var value, mults, topic, m, stillOpen;
              return _regenerator2.default.wrap(function _loop3$(_context16) {
                while (1) {
                  switch (_context16.prev = _context16.next) {
                    case 0:
                      _context16.next = 2;
                      return (0, _process.take)(ch);

                    case 2:
                      value = _context16.sent;
                      mults = p.mults;

                      if (!(value === _channels.CLOSED)) {
                        _context16.next = 7;
                        break;
                      }

                      (0, _keys2.default)(mults).forEach(function (topic) {
                        mults[topic].muxch().close();
                      });
                      return _context16.abrupt('return', 'break');

                    case 7:
                      // TODO: Somehow ensure/document that this must return a string
                      // (otherwise use proper (hash)maps)
                      topic = topicFn(value);
                      m = mults[topic];

                      if (!m) {
                        _context16.next = 14;
                        break;
                      }

                      _context16.next = 12;
                      return (0, _process.put)(m.muxch(), value);

                    case 12:
                      stillOpen = _context16.sent;

                      if (!stillOpen) {
                        delete mults[topic];
                      }

                    case 14:
                    case 'end':
                      return _context16.stop();
                  }
                }
              }, _loop3, _this3);
            });

          case 1:
            return _context17.delegateYield(_loop3(), 't0', 2);

          case 2:
            _ret3 = _context17.t0;

            if (!(_ret3 === 'break')) {
              _context17.next = 5;
              break;
            }

            return _context17.abrupt('break', 7);

          case 5:
            _context17.next = 1;
            break;

          case 7:
          case 'end':
            return _context17.stop();
        }
      }
    }, _callee14, this);
  }));
  return p;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.reduce"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>reduce (f, init, ch)](#apidoc.element.js-csp.operations.reduce)
- description and source-code
```javascript
function reduce(f, init, ch) {
  return (0, _csp.go)(_regenerator2.default.mark(function _callee4() {
    var result, value;
    return _regenerator2.default.wrap(function _callee4$(_context5) {
      while (1) {
        switch (_context5.prev = _context5.next) {
          case 0:
            result = init;

          case 1:
            _context5.next = 3;
            return (0, _process.take)(ch);

          case 3:
            value = _context5.sent;

            if (!(value === _channels.CLOSED)) {
              _context5.next = 6;
              break;
            }

            return _context5.abrupt('return', result);

          case 6:

            result = f(result, value);

          case 7:
            _context5.next = 1;
            break;

          case 9:
          case 'end':
            return _context5.stop();
        }
      }
    }, _callee4, this);
  }), [], true);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.removeFrom"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>removeFrom (p, ch)](#apidoc.element.js-csp.operations.removeFrom)
- description and source-code
```javascript
function removeFrom(p, ch) {
  return filterFrom(function (value) {
    return !p(value);
  }, ch);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.removeInto"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>removeInto (p, ch)](#apidoc.element.js-csp.operations.removeInto)
- description and source-code
```javascript
function removeInto(p, ch) {
  return filterInto(function (value) {
    return !p(value);
  }, ch);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.split"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>split (p, ch, trueBufferOrN, falseBufferOrN)](#apidoc.element.js-csp.operations.split)
- description and source-code
```javascript
function split(p, ch, trueBufferOrN, falseBufferOrN) {
  var tch = (0, _csp.chan)(trueBufferOrN);
  var fch = (0, _csp.chan)(falseBufferOrN);
  (0, _csp.go)(_regenerator2.default.mark(function _callee3() {
    var value;
    return _regenerator2.default.wrap(function _callee3$(_context4) {
      while (1) {
        switch (_context4.prev = _context4.next) {
          case 0:
            _context4.next = 2;
            return (0, _process.take)(ch);

          case 2:
            value = _context4.sent;

            if (!(value === _channels.CLOSED)) {
              _context4.next = 7;
              break;
            }

            tch.close();
            fch.close();
            return _context4.abrupt('break', 11);

          case 7:
            _context4.next = 9;
            return (0, _process.put)(p(value) ? tch : fch, value);

          case 9:
            _context4.next = 0;
            break;

          case 11:
          case 'end':
            return _context4.stop();
        }
      }
    }, _callee3, this);
  }));
  return [tch, fch];
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.take"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>take (n, ch, bufferOrN)](#apidoc.element.js-csp.operations.take)
- description and source-code
```javascript
function take(n, ch, bufferOrN) {
  var out = (0, _csp.chan)(bufferOrN);
  (0, _csp.go)(_regenerator2.default.mark(function _callee8() {
    var i, value;
    return _regenerator2.default.wrap(function _callee8$(_context9) {
      while (1) {
        switch (_context9.prev = _context9.next) {
          case 0:
            i = 0;

          case 1:
            if (!(i < n)) {
              _context9.next = 12;
              break;
            }

            _context9.next = 4;
            return (0, _process.take)(ch);

          case 4:
            value = _context9.sent;

            if (!(value === _channels.CLOSED)) {
              _context9.next = 7;
              break;
            }

            return _context9.abrupt('break', 12);

          case 7:
            _context9.next = 9;
            return (0, _process.put)(out, value);

          case 9:
            i += 1;
            _context9.next = 1;
            break;

          case 12:
            out.close();

          case 13:
          case 'end':
            return _context9.stop();
        }
      }
    }, _callee8, this);
  }));
  return out;
}
```
- example usage
```shell
...
'''

Pingpong (ported from [Go](http://talks.golang.org/2013/advconc.slide#6)).

'''javascript
function* player(name, table) {
  while (true) {
let ball = yield csp.take(table);

if (ball === csp.CLOSED) {
  console.log(name + ": table's gone");
  return;
}

ball.hits += 1;
...
```

#### <a name="apidoc.element.js-csp.operations.unique"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>unique (ch, bufferOrN)](#apidoc.element.js-csp.operations.unique)
- description and source-code
```javascript
function unique(ch, bufferOrN) {
  var out = (0, _csp.chan)(bufferOrN);
  var last = NOTHING;
  (0, _csp.go)(_regenerator2.default.mark(function _callee9() {
    var value;
    return _regenerator2.default.wrap(function _callee9$(_context10) {
      while (1) {
        switch (_context10.prev = _context10.next) {
          case 0:
            _context10.next = 2;
            return (0, _process.take)(ch);

          case 2:
            value = _context10.sent;

            if (!(value === _channels.CLOSED)) {
              _context10.next = 5;
              break;
            }

            return _context10.abrupt('break', 11);

          case 5:
            if (!(value !== last)) {
              _context10.next = 9;
              break;
            }

            last = value;
            _context10.next = 9;
            return (0, _process.put)(out, value);

          case 9:
            _context10.next = 0;
            break;

          case 11:
            out.close();

          case 12:
          case 'end':
            return _context10.stop();
        }
      }
    }, _callee9, this);
  }));
  return out;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.js-csp.operations.mix"></a>[module js-csp.operations.mix](#apidoc.module.js-csp.operations.mix)

#### <a name="apidoc.element.js-csp.operations.mix.mix"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>mix (out)](#apidoc.element.js-csp.operations.mix.mix)
- description and source-code
```javascript
function mix(out) {
  var m = new Mix(out);
  (0, _csp.go)(_regenerator2.default.mark(function _callee13() {
    var state, result, _value, channel, solos, stillOpen;

    return _regenerator2.default.wrap(function _callee13$(_context15) {
      while (1) {
        switch (_context15.prev = _context15.next) {
          case 0:
            state = m._getAllState();

          case 1:
            _context15.next = 3;
            return (0, _process.alts)(state.reads);

          case 3:
            result = _context15.sent;
            _value = result.value;
            channel = result.channel;

            if (!(_value === _channels.CLOSED)) {
              _context15.next = 11;
              break;
            }

            delete m.stateMap[chanId(channel)];
            state = m._getAllState();
            _context15.next = 22;
            break;

          case 11:
            if (!(channel === m.change)) {
              _context15.next = 15;
              break;
            }

            state = m._getAllState();
            _context15.next = 22;
            break;

          case 15:
            solos = state.solos;

            if (!(solos.indexOf(channel) > -1 || solos.length === 0 && !(state.mutes.indexOf(channel) > -1))) {
              _context15.next = 22;
              break;
            }

            _context15.next = 19;
            return (0, _process.put)(out, _value);

          case 19:
            stillOpen = _context15.sent;

            if (stillOpen) {
              _context15.next = 22;
              break;
            }

            return _context15.abrupt('break', 24);

          case 22:
            _context15.next = 1;
            break;

          case 24:
          case 'end':
            return _context15.stop();
        }
      }
    }, _callee13, this);
  }));
  return m;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.mix.add"></a>[function <span class="apidocSignatureSpan">js-csp.operations.mix.</span>add (m, ch)](#apidoc.element.js-csp.operations.mix.add)
- description and source-code
```javascript
function admix(m, ch) {
  m.admix(ch);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.mix.remove"></a>[function <span class="apidocSignatureSpan">js-csp.operations.mix.</span>remove (m, ch)](#apidoc.element.js-csp.operations.mix.remove)
- description and source-code
```javascript
function unmix(m, ch) {
  m.unmix(ch);
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.mix.removeAll"></a>[function <span class="apidocSignatureSpan">js-csp.operations.mix.</span>removeAll (m)](#apidoc.element.js-csp.operations.mix.removeAll)
- description and source-code
```javascript
function unmixAll(m) {
  m.unmixAll();
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.mix.setSoloMode"></a>[function <span class="apidocSignatureSpan">js-csp.operations.mix.</span>setSoloMode (m, mode)](#apidoc.element.js-csp.operations.mix.setSoloMode)
- description and source-code
```javascript
function setSoloMode(m, mode) {
  m.setSoloMode(mode);
}
```
- example usage
```shell
...
};

mix.toggle = function toggle(m, updateStateList) {
  m.toggle(updateStateList);
};

mix.setSoloMode = function setSoloMode(m, mode) {
  m.setSoloMode(mode);
};

function constantlyNull() {
  return null;
}

var Pub = function () {
...
```

#### <a name="apidoc.element.js-csp.operations.mix.toggle"></a>[function <span class="apidocSignatureSpan">js-csp.operations.mix.</span>toggle (m, updateStateList)](#apidoc.element.js-csp.operations.mix.toggle)
- description and source-code
```javascript
function toggle(m, updateStateList) {
  m.toggle(updateStateList);
}
```
- example usage
```shell
...
};

mix.removeAll = function unmixAll(m) {
  m.unmixAll();
};

mix.toggle = function toggle(m, updateStateList) {
  m.toggle(updateStateList);
};

mix.setSoloMode = function setSoloMode(m, mode) {
  m.setSoloMode(mode);
};

function constantlyNull() {
...
```



# <a name="apidoc.module.js-csp.operations.mult"></a>[module js-csp.operations.mult](#apidoc.module.js-csp.operations.mult)

#### <a name="apidoc.element.js-csp.operations.mult.mult"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>mult (ch)](#apidoc.element.js-csp.operations.mult.mult)
- description and source-code
```javascript
function mult(ch) {
  var m = new Mult(ch);
  var dchan = (0, _csp.chan)(1);
  var dcount = void 0;

  function makeDoneCallback(tap) {
    return function (stillOpen) {
      dcount -= 1;
      if (dcount === 0) {
        (0, _process.putThenCallback)(dchan, true);
      }
      if (!stillOpen) {
        m.untap(tap.channel);
      }
    };
  }

  (0, _csp.go)(_regenerator2.default.mark(function _callee12() {
    var _this = this;

    var _loop, _ret;

    return _regenerator2.default.wrap(function _callee12$(_context14) {
      while (1) {
        switch (_context14.prev = _context14.next) {
          case 0:
            _loop = _regenerator2.default.mark(function _loop() {
              var value, taps, t, initDcount;
              return _regenerator2.default.wrap(function _loop$(_context13) {
                while (1) {
                  switch (_context13.prev = _context13.next) {
                    case 0:
                      _context13.next = 2;
                      return (0, _process.take)(ch);

                    case 2:
                      value = _context13.sent;
                      taps = m.taps;
                      t = void 0;

                      if (!(value === _channels.CLOSED)) {
                        _context13.next = 9;
                        break;
                      }

                      (0, _keys2.default)(taps).forEach(function (id) {
                        t = taps[id];
                        if (!t.keepOpen) {
                          t.channel.close();
                        }
                      });

                      // TODO: Is this necessary?
                      m.untapAll();
                      return _context13.abrupt('return', 'break');

                    case 9:
                      dcount = (0, _keys2.default)(taps).length;
                      // XXX: This is because putAsync can actually call back
                      // immediately. Fix that
                      initDcount = dcount;
                      // Put value on tapping channels...

                      (0, _keys2.default)(taps).forEach(function (id) {
                        t = taps[id];
                        (0, _process.putThenCallback)(t.channel, value, makeDoneCallback(t));
                      });
                      // ... waiting for all puts to complete

                      if (!(initDcount > 0)) {
                        _context13.next = 15;
                        break;
                      }

                      _context13.next = 15;
                      return (0, _process.take)(dchan);

                    case 15:
                    case 'end':
                      return _context13.stop();
                  }
                }
              }, _loop, _this);
            });

          case 1:
            return _context14.delegateYield(_loop(), 't0', 2);

          case 2:
            _ret = _context14.t0;

            if (!(_ret === 'break')) {
              _context14.next = 5;
              break;
            }

            return _context14.abrupt('break', 7);

          case 5:
            _context14.next = 1;
            break;

          case 7:
          case 'end':
            return _context14.stop();
        }
      }
    }, _callee12, this);
  }));
  return m;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.mult.tap"></a>[function <span class="apidocSignatureSpan">js-csp.operations.mult.</span>tap (m, ch, keepOpen)](#apidoc.element.js-csp.operations.mult.tap)
- description and source-code
```javascript
tap = function (m, ch, keepOpen) {
  m.tap(ch, keepOpen);
  return ch;
}
```
- example usage
```shell
...
      }
    }, _callee12, this);
  }));
  return m;
}

mult.tap = function (m, ch, keepOpen) {
  m.tap(ch, keepOpen);
  return ch;
};

mult.untap = function (m, ch) {
  m.untap(ch);
};
...
```

#### <a name="apidoc.element.js-csp.operations.mult.untap"></a>[function <span class="apidocSignatureSpan">js-csp.operations.mult.</span>untap (m, ch)](#apidoc.element.js-csp.operations.mult.untap)
- description and source-code
```javascript
untap = function (m, ch) {
  m.untap(ch);
}
```
- example usage
```shell
...
function makeDoneCallback(tap) {
  return function (stillOpen) {
    dcount -= 1;
    if (dcount === 0) {
      (0, _process.putThenCallback)(dchan, true);
    }
    if (!stillOpen) {
      m.untap(tap.channel);
    }
  };
}

(0, _csp.go)(_regenerator2.default.mark(function _callee12() {
  var _this = this;
...
```

#### <a name="apidoc.element.js-csp.operations.mult.untapAll"></a>[function <span class="apidocSignatureSpan">js-csp.operations.mult.</span>untapAll (m)](#apidoc.element.js-csp.operations.mult.untapAll)
- description and source-code
```javascript
untapAll = function (m) {
  m.untapAll();
}
```
- example usage
```shell
...
    t = taps[id];
    if (!t.keepOpen) {
      t.channel.close();
    }
  });

  // TODO: Is this necessary?
  m.untapAll();
  return _context13.abrupt('return', 'break');

case 9:
  dcount = (0, _keys2.default)(taps).length;
  // XXX: This is because putAsync can actually call back
  // immediately. Fix that
  initDcount = dcount;
...
```



# <a name="apidoc.module.js-csp.operations.pub"></a>[module js-csp.operations.pub](#apidoc.module.js-csp.operations.pub)

#### <a name="apidoc.element.js-csp.operations.pub.pub"></a>[function <span class="apidocSignatureSpan">js-csp.operations.</span>pub (ch, topicFn)](#apidoc.element.js-csp.operations.pub.pub)
- description and source-code
```javascript
function pub(ch, topicFn) {
  var bufferFn = arguments.length > 2 && arguments[2] !== undefined ? arguments[2] : constantlyNull;

  var p = new Pub(ch, topicFn, bufferFn);
  (0, _csp.go)(_regenerator2.default.mark(function _callee14() {
    var _this3 = this;

    var _loop3, _ret3;

    return _regenerator2.default.wrap(function _callee14$(_context17) {
      while (1) {
        switch (_context17.prev = _context17.next) {
          case 0:
            _loop3 = _regenerator2.default.mark(function _loop3() {
              var value, mults, topic, m, stillOpen;
              return _regenerator2.default.wrap(function _loop3$(_context16) {
                while (1) {
                  switch (_context16.prev = _context16.next) {
                    case 0:
                      _context16.next = 2;
                      return (0, _process.take)(ch);

                    case 2:
                      value = _context16.sent;
                      mults = p.mults;

                      if (!(value === _channels.CLOSED)) {
                        _context16.next = 7;
                        break;
                      }

                      (0, _keys2.default)(mults).forEach(function (topic) {
                        mults[topic].muxch().close();
                      });
                      return _context16.abrupt('return', 'break');

                    case 7:
                      // TODO: Somehow ensure/document that this must return a string
                      // (otherwise use proper (hash)maps)
                      topic = topicFn(value);
                      m = mults[topic];

                      if (!m) {
                        _context16.next = 14;
                        break;
                      }

                      _context16.next = 12;
                      return (0, _process.put)(m.muxch(), value);

                    case 12:
                      stillOpen = _context16.sent;

                      if (!stillOpen) {
                        delete mults[topic];
                      }

                    case 14:
                    case 'end':
                      return _context16.stop();
                  }
                }
              }, _loop3, _this3);
            });

          case 1:
            return _context17.delegateYield(_loop3(), 't0', 2);

          case 2:
            _ret3 = _context17.t0;

            if (!(_ret3 === 'break')) {
              _context17.next = 5;
              break;
            }

            return _context17.abrupt('break', 7);

          case 5:
            _context17.next = 1;
            break;

          case 7:
          case 'end':
            return _context17.stop();
        }
      }
    }, _callee14, this);
  }));
  return p;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.js-csp.operations.pub.sub"></a>[function <span class="apidocSignatureSpan">js-csp.operations.pub.</span>sub (p, topic, ch, keepOpen)](#apidoc.element.js-csp.operations.pub.sub)
- description and source-code
```javascript
sub = function (p, topic, ch, keepOpen) {
  return p.sub(topic, ch, keepOpen);
}
```
- example usage
```shell
...
      }
    }, _callee14, this);
  }));
  return p;
}

pub.sub = function (p, topic, ch, keepOpen) {
  return p.sub(topic, ch, keepOpen);
};

pub.unsub = function (p, topic, ch) {
  p.unsub(topic, ch);
};

pub.unsubAll = function (p, topic) {
...
```

#### <a name="apidoc.element.js-csp.operations.pub.unsub"></a>[function <span class="apidocSignatureSpan">js-csp.operations.pub.</span>unsub (p, topic, ch)](#apidoc.element.js-csp.operations.pub.unsub)
- description and source-code
```javascript
unsub = function (p, topic, ch) {
  p.unsub(topic, ch);
}
```
- example usage
```shell
...
}

pub.sub = function (p, topic, ch, keepOpen) {
  return p.sub(topic, ch, keepOpen);
};

pub.unsub = function (p, topic, ch) {
  p.unsub(topic, ch);
};

pub.unsubAll = function (p, topic) {
  p.unsubAll(topic);
};

function pipelineInternal(n, to, from, close, taskFn) {
...
```

#### <a name="apidoc.element.js-csp.operations.pub.unsubAll"></a>[function <span class="apidocSignatureSpan">js-csp.operations.pub.</span>unsubAll (p, topic)](#apidoc.element.js-csp.operations.pub.unsubAll)
- description and source-code
```javascript
unsubAll = function (p, topic) {
  p.unsubAll(topic);
}
```
- example usage
```shell
...
};

pub.unsub = function (p, topic, ch) {
p.unsub(topic, ch);
};

pub.unsubAll = function (p, topic) {
p.unsubAll(topic);
};

function pipelineInternal(n, to, from, close, taskFn) {
if (n <= 0) {
  throw new Error('n must be positive');
}
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

# cgminer-api

Complete cgminer API implementation for Node.js with multi-version support, response validation, and integration tests.

[![NPM version][npm-image]][npm-url]
[![Build status][travis-image]][travis-url]
[![Dependency Status][daviddm-image]][daviddm-url]

## Install
```sh
$ npm install cgminer-api --save
```

## Usage
```js
var Client = require('cgminer-api').client;
var cgminer = new Client({
  host: '192.168.1.99',
  port: 4028
});

cgminer.connect()
  .then(function () {
    return cgminer.version();
  })
  .then(function (version) {
    console.log(version);
  })
  .catch(function (error) {
    console.log(error);
  });
```

## License
MIT

[npm-image]: https://img.shields.io/npm/v/cgminer-api.svg?style=flat
[npm-url]: https://npmjs.org/package/cgminer-api
[travis-image]: https://img.shields.io/travis/flow23/node-cgminer.svg?style=flat
[travis-url]: https://travis-ci.org/flow23/node-cgminer
[daviddm-image]: https://david-dm.org/flow23/node-cgminer.svg
[daviddm-url]: https://david-dm.org/flow23/node-cgminer

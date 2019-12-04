# Unixcrypt for Node.js - JS version
[![Build Status](https://travis-ci.com/BonnierNews/unixcrypt-js.svg?branch=master)](https://travis-ci.com/BonnierNews/unixcrypt-js)

A Node.js module for encrypting and verifying passwords according to the SHA-256 and SHA-512 Crypt standard:
https://www.akkadia.org/drepper/SHA-crypt.txt . Based on the TypeScript package [unixcrypt](https://github.com/markusberg/unixcrypt).

## Dependencies

This package has no external dependencies. It uses the cryptographic facilities built into Node.js.

For development there are dependencies on Chai and Mocha.

## Usage

### JavaScript

```javascript
var unixcrypt = require("unixcrypt")

const plaintextPassword = "password"
const pwhash = unixcrypt.encrypt(plaintextPassword)

// verify password with generated hash
console.log(unixcrypt.verify(plaintextPassword, pwHash))
// true
```
## Test

The tests are written with [Chai](http://www.chaijs.com/), and [Mocha](https://mochajs.org/).

```sh
$ yarn test
```

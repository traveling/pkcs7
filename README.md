# pkcs7 [![Build Status](https://secure.travis-ci.org/brightcove/pkcs7.png?branch=master)](http://travis-ci.org/brightcove/pkcs7)

> Add and remove pkcs7-style padding.


## Getting Started

Install the module with: `npm install pkcs7`

```js
var pkcs7 = require('pkcs7'), encrypted;
// pad a buffer!
enctcrypted = encrypt(pkcs7.pad(buffer));

// later, you can unpad it:
console.log('the secret is out! ' + pkcs7.unpad(decrypt(encrypted)));
```

Install with cli command

```sh
$ npm install -g pkcs7
$ pkcs7 --help
$ pkcs7 --version
```

## Documentation

PKCS#7 padding a really simple transformation some crytographics algorithms use to ensure the number of input bytes is a multiple of some constant. Here's how it works:

             01 -- if lth mod k = k-1
          02 02 -- if lth mod k = k-2
              .
              .
              .
    k k ... k k -- if lth mod k = 0

`k` is the constant value the encryption algorithm wants your input to be a multiple of. This project assumes `k` is *always* sixteen. Not much to it, right? If reading specs is your thing, check out [RFC 5652](http://tools.ietf.org/html/rfc5652).


## Examples

_(Coming soon)_


## Contributing

In lieu of a formal styleguide, take care to maintain the existing coding style. Add unit tests for any new or changed functionality. Lint and test your code using [Grunt](http://gruntjs.com).


## License

Copyright (c) 2014 Brightcove  
Licensed under the Apache-2 license.

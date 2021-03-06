logcafe.js
============

# About

LogCafe.js is a logging framework to support browser application logging. (amd-style and node.js support)

# Usage (node.js)

```javascript
$ node
> var LogCafe = require('logcafe');
> var logCafe = new LogCafe();

> var conf = { // configure
...     level: 'DEBUG',
...     separator: ', '
... };

> logCafe.setConfigure(conf); // set configure
{ loggers: {},
  config: { level: 'DEBUG', separator: ', ' } }

> var log = logCafe.getLogger('logcafe'); // set Logger
> log.info('logger succesfully got', 'test'); // output log
[info][logcafe] logger succesfully got, test (......:xx:yy)
```

# Usage (browser)

```javascript
var logCafe = new LogCafe();

var conf = { // configure
    level: 'DEBUG',
    separator: ', '
};

logCafe.setConfigure(conf); // set configure

var log = logCafe.getLogger('logcafe'); // set Logger

log.info('logger succesfully got', 'test'); // output log

>> [info][logcafe] logger succesfully got, test (......:xx:yy)
```

## Configure

```javascript
{
    level: 'DEBUG', // OFF|TRACE|DEBUG|INFO|WARN|ERROR
    separator: ', ' // Consolidation of argument, it is a separator.
    excludes: [] // Exclude category forward match
}
```

## Operating environment

* node.js
* require.js
* browser

## Build

dependence) `node.js`

`$ npm install .`

`$ make`

## Test (browser)

```
$ open ./spec/all.html
```

## Test (node.js)

```
$ npm install . # deps install
$ make test

info: checking node_modules.
if [ ! -d ./node_modules ]; then npm install .; else exit 0; fi

info: testing start.
./node_modules/mocha/bin/mocha test/

  [info][logcafe] logger succesfully got (/Users/fkei/repos/logcafe.js/test/test.logcafe.js:28:17)
․

  1 test complete (16 ms)
```


# AUTHORS

## Kei FUNAGAYAMA

* [https://github.com/fkei](https://github.com/fkei)
* [https://twitter.com/fkei](https://twitter.com/fkei)

## Kazuma MISHIMAGI

* https://github.com/maginemu
* https://twitter.com/maginemu


## CyberAgent Publicity

* infosys_oss@cyberagent.co.jp

# Changelog

@see https://github.com/CyberAgent/logcafe.js/blob/master/Changelog


# Copyright

CyberAgent, Inc. All rights reserved.


# License

MIT @see https://github.com/CyberAgent/logcafe.js/blob/master/LICENSE

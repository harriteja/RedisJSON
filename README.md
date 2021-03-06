### RedisJSON2 can be found here https://github.com/RedisJSON/RedisJSON2

[![GitHub issues](https://img.shields.io/github/release/RedisJSON/RedisJSON.svg)](https://github.com/RedisJSON/RedisJSON/releases/latest)
[![CircleCI](https://circleci.com/gh/RedisJSON/RedisJSON/tree/master.svg?style=svg)](https://circleci.com/gh/RedisJSON/RedisJSON/tree/master)
[![Docker Cloud Build Status](https://img.shields.io/docker/cloud/build/redislabs/rejson.svg)](https://hub.docker.com/r/redislabs/rejson/builds/)
[![Mailing List](https://img.shields.io/badge/Mailing%20List-RedisJSON-blue)](https://groups.google.com/forum/#!forum/redisjson)
[![Gitter](https://badges.gitter.im/RedisLabs/RedisJSON.svg)](https://gitter.im/RedisLabs/RedisJSON?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge)

# RedisJSON - a JSON data type for Redis

RedisJSON is a [Redis](http://redis.io/) module that implements [ECMA-404 The JSON Data Interchange Standard](http://json.org/) as a native data type. It allows storing, updating and fetching JSON values from Redis keys (documents).

Primary features:

* Full support of the JSON standard
* [JSONPath](http://goessner.net/articles/JsonPath/)-like syntax for selecting element inside documents
* Documents are stored as binary data in a tree structure, allowing fast access to sub-elements
* Typed atomic operations for all JSON values types

## Quickstart

1.  [Launch RedisJSON with Docker](http://redisjson.io#launch-redisjson-with-docker)
1.  [Use RedisJSON from **any** Redis client](http://redisjson.io#using-redisjson), e.g.:

![RedisJSON with `redis-cli`](docs/images/demo.gif)

## Documentation

Read the docs at http://redisjson.io

## Client libraries

Some languages have client libraries that provide support for RedisJSON's commands:

| Project | Language | License | Author | URL |
| ------- | -------- | ------- | ------ | --- |
| iorejson | Node.js | MIT | [Evan Huang @evanhuang8](https://github.com/evanhuang8) | [git](https://github.com/evanhuang8/iorejson) [npm](https://www.npmjs.com/package/iorejson) |
| node_redis-rejson | Node.js | MIT | [Kyle Davis @stockholmux](https://github.com/stockholmux) | [git](https://github.com/stockholmux/node_redis-rejson) [npm](https://www.npmjs.com/package/redis-rejson) |
| JReJSON | Java | BSD-2-Clause | [Redis Labs](https://redislabs.com) | [git](https://github.com/RedisLabs/JReJSON/) |
| rejson-py | Python | BSD-2-Clause | [Redis Labs](https://redislabs.com) | [git](https://github.com/RedisLabs/rejson-py) [pypi](https://pypi.python.org/pypi/rejson) |
| go-rejson (multiple clients) | Go | MIT | [Nitish Malhotra @nitishm](https://github.com/nitishm) | [git](https://github.com/nitishm/go-rejson/) |
| jonson  (go-redis client)| Go | Apache-2.0 | [Daniel Krom @KromDaniel](https://github.com/KromDaniel) | [git](https://github.com/KromDaniel/rejonson) |
| NReJSON | .NET | MIT/Apache-2.0 | [Tommy Hanks @tombatron](https://github.com/tombatron) | [git](https://github.com/tombatron/NReJSON) |
| phpredis-json | PHP | MIT | [Rafa Campoy @averias](https://github.com/averias/) | [git](https://github.com/averias/phpredis-json) |
| redislabs-rejson | PHP | MIT | [Mehmet Korkmaz @mkorkmaz](https://github.com/mkorkmaz) | [git](https://github.com/mkorkmaz/redislabs-rejson/) |
| rejson-rb | Ruby | MIT | [Pavan Vachhani @vachhanihpavan](https://github.com/vachhanihpavan/) | [git](https://github.com/vachhanihpavan/rejson-rb) [rubygems](https://rubygems.org/gems/rejson-rb)|

## Current limitations and known issues

* Internal arrays are not scaled down after deleting items (i.e. free memory isn't reclaimed)
* Numbers are stored using 64-bit integers or doubles, and out of range values are not accepted

## Acknowledgements

RedisJSON is developed with <3 at [Redis Labs](https://redislabs.com).

RedisJSON is made possible only because of the existance of these amazing open source projects:

* [jsonsl](https://github.com/mnunberg/jsonsl)
* [redis](https://github.com/antirez/redis)

## License

Redis Source Available License Agreement - see [LICENSE](LICENSE)


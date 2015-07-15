# Aedes

Barebone MQTT server that can run on any stream server.

[![js-standard-style](https://cdn.rawgit.com/feross/standard/master/badge.svg)](https://github.com/feross/standard)

## Example

```js
var aedes = require('./aedes')()
var server = require('net').createServer(aedes.handle)
var port = 1883

server.listen(port, function () {
  console.log('server listening on port', port)
})
```

## Todo

* [x] QoS 0 support
* [x] Retain messages support
* [x] QoS 1 support
* [x] QoS 2 support
* [x] clean=false support
* [x] Keep alive support
* [x] Will messages must survive crash
* [ ] Authentication
* [ ] Mosca events
* [ ] Wait a CONNECT packet only for X seconds
* [ ] Support a CONNECT packet without a username
* [ ] Disconnect other clients with the same client.id
* [ ] move the persistence in a separate module
* [ ] mongo persistence (external module)
* [ ] redis persistence (external module)
* [ ] levelup persistence (external module)

## License

MIT

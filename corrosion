const Corrosion = require('corrosion');
const proxy = new Corrosion();
const http = require('http')
http.createServer((req, res) => 
  proxy.request(req, res) // Request Proxy
).on('upgrade', (req, socket, head) => 
  proxy.upgrade(req, socket, head) // WebSocket Proxy
).listen(80);

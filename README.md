# svrx-plugin-localtunnel

[localtunnel client](https://github.com/localtunnel/localtunnel) plugin for [svrx](https://github.com/x-orpheus/svrx)

This plugin is used to expose your local server to `localtunnel.me`

## Usage

> **please confirm you have [installed svrx](https://github.com/x-orpheus/svrx) already**

### cli

```bash
svrx -p localtunnel?subdomain=svrx
```

### manual

```js
const svrx = require('svrx');

svrx({ 
    plugins: ['localtunnel'] 
}).start();

```

**with options**

```js

svrx({
    plugins: [{
        name: 'localtunnel',
        options: {
            subdomain: 'svrx'
        }
    ]
}).start();
```

> example above will init https://svrx.localtunnel.me for you

## Options

### **subdomain \[String]:**

A string value requesting a specific subdomain on the proxy server

subdomain is **optional**, localtunnel will auto create a random domain for you.

### **localhost \[String]:**

Proxy to this hostname instead of localhost

localhost is **optional**

### **host \[Object]:**

specify host if you want to use custom [localtunnel/server](https://github.com/localtunnel/server) 

deafult is `https://localtunnel.me`




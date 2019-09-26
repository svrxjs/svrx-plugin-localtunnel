# svrx-plugin-localtunnel

[svrx](https://github.com/x-orpheus/svrx) plugin for [localtunnel](https://github.com/localtunnel/localtunnel) 

This plugin is used to expose your local server to `localtunnel.me`

## Usage

> **please confirm you have [installed svrx](https://github.com/x-orpheus/svrx) already**

### Via CLI

```bash
svrx -p "localtunnel"
```

### Via API

```js
const svrx = require('@svrx/svrx');

svrx({ 
    plugins: ['localtunnel'] 
}).start();

```

**With options**

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

> Example above will prepare https://svrx.localtunnel.me for you

## Options

### **subdomain \[String]:**

A string value requesting a specific subdomain on the proxy server

Subdomain is **optional**, localtunnel will auto create a random domain for you.

### **localhost \[String]:**

Proxy to this hostname instead of localhost

localhost is **optional**

### **host \[String]:**

specify host if you want to use custom [localtunnel/server](https://github.com/localtunnel/server) 

Deafult is `https://localtunnel.me`




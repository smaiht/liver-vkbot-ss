# express-glitch-keepalive

An [Express](http://expressjs.com/) middleware that keeps your [Glitch](https://glitch.com/) project alive.

Inspired by [koa-glitch-keepalive](https://github.com/matzkoh/koa-glitch-keepalive).

## Installation

`npm i --save express liver-vkbot-ss`

## Usage

```js
const express = require('express');
const keepalive = require('liver-vkbot-ss');

const app = express();

app.use(keepalive);

app.get('/', (req, res) => {
  res.json('Ok');
});
```
## Configuration

Keepalive can be configured in a number of ways:

- The request path to use defaults to `/_keepalive` but can be changed with the environment variable `KEEPALIVE_PATH`.
- The delay between keepalive requests defaults to **3 minutes** but can be changed with the environment variable `KEEPALIVE_MINUTES`.

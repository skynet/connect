# Connect [![build status](https://secure.travis-ci.org/senchalabs/connect.png)](http://travis-ci.org/senchalabs/connect)

  Connect is an extensible HTTP server framework for [node](http://nodejs.org) using "plugins" known as _middleware_.

```js
var connect = require('connect')
  , http = require('http');

var app = connect()
  .use(require('compression')())
  .use(require('')())
  .use(require('')())
  .use(function(req, res){
    res.end('Hello from Connect!\n');
  });

http.createServer(app).listen(3000);
```

## Connect 3.0

Connect 3.0 is in progress in the `master` branch. The main changes in Connect are:

- Middleware will be moved to their own repositories in the [expressjs](http://github.com/expressjs) organization
- All node patches will be removed - all middleware _should_ work without Connect and with similar frameworks like [restify](https://github.com/mcavage/node-restify)
- Node `0.8` is no longer supported
- The website documentation has been removed - view the markdown readmes instead

If you would like to help maintain these middleware, please contact [@jongleberry](https://twitter.com/jongleberry).

## Middleware

These middleware are officially supported by the Connect/Express team:

  - [body-parser](https://github.com/expressjs/body-parser) - previous `bodyParser`, `json`, and `urlencoded`. You may also be interested in:
    - [body](https://github.com/raynos/body)
    - [co-body](https://github.com/visionmedia/co-body)
    - [raw-body](https://github.com/stream-utils/raw-body)
  - [compression](https://github.com/expressjs/compression) - previously `compress`
  - [morgan](https://github.com/expressjs/morgan) - previously `logger`
  - [express-session](https://github.com/expressjs/session) - previously `session`
  - [static-favicon](https://github.com/expressjs/favicon) - previously `favicon`
  - [response-time](https://github.com/expressjs/response-time) - previously `response-time`

These middleware previously included with Connect are no longer supported by the Connect/Express team or are replaced by an alternative module. Use one of these alternatives intead:

  - `cookieParser`
    - [cookies](https://github.com/jed/cookies) and [keygrip](https://github.com/jed/keygrip)
  - `limit`
    - [raw-body](https://github.com/stream-utils/raw-body)
  - `multipart`
    - [connect-multiparty](https://github.com/superjoe30/connect-multiparty)
    - [connect-busboy](https://github.com/mscdex/connect-busboy)
  - `staticCache`
    - [st](https://github.com/isaacs/st)
  - `query`
    - [qs](https://github.com/visionmedia/node-querystring)

## Running Tests

```bash
npm install
make test
```

## Contributors

 https://github.com/senchalabs/connect/graphs/contributors

## Node Compatibility

  - Connect `< 1.x` - node `0.2`
  - Connect `1.x` - node `0.4`
  - Connect `< 2.8` - node `0.6`
  - Connect `>= 2.8 < 3` - node `0.8`
  - Connect `>= 3` - node `0.10`

## License

View the [LICENSE](https://github.com/senchalabs/connect/blob/master/LICENSE) file. The [Silk](http://www.famfamfam.com/lab/icons/silk/) icons used by the `directory` middleware created by/copyright of [FAMFAMFAM](http://www.famfamfam.com/).

# api documentation for  [passport-local (v1.0.0)](https://github.com/jaredhanson/passport-local#readme)  [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-passport-local.svg)](https://travis-ci.org/npmdoc/node-npmdoc-passport-local)
#### Local username and password authentication strategy for Passport.

[![NPM](https://nodei.co/npm/passport-local.png?downloads=true)](https://www.npmjs.com/package/passport-local)

[![apidoc](https://npmdoc.github.io/node-npmdoc-passport-local/build/screen-capture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-passport_local_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-passport-local/build..beta..travis-ci.org/apidoc.html)

![package-listing](https://npmdoc.github.io/node-npmdoc-passport-local/build/screen-capture.npmPackageListing.svg)



# package.json

```json

{
    "author": {
        "name": "Jared Hanson",
        "email": "jaredhanson@gmail.com",
        "url": "http://www.jaredhanson.net/"
    },
    "bugs": {
        "url": "http://github.com/jaredhanson/passport-local/issues"
    },
    "dependencies": {
        "passport-strategy": "1.x.x"
    },
    "description": "Local username and password authentication strategy for Passport.",
    "devDependencies": {
        "chai": "1.x.x",
        "chai-passport-strategy": "0.1.x",
        "mocha": "1.x.x"
    },
    "directories": {},
    "dist": {
        "shasum": "1fe63268c92e75606626437e3b906662c15ba6ee",
        "tarball": "https://registry.npmjs.org/passport-local/-/passport-local-1.0.0.tgz"
    },
    "engines": {
        "node": ">= 0.4.0"
    },
    "homepage": "https://github.com/jaredhanson/passport-local#readme",
    "keywords": [
        "passport",
        "local",
        "auth",
        "authn",
        "authentication",
        "username",
        "password"
    ],
    "licenses": [
        {
            "type": "MIT",
            "url": "http://www.opensource.org/licenses/MIT"
        }
    ],
    "main": "./lib",
    "maintainers": [
        {
            "name": "jaredhanson",
            "email": "jaredhanson@gmail.com"
        }
    ],
    "name": "passport-local",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git://github.com/jaredhanson/passport-local.git"
    },
    "scripts": {
        "test": "node_modules/.bin/mocha --reporter spec --require test/bootstrap/node test/*.test.js"
    },
    "version": "1.0.0"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module passport-local](#apidoc.module.passport-local)
1.  [function <span class="apidocSignatureSpan">passport-local.</span>Strategy (options, verify)](#apidoc.element.passport-local.Strategy)
1.  [function <span class="apidocSignatureSpan">passport-local.</span>super_ ()](#apidoc.element.passport-local.super_)
1.  object <span class="apidocSignatureSpan">passport-local.</span>super_.prototype
1.  object <span class="apidocSignatureSpan">passport-local.</span>utils

#### [module passport-local.super_](#apidoc.module.passport-local.super_)
1.  [function <span class="apidocSignatureSpan">passport-local.</span>super_ ()](#apidoc.element.passport-local.super_.super_)
1.  [function <span class="apidocSignatureSpan">passport-local.super_.</span>Strategy ()](#apidoc.element.passport-local.super_.Strategy)

#### [module passport-local.super_.prototype](#apidoc.module.passport-local.super_.prototype)
1.  [function <span class="apidocSignatureSpan">passport-local.super_.prototype.</span>authenticate (req, options)](#apidoc.element.passport-local.super_.prototype.authenticate)

#### [module passport-local.utils](#apidoc.module.passport-local.utils)
1.  [function <span class="apidocSignatureSpan">passport-local.utils.</span>lookup (obj, field)](#apidoc.element.passport-local.utils.lookup)



# <a name="apidoc.module.passport-local"></a>[module passport-local](#apidoc.module.passport-local)

#### <a name="apidoc.element.passport-local.Strategy"></a>[function <span class="apidocSignatureSpan">passport-local.</span>Strategy (options, verify)](#apidoc.element.passport-local.Strategy)
- description and source-code
```javascript
function Strategy(options, verify) {
  if (typeof options == 'function') {
    verify = options;
    options = {};
  }
  if (!verify) { throw new TypeError('LocalStrategy requires a verify callback'); }

  this._usernameField = options.usernameField || 'username';
  this._passwordField = options.passwordField || 'password';

  passport.Strategy.call(this);
  this.name = 'local';
  this._verify = verify;
  this._passReqToCallback = options.passReqToCallback;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.passport-local.super_"></a>[function <span class="apidocSignatureSpan">passport-local.</span>super_ ()](#apidoc.element.passport-local.super_)
- description and source-code
```javascript
function Strategy() {
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.passport-local.super_"></a>[module passport-local.super_](#apidoc.module.passport-local.super_)

#### <a name="apidoc.element.passport-local.super_.super_"></a>[function <span class="apidocSignatureSpan">passport-local.</span>super_ ()](#apidoc.element.passport-local.super_.super_)
- description and source-code
```javascript
function Strategy() {
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.passport-local.super_.Strategy"></a>[function <span class="apidocSignatureSpan">passport-local.super_.</span>Strategy ()](#apidoc.element.passport-local.super_.Strategy)
- description and source-code
```javascript
function Strategy() {
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.passport-local.super_.prototype"></a>[module passport-local.super_.prototype](#apidoc.module.passport-local.super_.prototype)

#### <a name="apidoc.element.passport-local.super_.prototype.authenticate"></a>[function <span class="apidocSignatureSpan">passport-local.super_.prototype.</span>authenticate (req, options)](#apidoc.element.passport-local.super_.prototype.authenticate)
- description and source-code
```javascript
authenticate = function (req, options) {
  throw new Error('Strategy#authenticate must be overridden by subclass');
}
```
- example usage
```shell
...
      return done(null, user);
    });
  }
));

#### Authenticate Requests

Use 'passport.authenticate()', specifying the ''local'' strategy, to
authenticate requests.

For example, as route middleware in an [Express](http://expressjs.com/)
application:

app.post('/login',
  passport.authenticate('local', { failureRedirect: '/login' }),
...
```



# <a name="apidoc.module.passport-local.utils"></a>[module passport-local.utils](#apidoc.module.passport-local.utils)

#### <a name="apidoc.element.passport-local.utils.lookup"></a>[function <span class="apidocSignatureSpan">passport-local.utils.</span>lookup (obj, field)](#apidoc.element.passport-local.utils.lookup)
- description and source-code
```javascript
lookup = function (obj, field) {
  if (!obj) { return null; }
  var chain = field.split(']').join('').split('[');
  for (var i = 0, len = chain.length; i < len; i++) {
    var prop = obj[chain[i]];
    if (typeof(prop) === 'undefined') { return null; }
    if (typeof(prop) !== 'object') { return prop; }
    obj = prop;
  }
  return null;
}
```
- example usage
```shell
n/a
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

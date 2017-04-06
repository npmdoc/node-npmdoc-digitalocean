# api documentation for  [digitalocean (v0.9.1)](https://github.com/phillbaker/digitalocean-node#readme)  [![npm package](https://img.shields.io/npm/v/npmdoc-digitalocean.svg?style=flat-square)](https://www.npmjs.org/package/npmdoc-digitalocean) [![travis-ci.org build-status](https://api.travis-ci.org/npmdoc/node-npmdoc-digitalocean.svg)](https://travis-ci.org/npmdoc/node-npmdoc-digitalocean)
#### nodejs wrapper for digitalocean v2 api

[![NPM](https://nodei.co/npm/digitalocean.png?downloads=true)](https://www.npmjs.com/package/digitalocean)

[![apidoc](https://npmdoc.github.io/node-npmdoc-digitalocean/build/screenCapture.buildNpmdoc.browser._2Fhome_2Ftravis_2Fbuild_2Fnpmdoc_2Fnode-npmdoc-digitalocean_2Ftmp_2Fbuild_2Fapidoc.html.png)](https://npmdoc.github.io/node-npmdoc-digitalocean/build/apidoc.html)

![npmPackageListing](https://npmdoc.github.io/node-npmdoc-digitalocean/build/screenCapture.npmPackageListing.svg)

![npmPackageDependencyTree](https://npmdoc.github.io/node-npmdoc-digitalocean/build/screenCapture.npmPackageDependencyTree.svg)



# package.json

```json

{
    "author": {
        "name": "Phillip Baker",
        "email": "phillbaker@retrodict.com"
    },
    "bugs": {
        "url": "https://github.com/phillbaker/digitalocean-node/issues"
    },
    "dependencies": {
        "bluebird": "^3.0",
        "deep-extend": "0.x.x",
        "request": "^2.50"
    },
    "description": "nodejs wrapper for digitalocean v2 api",
    "devDependencies": {
        "bower": ">= 0.0.0",
        "browserify": "^13.0.0",
        "chai": "~1.10.0",
        "chai-shallow-deep-equal": "^1.4.0",
        "jsdoc": "3.4.0",
        "mocha": "~2.1.0",
        "mocha-jshint": "^2.3.1",
        "nock": "0.57.x"
    },
    "directories": {},
    "dist": {
        "shasum": "aec145c104fa91f76ad8fab115f609fd4340b2b6",
        "tarball": "https://registry.npmjs.org/digitalocean/-/digitalocean-0.9.1.tgz"
    },
    "engines": {
        "node": ">0.4.11",
        "npm": ">= 2.13.1"
    },
    "gitHead": "b34f83df3ff54b664fc7cad62ff2a871c8969306",
    "homepage": "https://github.com/phillbaker/digitalocean-node#readme",
    "keywords": [
        "wrapper",
        "api",
        "v2",
        "digital ocean",
        "digitalocean",
        "droplet"
    ],
    "license": "MIT",
    "main": "./lib/digitalocean",
    "maintainers": [
        {
            "name": "phillbaker",
            "email": "phillbaker@retrodict.com"
        }
    ],
    "name": "digitalocean",
    "optionalDependencies": {},
    "readme": "ERROR: No README data found!",
    "repository": {
        "type": "git",
        "url": "git+https://github.com/phillbaker/digitalocean-node.git"
    },
    "scripts": {
        "build": "mkdir -p dist && npm run build:js && npm run doc",
        "build:js": "browserify lib/digitalocean.js -o dist/digitalocean.js --standalone 'digitalocean'",
        "clean": "rm -r dist/*",
        "doc": "jsdoc lib/ --configure jsdoc.conf.json",
        "preversion": "npm test",
        "release": "git push --follow-tags && npm publish",
        "release:major": "npm version major -m 'Bump version to %s'",
        "release:minor": "npm version minor -m 'Bump version to %s'",
        "release:patch": "npm version patch -m 'Bump version to %s'",
        "test": "mocha --bail --recursive --reporter dot",
        "version": "npm run build && git add -A dist"
    },
    "tonicExampleFilename": "examples/make_droplet.js",
    "version": "0.9.1"
}
```



# <a name="apidoc.tableOfContents"></a>[table of contents](#apidoc.tableOfContents)

#### [module digitalocean](#apidoc.module.digitalocean)
1.  [function <span class="apidocSignatureSpan">digitalocean.</span>account (client)](#apidoc.element.digitalocean.account)
1.  [function <span class="apidocSignatureSpan">digitalocean.</span>client (token, options)](#apidoc.element.digitalocean.client)
1.  object <span class="apidocSignatureSpan">digitalocean.</span>account.prototype

#### [module digitalocean.account](#apidoc.module.digitalocean.account)
1.  [function <span class="apidocSignatureSpan">digitalocean.</span>account (client)](#apidoc.element.digitalocean.account.account)

#### [module digitalocean.account.prototype](#apidoc.module.digitalocean.account.prototype)
1.  [function <span class="apidocSignatureSpan">digitalocean.account.prototype.</span>createSshKey (attributes, callback)](#apidoc.element.digitalocean.account.prototype.createSshKey)
1.  [function <span class="apidocSignatureSpan">digitalocean.account.prototype.</span>deleteSshKey (id, callback)](#apidoc.element.digitalocean.account.prototype.deleteSshKey)
1.  [function <span class="apidocSignatureSpan">digitalocean.account.prototype.</span>get (callback)](#apidoc.element.digitalocean.account.prototype.get)
1.  [function <span class="apidocSignatureSpan">digitalocean.account.prototype.</span>getSshKey (id, callback)](#apidoc.element.digitalocean.account.prototype.getSshKey)
1.  [function <span class="apidocSignatureSpan">digitalocean.account.prototype.</span>listSshKeys ()](#apidoc.element.digitalocean.account.prototype.listSshKeys)
1.  [function <span class="apidocSignatureSpan">digitalocean.account.prototype.</span>updateSshKey (id, attributes, callback)](#apidoc.element.digitalocean.account.prototype.updateSshKey)



# <a name="apidoc.module.digitalocean"></a>[module digitalocean](#apidoc.module.digitalocean)

#### <a name="apidoc.element.digitalocean.account"></a>[function <span class="apidocSignatureSpan">digitalocean.</span>account (client)](#apidoc.element.digitalocean.account)
- description and source-code
```javascript
function Account(client) {
  this.client = client;
}
```
- example usage
```shell
n/a
```

#### <a name="apidoc.element.digitalocean.client"></a>[function <span class="apidocSignatureSpan">digitalocean.</span>client (token, options)](#apidoc.element.digitalocean.client)
- description and source-code
```javascript
client = function (token, options) {
  return new Client(token, options);
}
```
- example usage
```shell
...

## Usage

Every resource is accessed via an instance of the client. Please [chose one of your tokens](https://cloud.digitalocean.com/settings
/api/tokens) and use that where ever 'TOKEN' is referenced. For example:

'''js
var digitalocean = require('digitalocean');
var client = digitalocean.client('TOKEN'); // See
// client.{ RESOURCE_NAME }.{ METHOD_NAME }
'''

Every resource method accepts an optional callback as the last argument. For example:

'''js
client.account.get(function(err, account) {
...
```



# <a name="apidoc.module.digitalocean.account"></a>[module digitalocean.account](#apidoc.module.digitalocean.account)

#### <a name="apidoc.element.digitalocean.account.account"></a>[function <span class="apidocSignatureSpan">digitalocean.</span>account (client)](#apidoc.element.digitalocean.account.account)
- description and source-code
```javascript
function Account(client) {
  this.client = client;
}
```
- example usage
```shell
n/a
```



# <a name="apidoc.module.digitalocean.account.prototype"></a>[module digitalocean.account.prototype](#apidoc.module.digitalocean.account.prototype)

#### <a name="apidoc.element.digitalocean.account.prototype.createSshKey"></a>[function <span class="apidocSignatureSpan">digitalocean.account.prototype.</span>createSshKey (attributes, callback)](#apidoc.element.digitalocean.account.prototype.createSshKey)
- description and source-code
```javascript
createSshKey = function (attributes, callback) {
  return this.client.post('/account/keys', attributes, 201, 'ssh_key', callback);
}
```
- example usage
```shell
...
var client = digitalocean.client('TOKEN');
client.account
'''

* 'client.account.get([callback])'
* 'client.account.listSshKeys([page, perPage,] [callback])'
* 'client.account.listSshKeys([queryObject,] [callback])'
* 'client.account.createSshKey(attributes, [callback])'
* 'client.account.getSshKey(sshKey.id, [callback])'
* 'client.account.deleteSshKey(sshKey.id, [callback])'
* 'client.account.updateSshKey(sshKey.id, attributes, [callback])'

For the latest ssh key valid attributes, [see the official docs](https://developers.digitalocean.com/documentation/v2/#ssh-keys).

### Floating IP resource
...
```

#### <a name="apidoc.element.digitalocean.account.prototype.deleteSshKey"></a>[function <span class="apidocSignatureSpan">digitalocean.account.prototype.</span>deleteSshKey (id, callback)](#apidoc.element.digitalocean.account.prototype.deleteSshKey)
- description and source-code
```javascript
deleteSshKey = function (id, callback) {
  var url = util.safeUrl('account', 'keys', id);
  return this.client.delete(url, {}, 204, [], callback);
}
```
- example usage
```shell
...
'''

* 'client.account.get([callback])'
* 'client.account.listSshKeys([page, perPage,] [callback])'
* 'client.account.listSshKeys([queryObject,] [callback])'
* 'client.account.createSshKey(attributes, [callback])'
* 'client.account.getSshKey(sshKey.id, [callback])'
* 'client.account.deleteSshKey(sshKey.id, [callback])'
* 'client.account.updateSshKey(sshKey.id, attributes, [callback])'

For the latest ssh key valid attributes, [see the official docs](https://developers.digitalocean.com/documentation/v2/#ssh-keys).

### Floating IP resource

'''js
...
```

#### <a name="apidoc.element.digitalocean.account.prototype.get"></a>[function <span class="apidocSignatureSpan">digitalocean.account.prototype.</span>get (callback)](#apidoc.element.digitalocean.account.prototype.get)
- description and source-code
```javascript
get = function (callback) {
  return this.client.get('/account', {}, 200, 'account', callback);
}
```
- example usage
```shell
...
var client = digitalocean.client('TOKEN'); // See
// client.{ RESOURCE_NAME }.{ METHOD_NAME }
'''

Every resource method accepts an optional callback as the last argument. For example:

'''js
client.account.get(function(err, account) {
  console.log(err); // null on success
  console.log(account); //
});
'''

See below [for more options in the callback](#api-callback-structure).
...
```

#### <a name="apidoc.element.digitalocean.account.prototype.getSshKey"></a>[function <span class="apidocSignatureSpan">digitalocean.account.prototype.</span>getSshKey (id, callback)](#apidoc.element.digitalocean.account.prototype.getSshKey)
- description and source-code
```javascript
getSshKey = function (id, callback) {
  var url = util.safeUrl('account', 'keys', id);
  return this.client.get(url, {}, 200, 'ssh_key', callback);
}
```
- example usage
```shell
...
client.account
'''

* 'client.account.get([callback])'
* 'client.account.listSshKeys([page, perPage,] [callback])'
* 'client.account.listSshKeys([queryObject,] [callback])'
* 'client.account.createSshKey(attributes, [callback])'
* 'client.account.getSshKey(sshKey.id, [callback])'
* 'client.account.deleteSshKey(sshKey.id, [callback])'
* 'client.account.updateSshKey(sshKey.id, attributes, [callback])'

For the latest ssh key valid attributes, [see the official docs](https://developers.digitalocean.com/documentation/v2/#ssh-keys).

### Floating IP resource
...
```

#### <a name="apidoc.element.digitalocean.account.prototype.listSshKeys"></a>[function <span class="apidocSignatureSpan">digitalocean.account.prototype.</span>listSshKeys ()](#apidoc.element.digitalocean.account.prototype.listSshKeys)
- description and source-code
```javascript
listSshKeys = function () {
  var args = util.extractListArguments(arguments, 0);
  return this.client.get.apply(this.client, ['/account/keys', {}].concat(slice.call(args.params), [200, 'ssh_keys', args.callback
]));
}
```
- example usage
```shell
...
'''js
var digitalocean = require('digitalocean');
var client = digitalocean.client('TOKEN');
client.account
'''

* 'client.account.get([callback])'
* 'client.account.listSshKeys([page, perPage,] [callback])'
* 'client.account.listSshKeys([queryObject,] [callback])'
* 'client.account.createSshKey(attributes, [callback])'
* 'client.account.getSshKey(sshKey.id, [callback])'
* 'client.account.deleteSshKey(sshKey.id, [callback])'
* 'client.account.updateSshKey(sshKey.id, attributes, [callback])'

For the latest ssh key valid attributes, [see the official docs](https://developers.digitalocean.com/documentation/v2/#ssh-keys).
...
```

#### <a name="apidoc.element.digitalocean.account.prototype.updateSshKey"></a>[function <span class="apidocSignatureSpan">digitalocean.account.prototype.</span>updateSshKey (id, attributes, callback)](#apidoc.element.digitalocean.account.prototype.updateSshKey)
- description and source-code
```javascript
updateSshKey = function (id, attributes, callback) {
  var url = util.safeUrl('account', 'keys', id);
  return this.client.put(url, attributes, 200, 'ssh_key', callback);
}
```
- example usage
```shell
...

* 'client.account.get([callback])'
* 'client.account.listSshKeys([page, perPage,] [callback])'
* 'client.account.listSshKeys([queryObject,] [callback])'
* 'client.account.createSshKey(attributes, [callback])'
* 'client.account.getSshKey(sshKey.id, [callback])'
* 'client.account.deleteSshKey(sshKey.id, [callback])'
* 'client.account.updateSshKey(sshKey.id, attributes, [callback])'

For the latest ssh key valid attributes, [see the official docs](https://developers.digitalocean.com/documentation/v2/#ssh-keys).

### Floating IP resource

'''js
var digitalocean = require('digitalocean');
...
```



# misc
- this document was created with [utility2](https://github.com/kaizhu256/node-utility2)

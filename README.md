# minimal-dust

This package is a simple re-packaging of dustjs-linkedin and dustjs-helpers
with minimal modifications to streamline loading as a node module with no
dependencies.

The primary motivation for this is to remove the dependencies which were only
being used for the `dustc` CLI and introduced many nested dependencies which
are frequent sources of security warnings.

## Usage

This module is a drop-in replacement for the simple server-side usage of
dustjs-helpers@1.7.x with dustjs-linkedin included.

If you are using dustjs-helpers to load dustjs-linkedin and have something
like this in your code:

```js
//...
var dust = require('dustjs-helpers');
//...
```

Then all you need to do is replace it with `minimal-dust` like so:

```js
//...
var dust = require('minimal-dust');
//...
```

And then replace the dependencies:

```sh
npm uninstall --save dustjs-helpers dustjs-linkedin
npm install --save minimal-dust
```

For API and other similar documentation, see the official dustjs docs at http://www.dustjs.com/

## License

dust-helpers.js and the dustjs template engine are used under the terms of an
MIT license, Copyright (c) 2010 Aleksander Williams.

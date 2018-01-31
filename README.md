# Native JavaScript for Bootstrap
This is a library developed with native JavaScript for both **Bootstrap 3** and **Bootstrap 4** series, featuring superior performance compared to the original jQuery Plugins.

[![NPM Version](https://img.shields.io/npm/v/bootstrap.native.svg?style=flat-square)](https://www.npmjs.com/package/bootstrap.native)
[![NPM Downloads](https://img.shields.io/npm/dm/bootstrap.native.svg?style=flat-square)](http://npm-stat.com/charts.html?package=bootstrap.native)
[![jsDeliver](https://data.jsdelivr.com/v1/package/npm/bootstrap.native/badge)](https://www.jsdelivr.com/package/npm/bootstrap.native)
[![CDNJS](https://img.shields.io/cdnjs/v/bootstrap.native.svg?style=flat-square)](https://cdnjs.com/libraries/bootstrap.native)

 The library is under ***20Kb*** minified and ***6.5Kb*** gZipped. See <a href="http://thednp.github.io/bootstrap.native/">demo</a> for scripting examples and instructions.

If you use webpack, here here is the accompanying [webpack loader](https://github.com/jonathanfleckenstein/bootstrap.native-loader).

<<<<<<< HEAD
```
$ npm install --save bootstrap.native--virajsoni06
# Or
$ bower install --save bootstrap.native--virajsoni06
```

# Usage

`bootstrap.native` is UMD (Universal Module Definition) compatible. It will work correctly in CommonJS and AMD environments, but falls back to exporting to `window` in a normal `<script>` tag environment.

**Traditional script-tag example:**

```html
<!-- Using one of the CDN repositories-->
<script type="text/javascript" src="//cdn.jsdelivr.net/bootstrap.native/2.0.12/bootstrap-native.min.js"></script>
<script type="text/javascript" src="//cdnjs.cloudflare.com/ajax/libs/bootstrap.native/2.0.12/bootstrap-native.min.js"></script>
<!-- Using a local assets folder -->
<script type="text/javascript" src="/assets/js/bootstrap-native.min.js"></script>
<!-- Using Bower -->
<script type="text/javascript" src="/bower_components/bootstrap.native/dist/bootstrap-native.min.js"></script>
```

**Use the Bootstrap 4 version:**

```html
<!-- Using one of the CDN repositories-->
<script type="text/javascript" src="//cdn.jsdelivr.net/bootstrap.native/2.0.12/bootstrap-native-v4.min.js"></script>
<script type="text/javascript" src="//cdnjs.cloudflare.com/ajax/libs/bootstrap.native/2.0.12/bootstrap-native-v4.min.js"></script>
<!-- Using a local assets folder -->
<script type="text/javascript" src="/assets/js/bootstrap-native-v4.min.js"></script>
<!-- Using Bower -->
<script type="text/javascript" src="/bower_components/bootstrap.native/dist/bootstrap-native-v4.min.js"></script>
```

**Warning:** Do not use files directly from `/lib` folder! These files are just sources for the builds located in the `/dist` folder.

You can also use `bootstrap.native` in a CommonJS environment:

```js
var bsn = require("bootstrap.native");
// Create a button:
var btn = new bsn.Button(element,'loading');
```

Additionally, to use V4, you can do the following:
```
var bsn = require('bootstrap.native/dist/bootstrap-native-v4');
var btn = new bsn.Button(element,'loading');
```

**Note:** If you are working in a virtual browser environment (i.e. running front-end tests in NodeJS), `bootstrap.native` requires both `window` and `document` to be in scope. You will need to use a mock browser.


## Note About the Factory Methods
As mentioned above, the object properties of the exported object, when using `require()`, are actual classes when `document` and `window` are given - in which case we are sure to be facing an actual browser - and if absent, will be factory methods.

So when using `bootstrap.native` inside of a NodeJS app, make sure you create a proper Browser-like environment first to avoid unexpected behaviour.

# Browser Support
The components are developed with clean code mainly for modern browsers that nativelly support HTML5. When using polyfills, IE8-IE10 will thank you. The library comes with a custom polyfill you can use right away.

```html
<!-- Using one of the CDN repositories-->
<script type="text/javascript" src="//cdn.jsdelivr.net/bootstrap.native/2.0.12/polyfill.min.js"></script>
<script type="text/javascript" src="//cdnjs.cloudflare.com/ajax/libs/bootstrap.native/2.0.12/polyfill.min.js"></script>
<!-- Using a local assets folder -->
<script type="text/javascript" src="/assets/js/polyfill.min.js"></script>
<!-- Using Bower -->
<script type="text/javascript" src="/bower_components/bootstrap.native/dist/polyfill.min.js"></script>
```

# Custom Builds
You can make a custom build of bootstrap-native, including only the modules you need, by using the `build.js` and `build-v4.js` scripts.

## Usage:
```
$ node build.js --help
node build.js [--minify] [--ignore=<modules>...|--only=<modules>...]

Options:
  --minify, -m  Minify output                         [boolean] [default: false]
  --ignore, -i  Omit the given module(s) from the bundle                 [array]
  --only        Only include the given module(s) in the bundle           [array]
  --help        Show help                                              [boolean]

Running without --ignore or --only will compile all the modules.
Writes to stdout
```

\*nix users can run `./build.js` as well as `node build.js`.
=======
# Wiki
Please take a minute to check the `bootstrap.native` Wiki pages, they're updated with every new commit:
* [Acknowledgements](https://github.com/thednp/bootstrap.native/wiki/Acknowledgements) - A quick note on some of the similarities and differences with the original jQuery plugins. Nothing to worry about, but still good to know all the tricks on how to maximize your workflow.
* [How to use](https://github.com/thednp/bootstrap.native/wiki/How-to-use) - An in depth guide on how to use it with stuff like `npm`, `RequireJS` or `CDN` links.
* [Browser support](https://github.com/thednp/bootstrap.native/wiki/Browser-support) - A word on how to enable the library for legacy browsers.
* [FAQs](https://github.com/thednp/bootstrap.native/wiki/FAQs) - A short list of frequent asked questions regarding the use of the library.
* [About](https://github.com/thednp/bootstrap.native/wiki/About) - Learn about the `bootstrap.native` project inception, goals and motivations.
>>>>>>> 641148791eb03a68014b0b9857530a5a91299e56

# Original Contributors
- [Ingwie Phoenix](https://github.com/IngwiePhoenix): RequireJS/CommonJS compatibility and usability with common package managers. _Was glad to help!_
- [Ryan Zimmerman](https://github.com/RyanZim): **Amazing** custom build script.
- Full contributors list [here](https://github.com/thednp/bootstrap.native/graphs/contributors). Thanks so much!

# Fork Contributors
- [Viraj Soni](https://github.com/virajsoni06)

# License
The library is released under the [MIT license](https://github.com/thednp/bootstrap.native/blob/master/LICENSE).
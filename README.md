# interactive-examples

[![Build Status](https://travis-ci.org/mdn/interactive-examples.svg?branch=master)](https://travis-ci.org/mdn/interactive-examples)

Home of the [MDN](https://developer.mozilla.org/) interactive code examples.

## Folder structure

* [css] - This contains the CSS used by the base templates.
* [js] - This contains the JS used by the base templates.
* [live-examples] - This contains the live example CSS and JS fragments.
* [media] - The contains images used by the live examples and templates.
* [tmpl] - The base templates.

The dynamically generated pages, their dependencies, and assets are generated to the `gh-pages` branch.

## site.json

This describes the pages and bundles that make up the live examples.

### Bundles

Bundles are mainly used by the base templates, and look like so:

```
"cssExamplesBase": {
    "javascript": ["js/lib/prism.js", "js/editable-css.js"],
    "css": ["css/editable-css.css", "css/libs/prism.css"],
    "destFileName": "css-examples-base"
},
```

* `javascript` - This is an array of JS files that will be concatenated and Uglified.
* `css` - This is an array of CSS files that will be concatenated.
* `destFileName` - The file name to use for the generated bundle; `.css` or `.js` will be appended as appropriate.

### Pages

This section is used to describe live example pages that will be generated. The schema is as follows:

```
"arrayFind": {
    "baseTmpl": "tmpl/live-js-tmpl.html",
    ["cssExampleSrc": "../../live-examples/css-examples/css/animation.css",]
    ["jsExampleSrc": "../../live-examples/js-examples/array-find.js",]
    ["exampleCode": "live-examples/css-examples/border-top-color.html",]
    "fileName": "array-find.html",
    "type": "js"
},
```

* `baseTmpl` - The base template to use for this example.
* `cssExampleSrc` - The file location that will be used as the value for the `href` attribute of a `link` tag.
* `jsExampleSrc` - The file location that will be used as the value for the `src` attribute of a `script` tag.
* `exampleCode` - This is currently only used by the CSS examples, and points to the location of the relevant live example HTML file.
* `fileName` - This is the file name that will be used for the generated live example page.
* `type` - The type of example; currently the only available types are js (JavaScript) or css.

## Browser support baseline

The following is a list of browser/version combinations that are supported by the interactive editor. In browsers that do not meet the criteria, the editor degrades gracefully to displaying static examples.

* Firefox - Latest three release versions.
* Chrome - Latest three release versions.
* Opera - Latest two release versions.
* Safari - Latest two release versions.
* Internet Explorer - version 11.
* Edge - Latest release version.

## Contributing

If you're interested in contributing to this project, great! Please see the [CONTRIBUTING](CONTRIBUTING.md) document.

## Contributors

Thanks goes to these wonderful people ([emoji key](https://github.com/kentcdodds/all-contributors#emoji-key)):

<!-- ALL-CONTRIBUTORS-LIST:START - Do not remove or modify this section -->
<!-- prettier-ignore -->
| [<img src="https://avatars3.githubusercontent.com/u/10350960?s=460&v=4" width="100px;"/><br /><sub><b>Schalk Neethling</b></sub>](https://github.com/schalkneethling)<br />[💻](https://github.com/mdn/interactive-examples/commits?author=schalkneethling "Code") [📖](https://github.com/mdn/interactive-examples/commits?author=schalkneethling "Documentation") [⚠️](https://github.com/mdn/interactive-examples/commits?author=schalkneethling "Tests") | [<img src="https://avatars3.githubusercontent.com/u/208756?s=460&v=4" width="100px;"/><br /><sub><b>Mark Boas</b></sub>](https://github.com/maboa)<br />[💻](https://github.com/mdn/interactive-examples/commits?author=maboa "Code") [📖](https://github.com/mdn/interactive-examples/commits?author=maboa "Documentation") | [<img src="https://avatars3.githubusercontent.com/u/432915?s=460&v=4" width="100px;"/><br /><sub><b>William Bamberg</b></sub>](https://github.com/wbamberg)<br />[💻](https://github.com/mdn/interactive-examples/commits?author=wbamberg "Code") [📖](https://github.com/mdn/interactive-examples/commits?author=wbamberg "Documentation") | [<img src="https://avatars3.githubusercontent.com/u/854701?s=460&v=4" width="100px;"/><br /><sub><b>Stephanie Hobson</b></sub>](https://github.com/stephaniehobson)<br />[💻](https://github.com/mdn/interactive-examples/commits?author=stephaniehobson "Code") | [<img src="https://avatars3.githubusercontent.com/u/161718?s=460&v=4" width="100px;"/><br /><sub><b>Josh Mize</b></sub>](https://github.com/jgmize)<br />[💻](https://github.com/mdn/interactive-examples/commits?author=jgmize "Code") | [<img src="https://avatars3.githubusercontent.com/u/47647?s=460&v=4" width="100px;"/><br /><sub><b>Chris Mills</b></sub>](https://github.com/chrisdavidmills)<br />[📖](https://github.com/mdn/interactive-examples/commits?author=chrisdavidmills "Documentation") | [<img src="https://avatars3.githubusercontent.com/u/58244?s=460&v=4" width="100px;"/><br /><sub><b>Dave Parfitt</b></sub>](https://github.com/metadave)<br />[💻](https://github.com/mdn/interactive-examples/commits?author=metadave "Code") |
| :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| [<img src="https://avatars3.githubusercontent.com/u/13082030?s=460&v=4" width="100px;"/><br /><sub><b>Normal Human</b></sub>](https://github.com/normalhuman)<br />[📖](https://github.com/mdn/interactive-examples/commits?author=normalhuman "Documentation") | [<img src="https://avatars3.githubusercontent.com/u/1783036?s=460&v=4" width="100px;"/><br /><sub><b>Gal Pasternak</b></sub>](https://github.com/galman33)<br />[📖](https://github.com/mdn/interactive-examples/commits?author=galman33 "Documentation") | [<img src="https://avatars3.githubusercontent.com/u/2413436?s=460&v=4" width="100px;"/><br /><sub><b>SphinxKnight</b></sub>](https://github.com/SphinxKnight)<br />[💻](https://github.com/mdn/interactive-examples/commits?author=SphinxKnight "Code") | [<img src="https://avatars3.githubusercontent.com/u/33892472?s=460&v=4" width="100px;"/><br /><sub><b>Ayush Gupta</b></sub>](https://github.com/7ayushgupta)<br />[💻](https://github.com/mdn/interactive-examples/commits?author=7ayushgupta "Code") | [<img src="https://avatars2.githubusercontent.com/u/286017?s=460&v=4" width="100px;"/><br /><sub><b>John Whitlock</b></sub>](https://github.com/jwhitlock)<br />[💻](https://github.com/mdn/interactive-examples/commits?author=jwhitlock "Code") [🚇](#infra-jwhitlock "Infrastructure (Hosting, Build-Tools, etc)") |
<!-- ALL-CONTRIBUTORS-LIST:END -->

This project follows the [all-contributors](https://github.com/kentcdodds/all-contributors) specification. Contributions of any kind welcome!

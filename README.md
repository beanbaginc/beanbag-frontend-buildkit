# Beanbag Frontend Buildkit

This package depends on and installs a handful of tools used to build the CSS
and JavaScript used in [Beanbag](https://www.beanbaginc.com) products and
services (such as [Review Board](https://www.reviewboard.org) and
[RBCommons](https://rbcommons.com)).

It's also used for developers building custom code review features on the
Review Board Platform.

The contents of the buildkit are expected to change over time. We follow
semantic versioning, and will bump up the package's version appropriately as we
make changes.

## What's Included

### CSS Build Tools

* [LessCSS 4](https://lesscss.org/) (4.1 or higher), with:
    * [Auto-prefixer plugin](https://www.npmjs.com/package/@beanbag/less-plugin-autoprefix), for better cross-browser CSS compatibility.


### JavaScript Build Tools

* [Babel 7](https://babeljs.io/) (7.20 or higher), with:
    * [TypeScript support](https://www.npmjs.com/package/@babel/preset-typescript)
    * [dedent plugin](https://www.npmjs.com/package/babel-plugin-dedent) for
	  dedenting template literals.
    * [Django gettext plugin](https://www.npmjs.com/package/babel-plugin-django-gettext)
	  for conveniently localizing strings in projects using Django.

* [rollup.js 3](https://rollupjs.org/) (3.9 or higher), with:
    * [Babel plugin](https://www.npmjs.com/package/@rollup/plugin-babel), to
	  compile source files using Babel.
    * [node-resolve plugin](https://www.npmjs.com/package/@rollup/plugin-node-resolve),
	  to help locate imported modules within `node_modules`.

* [UglifyJS 3](https://www.npmjs.com/package/uglify-js) (3.16 or higher).


## Installation

To manually install this packages and its dependencies, run:

```
npm install --save-dev beanbag-frontend-buildkit
```

We also recommend installing [ESLint](https://eslint.org/) and our
[beanbag-eslint-plugin](https://www.npmjs.com/package/@beanbag/eslint-plugin):

```
npm install --save-dev eslint @beanbag/eslint-plugin
```

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

* [LessCSS](https://lesscss.org/), with:
    * [Auto-prefixer plugin](https://www.npmjs.com/package/@beanbag/less-plugin-autoprefix),
      for better cross-browser CSS compatibility.


### JavaScript Build Tools

* [Babel](https://babeljs.io/), with:
    * [TypeScript support](https://www.npmjs.com/package/@babel/preset-typescript)
    * [decorator proposals](https://www.npmjs.com/package/@babel/plugin-proposal-decorators]
      for experimental decorator support.
    * [dedent plugin](https://www.npmjs.com/package/babel-plugin-dedent) for
      dedenting template literals.
    * [Django gettext plugin](https://www.npmjs.com/package/babel-plugin-django-gettext)
      for conveniently localizing strings in projects using Django.

* [rollup.js](https://rollupjs.org/), with:
    * [Babel plugin](https://www.npmjs.com/package/@rollup/plugin-babel), to
      transpile modern JavaScript.
    * [dts plugin](https://www.npmjs.com/package/rollup-plugin-dts), bundle
      TypeScript `.d.ts` files.
    * [external-globals plugin](https://www.npmjs.com/package/rollup-plugin-external-globals),
      to rewrite imports from specific modules to use global JavaScript namespaces instead.
    * [node-resolve plugin](https://www.npmjs.com/package/@rollup/plugin-node-resolve),
      to help locate imported modules within `node_modules`.

* [Terser](https://terser.org/)


## Installation

To manually install this packages and its dependencies, run:

```
npm install --save-dev beanbag-frontend-buildkit
```


We also recommend using
[@beanbag/js-buildkit](https://www.npmjs.com/package/@beanbag/js-buildkit),
which specifies the specific versions of TypeScript and ESLint, and includes
our [ESLint plugin](https://www.npmjs.com/package/@beanbag/eslint-plugin).

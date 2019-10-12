[![Build Status](https://travis-ci.org/bostontrader/bookwerx-ui.svg?branch=react)](https://travis-ci.org/bostontrader/bookwerx-ui)
[![Coverage Status](https://coveralls.io/repos/github/bostontrader/bookwerx-ui/badge.svg?branch=react)](https://coveralls.io/github/bostontrader/bookwerx-ui?branch=react)
[![Known Vulnerabilities](https://snyk.io/test/github/bostontrader/bookwerx-ui/badge.svg)](https://snyk.io/test/github/bostontrader/bookwerx-ui)

[![MIT license](http://img.shields.io/badge/license-MIT-brightgreen.svg)](http://opensource.org/licenses/MIT)
[![Dependency Status](https://david-dm.org/bostontrader/bookwerx-ui.svg)](https://david-dm.org/bostontrader/bookwerx-ui)
[![devDependency Status](https://david-dm.org/bostontrader/bookwerx-ui/dev-status.svg)](https://david-dm.org/bostontrader/bookwerx-ui#info=devDependencies)

# Welcome to bookwerx-ui

## This repository is obsolete and no longer maintaned.  It has been succeeded by [bookwerx-ui-elm](https://github.com/bostontrader/bookwerx-ui-elm)

The purpose of **bookwerx-ui** is to provide an example user interface to the [bookwerx-core](https://github.com/bostontrader/bookwerx-core) bookkeeping engine.


## Getting Started

```sh
$ npm install
$ npm test
$ npm start
```

Note: Be sure to quote the glob pattern in npm commands or you may have unpleasant surprises re: which files and directories it finds.  In particularly, globstar (**) is a problem.


## Dependencies

**bookwerx-ui** uses React for the UI and routing and hence requires:

* react
* react-dom
* react-router-dom

**bookwerx-ui** also uses:

* bulma - For styling.
* react-select - Where the UI uses select controls, this is useful.

## devDependencies

**bookwerx-ui** uses webpack and the weback development server. We also use some twisted to hack to prevent CSS from getting transpiled.  That's a big does-not-compute so we don't want that.

* require-hacker
* webpack
* webpack-dev-server

**bookwerx-ui** uses ES2015 source code as well as a few additional fancy language features.  We have chosen babel for our transpiling needs. This gives rise to the need to use:

* babel-core
* babel-loader - Webpack needs this to connect to babel.
* babel-preset-es2015 - Need this generally for ES2015 syntax.
* babel-preset-react - Need this in order to use JSX syntax.

Because we load some css we need:

* css-loader
* style-loader

For testing we use Ava, Enzyme, and Nyc.  I recently had a problem with ajv being missing.  So I therefore needed to add it.  As per the enzyme docs, if we use React >=15.5 then I must also use react-test-renderer:

* ajv
* ava
* enzyme
* nyc
* react-test-renderer

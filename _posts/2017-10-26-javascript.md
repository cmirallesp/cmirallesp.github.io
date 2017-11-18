---
layout: post
title: Javascript howto
tags: javascript js node npm
---

<!-- vim-markdown-toc GFM -->

* [Node](#node)
	* [Installation](#installation)
* [packages](#packages)
* [Flow (javascript with types)](#flow-javascript-with-types)
	* [Installation](#installation-1)
	* [Usage](#usage)
	* [Configuring babel](#configuring-babel)
	* [Nvim configuration](#nvim-configuration)
* [Eslint](#eslint)
	* [Flowtype](#flowtype)
	* [Configuration (.eslint)](#configuration-eslint)
* [Test (Mocha and Chai)](#test-mocha-and-chai)
	* [Installation](#installation-2)

<!-- vim-markdown-toc -->

# Node

##Installation

If command `node` doesn't work you may want to install it.
Several options:
- from [https://nodejs.org/en/download/](https://nodejs.org/en/download/)
- `brew install node`

# packages

Node packages manager (npm) allows manage the packages to install at your system.
If you use -g param, package will be installed globally.

1. npm-freeze: it create a manifest file with all the modules installed in folder `node-modules`

# Flow (javascript with types)

## Installation

````bash
npm install --save-dev flow-bin
npm install --save-dev babel-preset-flow
```

## Usage

Add a "flow" script to your package.json:

```json
{
  "name": "my-flow-project",
  "version": "1.0.0",
  "devDependencies": {
    "flow-bin": "^0.41.0"
  },
  "scripts": {
    "flow": "flow"
  }
}
```

Now you can do `node run flow`

## Configuring babel

1. Via .babelrc

```json
{
  "presets": ["flow"]
}
```

2. Via command line `babel --presets flow script.js`

[https://flow.org/en/docs/](https://flow.org/en/docs/)

## Nvim configuration

[https://github.com/ryyppy/flow-vim-quickfix](https://github.com/ryyppy/flow-vim-quickfix)
[https://medium.com/@renatoagds/flow-vim-the-long-journey-497e020114e5](https://medium.com/@renatoagds/flow-vim-the-long-journey-497e020114e5)

# Eslint

```bash
npm install eslint --save-dev
npm install babel-eslint --save-dev
```
## Flowtype

```bash
npm install eslint-plugin-flowtype --save-dev
```

## Configuration (.eslint)

Configure to use [recommended rules](https://github.com/gajus/eslint-plugin-flowtype/blob/master/src/configs/recommended.json)

```json
{
  "parser": "babel-eslint",
  "plugins": [
    "flowtype"
  ],
	"extends": [
    "plugin:flowtype/recommended"
  ],
}
```

Or set your own rules
```json
{
  "parser": "babel-eslint",
  "plugins": [
    "flowtype"
  ],
  "rules": {
    "flowtype/boolean-style": [
      2,
      "boolean"
    ],
    "flowtype/define-flow-type": 1,
    "flowtype/delimiter-dangle": [
      2,
      "never"
    ],
    "flowtype/generic-spacing": [
      2,
      "never"
    ],
    "flowtype/no-primitive-constructor-types": 2,
    "flowtype/no-types-missing-file-annotation": 2,
    "flowtype/no-weak-types": 2,
    "flowtype/object-type-delimiter": [
      2,
      "comma"
    ],
    "flowtype/require-parameter-type": 2,
    "flowtype/require-return-type": [
      2,
      "always",
      {
        "annotateUndefined": "never"
      }
    ],
    "flowtype/require-valid-file-annotation": 2,
    "flowtype/semi": [
      2,
      "always"
    ],
    "flowtype/space-after-type-colon": [
      2,
      "always"
    ],
    "flowtype/space-before-generic-bracket": [
      2,
      "never"
    ],
    "flowtype/space-before-type-colon": [
      2,
      "never"
    ],
    "flowtype/type-id-match": [
      2,
      "^([A-Z][a-z0-9]+)+Type$"
    ],
    "flowtype/union-intersection-spacing": [
      2,
      "always"
    ],
    "flowtype/use-flow-type": 1,
    "flowtype/valid-syntax": 1
  },
  "settings": {
    "flowtype": {
      "onlyFilesWithFlowAnnotation": false
    }
  }
}
```



# Test (Mocha and Chai)

Mocha is a test framework while chai allows us to write specs as assert/should/expect

## Installation

`npm install --save-dev mocha chai` (or globally `npm install --global mocha chai`)




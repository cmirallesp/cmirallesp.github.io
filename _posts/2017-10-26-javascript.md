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
	* [Usage with babel](#usage-with-babel)

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
## Usage with babel

1. Via .babelrc

```json
{
  "presets": ["flow"]
}
```

2. Via command line `babel --presets flow script.js`

[https://flow.org/en/docs/](https://flow.org/en/docs/)

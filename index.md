---
layout: page
title:
permalink: /
---

TangoJS - *a complete solution for creating web-based
[TANGO Controls](http://www.tango-controls.org/) client applications*.

![](_assets/logo_tangocontrols.png)

# Demo

[Synoptic panel](#) built with TangoJS.

> For Firefox, enable `dom.webcomponents.enabled` and `layout.css.grid.enabled`.

> For Chrome, enable *experimental web platform features*.

# Stack
TangoJS modular architecture consists of:

* [tangojs-web-components](https://github.com/tangojs/tangojs-web-components) -
  widget toolkit built with Web Components,
* [tangojs-core](https://github.com/tangojs/tangojs-core) -
  core API generated from TANGO IDL,
* pluggable backends:
  * [tangojs-connector-local](
    https://github.com/tangojs/tangojs-connector-local) -
    in-memory mock,
  * [tangojs-connector-mtango](
    https://github.com/tangojs/tangojs-connector-mtango) -
    [mTango](https://bitbucket.org/hzgwpn/mtango/wiki/Home) integration.

# Examples

Simple setup:

```html
<script src="node_modules/tangojs-core/lib/tangojs-core.js"></script>
<!-- more dependencies -->

<link rel="import" href="tangojs-web-components/tangojs-line-edit.html">
<!-- desired widgets -->
```

Declarative syntax:

```html
<tangojs-state-led
  model="tangojs/test/dev1"
  poll-period="1000"
  show-name
  show-led>
</tangojs-state-led>
```

Javascript API:

```javascript
const proxy = new tangojs.core.api.AttributeProxy('tangojs/test/1/number_scalar')
const input = new tangojs.struct.core.api.AttributeValue({ value: 32 })
proxy.write(input)
```

# Installation

All the components are available in the npm Registry.

```
$ npm install --save tangojs
$ npm install --save tangojs-connector-local
$ npm install --save tangojs-web-components
```

# Getting started
Best way to start with TangoJS is to check the [tangojs-webapp-template](
https://github.com/tangojs/tangojs-webapp-template) repo.

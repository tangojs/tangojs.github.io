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

> Enable `dom.webcomponents.enabled` and `layout.css.grid.enabled` for Firefox
> (45+) and `experimental web platform features` for Chrome (50+).

# Stack
TangoJS modular architecture consists of:

* [tangojs-web-components](https://github.com/mliszcz/tangojs-web-components) -
  widget toolkit built with Web Components,
* [tangojs-core](https://github.com/mliszcz/tangojs) -
  core API generated from TANGO IDL,
* pluggable backends:
  * [tangojs-connector-local](
    https://github.com/mliszcz/tangojs-connector-local) -
    in-memory mock.

# Examples

Simple setup:

```html
<script src="node_modules/tangojs/lib/tangojs.js"></script>
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
const proxy = new tangojs.proxy.AttributeProxy('tangojs/test/1/number_scalar')
const input = new tangojs.struct.AttributeValue({ value: 32 })
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
Best way to start with TangoJS is to check the
[getting-started repo](https://github.com/tangojs/tangojs-getting-started).

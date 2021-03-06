# smooth-page-scroll

Easy replacement for in-page hash-link scrolling.

> Note:
> This lib requires `window.{request,cancel}AnimationFrame`, `history.{push,replace}State`.

## Demo

See https://leader22.github.io/smooth-page-scroll

## How to use

by `npm`.

```
npm i smooth-page-scroll --save
```

by `script` tag.

```html
<script src="./path/to/smooth-page-scroll.min.js"></script>
```

then,

```js
// for CommonJS
var SmoothPageScroll = require('smooth-page-scroll');

SmoothPageScroll.install();
```

finally,

```html
<a href="#dest">Go!</a>

<div id="dest">
  Destination
</div>
```

## APIs

### install()

Enable smooth page scroll.

### uninstall()

Disable smooth page scroll.

### update()

Re install smooth page scroll.
Use this after DOM manipulation(like appending new DOM elements).

## Options

You can pass options as `install(options)`.

props | type | default | desc
:---- | :--: | :------ | :---
gapX | number | `40` | Gap for destination posX.
gapY | number | `40` | Gap for destination posY.
duration | number | `500` | Duration for scrolling.
easing | func | `t => t*(2-t)` | Easing function for scrolling.
useHashAsHistory | bool | `true` | If true, pushState on hash has changed.

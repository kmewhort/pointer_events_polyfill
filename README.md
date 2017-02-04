# Pointer Events Polyfill

Pointer Events Polyfill is a short javascript library which adds support for the style attribute "pointer-events: none" to browsers without this feature (namely, MS IE).

## Installation

Include any reasonable recent version of **jQuery** and **pointer\_events\_polyfill.js**.

## Basic usage:

```js
$(document).ready(function(){
  PointerEventsPolyfill.initialize({});
});
```

That's it! Any "pointer-events: none" attributes will now work seamlessly in IE.

## Options

You can also pass any of the following options into the *initialize* call:

* **selector**: CSS selector (default: \*). You may wish to narrow this from '*' (all elements) in order to increase performance.
* **mouseEvents**: Array of JS mouse events (default: ['click','dblclick','mousedown','mouseup']). Note that this default excludes a few mouse events for performance reasons, but you can add them back in.
* **usePolyfillIf**: Function with boolean return value (default: simple check for IE<11). Return *true* to apply Pointer Events Polyfill. You can specify your own browser-support test function here (for example, you may wish to use feature detection with Modernizr instead of the default IE check).

## License

(c) 2013, Kent Mewhort, licensed under BSD. See LICENSE.txt for details.


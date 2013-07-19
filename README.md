# Pointer Events Polyfill

Pointer Events Polyfill is a short javascript library to add support for the style attribute "pointer-events: none" to browsers without this feature (namely, MS IE).

## Installation

Include any reasonable recent version of **jQuery** and **pointer_events_polyfill.js**.

## Usage

Basic usage:

    $(document).ready(function(){
      PointerEventsPolyfill.initialize({});
    });

That's it! Any "pointer-events: none" attributes will now work seamlessly in IE.

## Options

You can also pass any of the following options into the *initialize* call:
* **selector**: CSS selector [default: '*']. You may wish to narrow this from '*' (all elements) in order to increase performance.
* **mouseEvents** Array of JS mouse events [default: ['click','dblclick','mousedown','mouseup']]. Note that the default excludes a few for performance reasons, but you can add them back in.
* **usePolyfillIf** function with a return of true to initialize Pointer Events Polyfill [default: simply check for IE<11]. You can specify your own browser-support testing function here (for example, you may wish to use feature detection with Modernizr instead of the default IE check).

## License

(c) 2013, Kent Mewhort, licensed under BSD. See LICENSE.txt for details.


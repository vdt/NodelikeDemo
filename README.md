NodelikeDemo
============

Nodelike is a weekend hack to implement a roughly Node.JS-compatible interface using JavaScriptCore.framework on iOS 7 and OS X Mavericks.

This is currently in a very incomplete state, and not viable for serious use.
It could, however, become usable over the following weeks.

The goals
---------
- to be _drop-in compatible_ with the current nodejs master
- to be _very lightweight_
- to _reuse javascript code from node_ (/lib)
- to provide the _most minimal binding_ that is possible
- NOT to archieve Node.js performance (this is meant as a client-side, not a server-side application)
- NOT to be backwards-compatible (nodejs cutting edge and newest iOS/OS X required)
- NOT to integrate libuv

How to use the demo app
-----------------------

You can enter Javascript code into the TextView and execute that via a tap on the `Execute` button.
After each execution, the result of the global variable `_` is pasted into the TextView.
So to get the result of an addition, do: `_ = 1 + 3.2`. To print a variable: `_ = JSON.stringify(process.argv)`.

Have fun!

What's working right now
------------------------

- `process`: `.cwd()`, `.chdir()`, `.argv`, `.env`, `.exit()`, `.nextTick()`
- `require()` for native modules
- `util`
- `url`
- `events`
- `path`
- `stream`
- `querystring`
- `punycode`
- `assert`

# Node module @built-in/readable-stream

This is a shim Node.js module that simply returns the result of calling `require('node:stream')`.

It is intended to be used with the `package.json` [`overrides`](https://docs.npmjs.com/cli/v9/configuring-npm/package-json#overrides) clause, forcing dependencies that require the [`readable-stream`](https://www.npmjs.com/package/readable-stream) module to use the built-in Node.js implementation from the `stream` module.

## Installation

While this is published as a regular npm package, it is _not_ intended to be directly installed, but rather indirectly through the dependency `overrides` clause. To use, edit your `package.json` to contain the following:

```json
{
    "overrides": {
        "readable-stream": "npm:@built-in/readable-stream@1"
    }
}
```

Now run `npm install --save` to update update your installed dependencies. This replaces all instances of `readable-stream` from `node_modules` with this module.

## License

This is free and unencumbered software released into the public domain.

Anyone is free to copy, modify, publish, use, compile, sell, or
distribute this software, either in source code form or as a compiled
binary, for any purpose, commercial or non-commercial, and by any
means.

In jurisdictions that recognize copyright laws, the author or authors
of this software dedicate any and all copyright interest in the
software to the public domain. We make this dedication for the benefit
of the public at large and to the detriment of our heirs and
successors. We intend this dedication to be an overt act of
relinquishment in perpetuity of all present and future rights to this
software under copyright law.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND,
EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF
MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.
IN NO EVENT SHALL THE AUTHORS BE LIABLE FOR ANY CLAIM, DAMAGES OR
OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE,
ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR
OTHER DEALINGS IN THE SOFTWARE.

For more information, please refer to <http://unlicense.org/>

# Snapshot report for `test/test.js`

The actual snapshot is saved in `test.js.snap`.

Generated by [AVA](https://avajs.dev).

## inject cjs shim for esm output

> Snapshot 1

    `␊
    // -- Shims --␊
    import cjsUrl from 'url';␊
    import cjsPath from 'path';␊
    import cjsModule from 'module';␊
    const __filename = cjsUrl.fileURLToPath(import.meta.url);␊
    const __dirname = cjsPath.dirname(__filename);␊
    const require = cjsModule.createRequire(import.meta.url);␊
    const child = require('child');␊
    ␊
    export { child };␊
    `

## inject cjs shim for esm output with sourcemap

> Snapshot 1

    `␊
    // -- Shims --␊
    import cjsUrl from 'url';␊
    import cjsPath from 'path';␊
    import cjsModule from 'module';␊
    const __filename = cjsUrl.fileURLToPath(import.meta.url);␊
    const __dirname = cjsPath.dirname(__filename);␊
    const require = cjsModule.createRequire(import.meta.url);␊
    const child = require('child');␊
    ␊
    export { child };␊
    //# sourceMappingURL=cjs.js.map␊
    `

## not inject cjs shim for cjs output

> Snapshot 1

    `'use strict';␊
    ␊
    const child = require('child');␊
    ␊
    exports.child = child;␊
    `

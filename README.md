# react-flow node issue

## Update: Issue Fixed

The issue was solved in `v9.0.3`.

<https://github.com/wbkd/react-flow/issues/934#issuecomment-785916788`>

## Steps

- `npm install`
- `npm test`

## Versions

```shell
node -v
v14.9.0
```

and see `package.json`

## Issue

```shell
npm test | pbcopy
internal/modules/cjs/loader.js:1092
      throw new ERR_REQUIRE_ESM(filename, parentPath, packageJsonPath);
      ^

Error [ERR_REQUIRE_ESM]: Must use import to load ES Module: /home/user/dev/repository/react-flow-node-issue-example/node_modules/@babel/runtime/helpers/esm/extends.js
require() of ES modules is not supported.
require() of /home/user/dev/repository/react-flow-node-issue-example/node_modules/@babel/runtime/helpers/esm/extends.js from /home/user/dev/repository/react-flow-node-issue-example/node_modules/react-flow-renderer/dist/ReactFlow.js is an ES module file as it is a .js file whose nearest parent package.json contains "type": "module" which defines all .js files in that package scope as ES modules.
Instead rename extends.js to end in .cjs, change the requiring code to use import(), or remove "type": "module" from /home/user/dev/repository/react-flow-node-issue-example/node_modules/@babel/runtime/helpers/esm/package.json.

    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:13)
    at Module.load (internal/modules/cjs/loader.js:940:32)
    at Function.Module._load (internal/modules/cjs/loader.js:781:14)
    at Module.require (internal/modules/cjs/loader.js:964:19)
    at require (internal/modules/cjs/helpers.js:88:18)
    at Object.<anonymous> (/home/user/dev/repository/react-flow-node-issue-example/node_modules/react-flow-renderer/dist/ReactFlow.js:6:1)
    at Module._compile (internal/modules/cjs/loader.js:1075:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1096:10)
    at Module.load (internal/modules/cjs/loader.js:940:32)
    at Function.Module._load (internal/modules/cjs/loader.js:781:14) {
  code: 'ERR_REQUIRE_ESM'
}
npm ERR! Test failed.  See above for more details.
```

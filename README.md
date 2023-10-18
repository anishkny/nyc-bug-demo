# NYC Bug Demo

## Repro

```bash
$ npm install
$ npm start

> start
> nyc node index.js

Server running at http://127.0.0.1:3000/
^Cnode:internal/validators:95
      throw new ERR_INVALID_ARG_TYPE(name, 'number', value);
      ^

TypeError [ERR_INVALID_ARG_TYPE]: The "code" argument must be of type number. Received type string ('128SIGINT')
    at process.set [as exitCode] (node:internal/bootstrap/node:123:9)
    at ChildProcess.<anonymous> (/Users/anish/workspace/nyc-bug-demo/node_modules/foreground-child/index.js:63:22)
    at ChildProcess.emit (node:events:514:28)
    at maybeClose (node:internal/child_process:1105:16)
    at ChildProcess._handle.onexit (node:internal/child_process:305:5) {
  code: 'ERR_INVALID_ARG_TYPE'
}

Node.js v20.8.1
```

Generated with [vike.dev/new](https://vike.dev/new) ([version 429](https://www.npmjs.com/package/create-vike/v/0.0.429)) using this command:

```sh
pnpm create vike@latest --react --tailwindcss --hono --eslint --prettier
```

Then, added a commit integrating vike-server.

Now, when running `pnpm build` on **Windows 11** and node 22, we encounter following error:

```bash
PS C:\Users\SANJAY\Projects\vike-server-demo> pnpm build

> @ build C:\Users\SANJAY\Projects\vike-server-demo
> vike build

Error during build:
Error: Build failed with 1 error:
node_modules/.pnpm/esbuild@0.24.2/node_modules/esbuild/lib/main.js:1226:21: ERROR: [plugin: vike-esbuild] [vike@0.4.228][Bug] You stumbled upon a Vike bug. Go to https://github.com/vikejs/vike/issues/new?template=bug.yml and copy-paste this error. A maintainer will fix the bug (usually within 24 hours). Debug info (for Vike maintainers; you can ignore this): Not a posix path: C:\Users\SANJAY\Projects\vike-server-demo\pages
    at failureErrorWithLog (C:\Users\SANJAY\Projects\vike-server-demo\node_modules\.pnpm\esbuild@0.24.2\node_modules\esbuild\lib\main.js:1476:15)
    at C:\Users\SANJAY\Projects\vike-server-demo\node_modules\.pnpm\esbuild@0.24.2\node_modules\esbuild\lib\main.js:945:25
    at runOnEndCallbacks (C:\Users\SANJAY\Projects\vike-server-demo\node_modules\.pnpm\esbuild@0.24.2\node_modules\esbuild\lib\main.js:1316:45)
    at buildResponseToResult (C:\Users\SANJAY\Projects\vike-server-demo\node_modules\.pnpm\esbuild@0.24.2\node_modules\esbuild\lib\main.js:943:7)
    at C:\Users\SANJAY\Projects\vike-server-demo\node_modules\.pnpm\esbuild@0.24.2\node_modules\esbuild\lib\main.js:970:16
    at responseCallbacks.<computed> (C:\Users\SANJAY\Projects\vike-server-demo\node_modules\.pnpm\esbuild@0.24.2\node_modules\esbuild\lib\main.js:622:9)
    at handleIncomingPacket (C:\Users\SANJAY\Projects\vike-server-demo\node_modules\.pnpm\esbuild@0.24.2\node_modules\esbuild\lib\main.js:677:12)
    at Socket.readFromStdout (C:\Users\SANJAY\Projects\vike-server-demo\node_modules\.pnpm\esbuild@0.24.2\node_modules\esbuild\lib\main.js:600:7)
    at Socket.emit (node:events:524:28)
    at addChunk (node:internal/streams/readable:561:12) {
  errors: [Getter/Setter],
  warnings: [Getter/Setter],
  _formatted: '\x1B[31mFailed to transpile\x1B[39m \x1B[1m\x1B[31m/pages/+config.ts\x1B[39m\x1B[22m \x1B[31mbecause:\x1B[39m\n' +
    '\x1B[31mX \x1B[41;31m[\x1B[41;97mERROR\x1B[41;31m]\x1B[0m \x1B[1m[vike@0.4.228]\x1B[1m\x1B[31m[Bug]\x1B[39m\x1B[22m You stumbled upon a Vike bug. Go to \x1B[4mhttps://github.com/vikejs/vike/issues/new?template=bug.yml\x1B[24m and copy-paste this error. A maintainer will fix the bug (usually within 24 hours). \x1B[2mDebug info (for Vike maintainers; you can ignore this): Not a posix path: C:\\Users\\SANJAY\\Projects\\vike-server-demo\\pages\x1B[22m\x1B[0m \x1B[1m\x1B[35m[plugin vike-esbuild]\x1B[0m\n' +
    '\n' +
    '    node_modules/.pnpm/esbuild@0.24.2/node_modules/esbuild/lib/main.js:1226:21:\n' +
    '\x1B[37m      1226 │         let result = \x1B[32m\x1B[37mawait callback({\n' +
    '           ╵                      \x1B[32m^\x1B[0m\n' +
    '\n' +
    '    at assertPosixPath (file:///C:/Users/SANJAY/Projects/vike-server-demo/node_modules/.pnpm/vike@0.4.228_react-streamin_e8a25d628dbd509dfff4a0da8d6f041e/node_modules/vike/dist/esm/utils/path.js:43:5)\n' +
    '    at requireResolve_ (file:///C:/Users/SANJAY/Projects/vike-server-demo/node_modules/.pnpm/vike@0.4.228_react-streamin_e8a25d628dbd509dfff4a0da8d6f041e/node_modules/vike/dist/esm/utils/requireResolve.js:18:5)\n' +
    '    at requireResolveOptional (file:///C:/Users/SANJAY/Projects/vike-server-demo/node_modules/.pnpm/vike@0.4.228_react-streamin_e8a25d628dbd509dfff4a0da8d6f041e/node_modules/vike/dist/esm/utils/requireResolve.js:41:17)\n' +
    '    at file:///C:/Users/SANJAY/Projects/vike-server-demo/node_modules/.pnpm/vike@0.4.228_react-streamin_e8a25d628dbd509dfff4a0da8d6f041e/node_modules/vike/dist/esm/node/plugin/plugins/importUserCode/v1-design/getVikeConfig/transpileAndExecuteFile.js:124:50\n' +
    '    at requestCallbacks.on-resolve (C:\\Users\\SANJAY\\Projects\\vike-server-demo\\node_modules\\.pnpm\\esbuild@0.24.2\\node_modules\\esbuild\\lib\\main.js:1226:22)\n' +
    '    at handleRequest (C:\\Users\\SANJAY\\Projects\\vike-server-demo\\node_modules\\.pnpm\\esbuild@0.24.2\\node_modules\\esbuild\\lib\\main.js:647:11)\n' +
    '\n' +
    '  This error came from the "onResolve" callback registered here:\n' +
    '\n' +
    '    node_modules/.pnpm/esbuild@0.24.2/node_modules/esbuild/lib/main.js:1150:20:\n' +
    '\x1B[37m      1150 │       let promise = \x1B[32m\x1B[37msetup({\n' +
    '           ╵                     \x1B[32m^\x1B[0m\n' +
    '\n' +
    '    at setup (file:///C:/Users/SANJAY/Projects/vike-server-demo/node_modules/.pnpm/vike@0.4.228_react-streamin_e8a25d628dbd509dfff4a0da8d6f041e/node_modules/vike/dist/esm/node/plugin/plugins/importUserCode/v1-design/getVikeConfig/transpileAndExecuteFile.js:106:23)\n' +
    '    at handlePlugins (C:\\Users\\SANJAY\\Projects\\vike-server-demo\\node_modules\\.pnpm\\esbuild@0.24.2\\node_modules\\esbuild\\lib\\main.js:1150:21)\n' +
    '    at buildOrContextImpl (C:\\Users\\SANJAY\\Projects\\vike-server-demo\\node_modules\\.pnpm\\esbuild@0.24.2\\node_modules\\esbuild\\lib\\main.js:873:5)\n' +
    '    at Object.buildOrContext (C:\\Users\\SANJAY\\Projects\\vike-server-demo\\node_modules\\.pnpm\\esbuild@0.24.2\\node_modules\\esbuild\\lib\\main.js:699:5)\n' +
    '    at C:\\Users\\SANJAY\\Projects\\vike-server-demo\\node_modules\\.pnpm\\esbuild@0.24.2\\node_modules\\esbuild\\lib\\main.js:2029:15\n' +
    '    at new Promise (<anonymous>)\n' +
    '    at Object.build (C:\\Users\\SANJAY\\Projects\\vike-server-demo\\node_modules\\.pnpm\\esbuild@0.24.2\\node_modules\\esbuild\\lib\\main.js:2028:25)\n' +
    '    at build (C:\\Users\\SANJAY\\Projects\\vike-server-demo\\node_modules\\.pnpm\\esbuild@0.24.2\\node_modules\\esbuild\\lib\\main.js:1879:51)\n' +
    '    at transpileWithEsbuild (file:///C:/Users/SANJAY/Projects/vike-server-demo/node_modules/.pnpm/vike@0.4.228_react-streamin_e8a25d628dbd509dfff4a0da8d6f041e/node_modules/vike/dist/esm/node/plugin/plugins/importUserCode/v1-design/getVikeConfig/transpileAndExecuteFile.js:254:24)\n' +
    '\n' +
    '  The plugin "vike-esbuild" was triggered by this import\n' +
    '\n' +
    '    pages/+config.ts:4:23:\n' +
    '\x1B[37m      4 │ import vikeServer from \x1B[32m"vike-server/config"\x1B[37m;\n' +
    '        ╵                        \x1B[32m~~~~~~~~~~~~~~~~~~~~\x1B[0m'
}
 ELIFECYCLE  Command failed with exit code 1.
```

# Environment

- Windows 11
- Node 22


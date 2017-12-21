Steps:

```
npm install
lerna bootstrap

cd packages/example
eslint index.js

cd packages/scoped-example
eslint index.js
```



Output:

```
➜  example git:(master) ✗ eslint index.js
Cannot find module 'eslint-config-example'
Referenced from: /Users/chris/github/eslint-issue-9746/packages/example/.eslintrc.js
Error: Cannot find module 'eslint-config-example'
Referenced from: /Users/chris/github/eslint-issue-9746/packages/example/.eslintrc.js
    at ModuleResolver.resolve (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/util/module-resolver.js:74:19)
    at resolve (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/config/config-file.js:471:25)
    at load (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/config/config-file.js:542:26)
    at configExtends.reduceRight (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/config/config-file.js:421:36)
    at Array.reduceRight (<anonymous>)
    at applyExtends (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/config/config-file.js:403:28)
    at loadFromDisk (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/config/config-file.js:514:22)
    at Object.load (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/config/config-file.js:550:20)
    at Config.getLocalConfigHierarchy (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/config.js:228:44)
    at Config.getConfigHierarchy (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/config.js:180:43)


➜  scoped-example git:(master) ✗ eslint index.js
Cannot find module '@chrisblossom/eslint-config'
Referenced from: /Users/chris/github/eslint-issue-9746/packages/scoped-example/.eslintrc.js
Error: Cannot find module '@chrisblossom/eslint-config'
Referenced from: /Users/chris/github/eslint-issue-9746/packages/scoped-example/.eslintrc.js
    at ModuleResolver.resolve (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/util/module-resolver.js:74:19)
    at resolve (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/config/config-file.js:471:25)
    at load (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/config/config-file.js:542:26)
    at configExtends.reduceRight (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/config/config-file.js:421:36)
    at Array.reduceRight (<anonymous>)
    at applyExtends (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/config/config-file.js:403:28)
    at loadFromDisk (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/config/config-file.js:514:22)
    at Object.load (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/config/config-file.js:550:20)
    at Config.getLocalConfigHierarchy (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/config.js:228:44)
    at Config.getConfigHierarchy (/Users/chris/github/eslint-issue-9746/node_modules/eslint/lib/config.js:180:43)
```


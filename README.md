# 33755

## Current behavior

renovate fails with

```

DEBUG: Preparing files for committing to branch renovate/golang.org-x-net-0.x (repository=dominikholler/symlinkdependency, branch=renovate/golang.org-x-net-0.x)
DEBUG: Setting git author name: Dominik Holler (repository=dominikholler/symlinkdependency, branch=renovate/golang.org-x-net-0.x)
DEBUG: Setting git author email: github@hollyhome.ath.cx (repository=dominikholler/symlinkdependency, branch=renovate/golang.org-x-net-0.x)
DEBUG: Unknown error committing files (repository=dominikholler/symlinkdependency, branch=renovate/golang.org-x-net-0.x)
       "err": {
         "task": {
           "commands": ["add", "vendor/golang.org/x/net/LICENSE"],
           "format": "utf-8",
           "parser": "[function]"
         },
         "message": "fatal: pathspec 'vendor/golang.org/x/net/LICENSE' is beyond a symbolic link\n",
         "stack": "Error: fatal: pathspec 'vendor/golang.org/x/net/LICENSE' is beyond a symbolic link\n\n    at Object.action (/usr/local/renovate/node_modules/.pnpm/simple-git@3.27.0/node_modules/simple-git/src/lib/plugins/error-detection.plugin.ts:42:29)\n    at PluginStore.exec (/usr/local/renovate/node_modules/.pnpm/simple-git@3.27.0/node_modules/simple-git/src/lib/plugins/plugin-store.ts:54:29)\n    at /usr/local/renovate/node_modules/.pnpm/simple-git@3.27.0/node_modules/simple-git/src/lib/runners/git-executor-chain.ts:124:42\n    at new Promise (<anonymous>)\n    at GitExecutorChain.handleTaskData (/usr/local/renovate/node_modules/.pnpm/simple-git@3.27.0/node_modules/simple-git/src/lib/runners/git-executor-chain.ts:121:14)\n    at GitExecutorChain.<anonymous> (/usr/local/renovate/node_modules/.pnpm/simple-git@3.27.0/node_modules/simple-git/src/lib/runners/git-executor-chain.ts:97:40)\n    at Generator.next (<anonymous>)\n    at fulfilled (/usr/local/renovate/node_modules/.pnpm/simple-git@3.27.0/node_modules/simple-git/dist/cjs/index.js:52:24)\n    at processTicksAndRejections (node:internal/process/task_queues:105:5)"
       }
 WARN: Error updating branch (repository=dominikholler/symlinkdependency, branch=renovate/golang.org-x-net-0.x)
       "err": {
         "task": {
           "commands": ["add", "vendor/golang.org/x/net/LICENSE"],
           "format": "utf-8",
           "parser": "[function]"
         },
         "message": "fatal: pathspec 'vendor/golang.org/x/net/LICENSE' is beyond a symbolic link\n",
         "stack": "Error: fatal: pathspec 'vendor/golang.org/x/net/LICENSE' is beyond a symbolic link\n\n    at Object.action (/usr/local/renovate/node_modules/.pnpm/simple-git@3.27.0/node_modules/simple-git/src/lib/plugins/error-detection.plugin.ts:42:29)\n    at PluginStore.exec (/usr/local/renovate/node_modules/.pnpm/simple-git@3.27.0/node_modules/simple-git/src/lib/plugins/plugin-store.ts:54:29)\n    at /usr/local/renovate/node_modules/.pnpm/simple-git@3.27.0/node_modules/simple-git/src/lib/runners/git-executor-chain.ts:124:42\n    at new Promise (<anonymous>)\n    at GitExecutorChain.handleTaskData (/usr/local/renovate/node_modules/.pnpm/simple-git@3.27.0/node_modules/simple-git/src/lib/runners/git-executor-chain.ts:121:14)\n    at GitExecutorChain.<anonymous> (/usr/local/renovate/node_modules/.pnpm/simple-git@3.27.0/node_modules/simple-git/src/lib/runners/git-executor-chain.ts:97:40)\n    at Generator.next (<anonymous>)\n    at fulfilled (/usr/local/renovate/node_modules/.pnpm/simple-git@3.27.0/node_modules/simple-git/dist/cjs/index.js:52:24)\n    at processTicksAndRejections (node:internal/process/task_queues:105:5)"
       }

```


## Expected behavior

renovate is able to update the dependency, even if symlinked.


## Link to the Renovate issue or Discussion

https://github.com/renovatebot/renovate/discussions/33755

```bash
git clone git@github.com:brillout/urql-vite3
cd urql-vite3/
pnpm install
pnpm run prod
```

As single line:

```bash
git clone git@github.com:brillout/urql-vite3 && cd urql-vite3/ && pnpm install && pnpm run prod
```

Go to [http://localhost:3000](http://localhost:3000) and observe following error:

```
file:///home/romuuu/tmp/urql/dist/server/assets/index.page.2bb793a4.js:1
import { gql, useQuery } from "urql";
         ^^^
SyntaxError: Named export 'gql' not found. The requested module 'urql' is a CommonJS module, which may not support all module.exports as named exports.
CommonJS modules can always be imported via the default export, for example using:

import pkg from 'urql';
const { gql, useQuery } = pkg;

    at ModuleJob._instantiate (node:internal/modules/esm/module_job:128:21)
    at async ModuleJob.run (node:internal/modules/esm/module_job:194:5)
    at async Promise.all (index 0)
    at async ESMLoader.import (node:internal/modules/esm/loader:409:24)
    at async Object.pageFile.loadFile (/home/romuuu/tmp/urql/node_modules/.pnpm/vite-plugin-ssr@0.4.0-beta.34_vite@3.0.0-alpha.9/node_modules/vite-plugin-ssr/dist/cjs/shared/getPageFiles/parseGlobResults.js:25:40)
    at async Promise.all (index 0)
    at async loadPageFilesServerSide (/home/romuuu/tmp/urql/node_modules/.pnpm/vite-plugin-ssr@0.4.0-beta.34_vite@3.0.0-alpha.9/node_modules/vite-plugin-ssr/dist/cjs/shared/getPageFiles/analyzePageServerSide/loadPageFilesServerSide.js:8:5)
    at async Promise.all (index 0)
    at async loadPageFilesServer (/home/romuuu/tmp/urql/node_modules/.pnpm/vite-plugin-ssr@0.4.0-beta.34_vite@3.0.0-alpha.9/node_modules/vite-plugin-ssr/dist/cjs/node/renderPage.js:373:69)
    at async renderPage_ (/home/romuuu/tmp/urql/node_modules/.pnpm/vite-plugin-ssr@0.4.0-beta.34_vite@3.0.0-alpha.9/node_modules/vite-plugin-ssr/dist/cjs/node/renderPage.js:87:23)
```

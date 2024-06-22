# next-auth-cookie-err-reproduction

This repo is a reproduction of a bug in NextAuth.js where the cookie import fails with the following error:

```
Failed to compile.

./node_modules/@auth/core/lib/utils/web.js
Attempted import error: 'parse' is not exported from 'cookie' (imported as 'parseCookie').

Import trace for requested module:
./node_modules/@auth/core/lib/utils/web.js
./node_modules/@auth/core/index.js
./node_modules/next-auth/index.js
./src/auth.ts
./src/app/api/[...nextauth]/route.ts

./node_modules/@auth/core/lib/utils/web.js
Attempted import error: 'serialize' is not exported from 'cookie' (imported as 'serialize').

Import trace for requested module:
./node_modules/@auth/core/lib/utils/web.js
./node_modules/@auth/core/index.js
./node_modules/next-auth/index.js
./src/auth.ts
./src/app/api/[...nextauth]/route.ts


> Build failed because of webpack errors
```

To reproduce:

- Clone this repo
- Run `npm install`
- Run `npm run build`

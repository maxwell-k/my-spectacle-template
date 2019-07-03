# My spectacle template

## Quick start

```sh
npx yarn install &&
patch node_modules/spectacle-renderer/lib/index.js networkidle2.patch
```

- Start a development server at <http://localhost:3000/>: `npm start`
- Build & serve production assets at <http://localhost:3000/>: `npm run deploy`
- Create `./presentation.pdf` from <http://localhost:3000/>: `npm run export`

## Operating system

This repository has been tested under Alpine Linux Edge. It should also work
under version 3.10.

```
$ apk list chromium
chromium-73.0.3683.103-r0 x86_64 {chromium} (BSD) [installed]
```

## Patch

`networkidle2.patch` was created with:

```sh
diff -Naur a/node_modules/spectacle-renderer/lib/index.js b/node_modules/spectacle-renderer/lib/index.js > networkidle2.patch
```

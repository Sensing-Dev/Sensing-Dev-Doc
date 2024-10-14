## Install Docusaurus

```
npm install --global docusaurus-init
npm install
```

## Preview

For defalut language (English),

```
npm run start
```

For another languages (e.g. Japanese)

```
npm run start -- --locale ja
```

## Build

```
npm build
```

## Static build for local

```
npm run build && npm run local-postbuild
```

This runs the local-postbuild to replace the absolute path to relative path

## New Release

When we have the latest release, update `static\version_const\latest.js`.

## Versioning

1. `npm run docusaurus docs:version vXX.YY` to create a new version.

2. Run `python3 version_update.py vXX.YY` to replace all js file path

4. Clean up `docs\this_version\api-change.mdx` (en) and `i18n\ja\docusaurus-plugin-content-docs\current\this_version\api-change.mdx` (ja) to reset the API update.

5. Remove the API update admonition from tutorials.

Note that you don't have to update Windows setup guilde to remove right-click instruction. It is automatically updated by step 3. See the detail in `static\msi_instruction_if_latest.js`
The errors I get:

```
TypeScript error: /.../tsify-module-system/ts/main.ts(2,30): Error TS2307: Cannot find module '@popperjs/core'.
TypeScript error: /.../tsify-module-system/ts/main.ts(3,23): Error TS2307: Cannot find module 'wpapi'.
TypeScript error: /.../tsify-module-system/ts/player.ts(1,30): Error TS2307: Cannot find module 'howler'.
TypeScript error: /.../tsify-module-system/ts/player.ts(5,27): Error TS2339: Property 'getBrowserLanguage' does not exist on type 'typeof Utils'.
```

# Update 1

With the latest changes, I get these errors in the terminal:

```
Error: Parsing file /.../tsify-module-system/node_modules/@popperjs/core/dist/esm/index.js: 'import' and 'export' may appear only with 'sourceType: module' (1:0)
```

The output changes according to the module system in use. I do not know which one works with my modules. Besides, I am not sure if watchify bundles all I need into the bundle.js file. It seems to not take in consideration the used modules, and I hope that this is just because the usages are dead code.

# Update 2

The output of `./watch.sh` is [here](https://gist.github.com/silviubogan/6df042228f50a7575e788f8f3b1d0b7d). At the end is the same error.

# Update 3

The issue was solved, see the commit before the last commit.
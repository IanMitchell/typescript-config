# @0x57/typescript-config

An opinionated shared TypeScript config targeting TypeScript v5.9.

## Usage

Install the package:

```sh
bun add -D @0x57/typescript-config
```

Then create or modify your `tsconfig.json` file depending on the situations below. 

## Next.js

```json
{
	"extends": "@0x57/typescript-config/nextjs.json"
}
```

# Library

```json
{
	"extends": "@0x57/typescript-config/library.json",
	"compilerOptions": {
		"rootDir": "src",
		"outDir": "dist"
	},
	"include": ["src", "test"],
	"exclude": ["node_modules", "dist"]
}
```

# Browser

The browser configuration assumes bundling with Vite.

```json
{
	"extends": "@0x57/typescript-config/browser.json",
	"compilerOptions": {
		"rootDir": "src",
		"outDir": "dist"
	},
	"include": ["src", "test"],
	"exclude": ["node_modules", "dist"]
}
```

# Server Application

If you are not using Bun, you may want to use the setup for a library instead.

```json
{
	"extends": "@0x57/typescript-config/base.json"
}
```

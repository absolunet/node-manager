# @absolunet/manager

[![npm][npm-badge]][npm-url]
[![npm dependencies][dependencies-badge]][dependencies-url]
[![Tests][tests-badge]][tests-url]
[![npms][npms-badge]][npms-url]
[![License: MIT][license-badge]][license-url]

> Manager for single/multi packages JavaScript projects


## Install

```bash
$ npm install @absolunet/manager
```


## Usage

In your `./package.json` file add
```json
{
	"scripts": {
		"manager:outdated": "node manager --task=outdated",
		"manager:build": "node manager --task=build",
		"manager:watch": "node manager --task=watch",
		"manager:fix": "node manager --task=fix",
		"manager:documentation": "node manager --task=documentation",
		"manager:prepare": "node manager --task=prepare",
		"manager:version": "node manager --task=version --release=$npm_config_release",
		"manager:rebuild": "node manager --task=rebuild"
	}
}
```


In a `./manager.js` file
```js
import { manager } from "@absolunet/manager";

manager.init({
	repositoryType: "single-package",
	dist: {
		node: {},
		browser: [
			{
				type: "module",
			},
		],
	},
});
```

or


```js
import { manager } from "@absolunet/manager";

manager.init({
	repositoryType: "multi-package",
	dist: {
		browser: [
			{
				type: "script",
				name: "my-super-pacakge",
			},
		],
	},
});
```


## Documentation

See the [full documentation](https://documentation.absolunet.com/node-manager) for an in-depth look.

See the [Changelog](CHANGELOG.md) to see what has changed.


## Contribute

See the [Contributing Guidelines](CONTRIBUTING.md) for ways to get started.

See the [Support Guide](SUPPORT.md) for ways to get help.

See the [Security Policy](SECURITY.md) for sharing vulnerability reports.

This project has a [Code of Conduct](CODE_OF_CONDUCT.md).
By interacting with this repository, organization, or community you agree to abide by its terms.


## License

[MIT](LICENSE) © [Absolunet](https://absolunet.com)




[npm-badge]:          https://img.shields.io/npm/v/@absolunet/manager?style=flat-square
[dependencies-badge]: https://img.shields.io/david/absolunet/node-manager?style=flat-square
[tests-badge]:        https://img.shields.io/github/workflow/status/absolunet/node-manager/tests/production?label=tests&style=flat-square
[npms-badge]:         https://badges.npms.io/%40absolunet%2Fmanager.svg?style=flat-square
[license-badge]:      https://img.shields.io/badge/license-MIT-green?style=flat-square

[npm-url]:          https://www.npmjs.com/package/@absolunet/manager
[dependencies-url]: https://david-dm.org/absolunet/node-manager
[tests-url]:        https://github.com/absolunet/node-manager/actions?query=workflow%3Atests+branch%3Aproduction
[npms-url]:         https://npms.io/search?q=%40absolunet%2Fmanager
[license-url]:      https://opensource.org/licenses/MIT

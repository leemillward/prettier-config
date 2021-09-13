# @leemillward/prettier-config
[![npm version](https://badge.fury.io/js/%40leemillward%2Fprettier-config.svg)](https://badge.fury.io/js/%40leemillward%2Fprettier-config)

[Shareable config](https://prettier.io/docs/en/configuration.html#sharing-configurations) for [Prettier](https://prettier.io/)

## Installation

Install Prettier and `@leemillward/prettier-config`:

```
npm install --save-dev prettier @leemillward/prettier-config
```

## Usage
Prettier rules come bundled in `@leemillward/prettier-config`. To enable these rules, add a `prettier` property in your `package.json`. See the [Prettier configuration docs](https://prettier.io/docs/en/configuration.html) for more details.

```json
"prettier": "@leemillward/prettier-config"
```

If you don't want to use `package.json`, you can use any of the supported extensions to export a string:

```jsonc
// `.prettierrc.json`
"@leemillward/prettier-config"
```

```javascript
// `prettier.config.js` or `.prettierrc.js`
module.exports = '@leemillward/prettier-config';
```

## Extending

This configuration is not intended to be changed, but if you have a setup where modification is required, it is possible. Prettier does not offer an "extends" mechanism as you might be familiar from tools such as ESLint.

To extend a configuration you will need to use a `prettier.config.js` or `.prettierrc.js` file that exports an object:

```javascript
module.exports = {
    ...require('@leemillward/prettier-config'),
    semi: false
};
```

## [CHANGELOG](CHANGELOG.md)

## [LICENSE](LICENSE)

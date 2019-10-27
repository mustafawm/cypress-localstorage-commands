[![Build status][travisci-image]][travisci-url] [![Coverage Status][coveralls-image]][coveralls-url] [![Quality Gate][quality-gate-image]][quality-gate-url]

[![NPM dependencies][npm-dependencies-image]][npm-dependencies-url] [![Last commit][last-commit-image]][last-commit-url] [![Last release][release-image]][release-url] 

[![NPM downloads][npm-downloads-image]][npm-downloads-url] [![License][license-image]][license-url]

# Cypress localStorage commands

Extends Cypress' cy commands with localStorage methods. Allows preserving localStorage between tests.

## The problem

You want to preserve localStorage between Cypress tests.

## This solution

This solution allows you to use all browser localStorage methods through Cypress commands, and preserve it between tests.

## Installation

This module is distributed via npm which is bundled with node and should be installed as one of your project's devDependencies:

```bash
npm i --save-dev cypress-localstorage-commands
```

## Usage

`cypress-localstorage-commands` extends Cypress' cy command.

Add this line to your project's `cypress/support/commands.js`:

```js
import "cypress-localstorage-commands"
```

You can now use all next commands:

```js
cy.saveLocalStorage() // Save current localStorage values into an internal "snapshot"
```

```js
cy.restoreLocalStorage() // Restore localStorage to previously "snapshot" saved values
```

```js
cy.clearLocalStorageSnapshot() // Clear localStorage "snapshot" values
```

```js
cy.getLocalStorage("item") // Get localStorage item
```

```js
cy.setLocalStorage("item", "value") // Set localStorage item
```

```js
cy.removeLocalStorage("item") // Remove localStorage item
```

## Contributing

Contributors are welcome.
Please read the [contributing guidelines](.github/CONTRIBUTING.md) and [code of conduct](.github/CODE_OF_CONDUCT.md).

## License

MIT, see [LICENSE](./LICENSE) for details.

[coveralls-image]: https://coveralls.io/repos/github/javierbrea/cypress-localstorage-commands/badge.svg
[coveralls-url]: https://coveralls.io/github/javierbrea/cypress-localstorage-commands
[travisci-image]: https://travis-ci.com/javierbrea/cypress-localstorage-commands.svg?branch=master
[travisci-url]: https://travis-ci.com/javierbrea/cypress-localstorage-commands
[last-commit-image]: https://img.shields.io/github/last-commit/javierbrea/cypress-localstorage-commands.svg
[last-commit-url]: https://github.com/javierbrea/cypress-localstorage-commands/commits
[license-image]: https://img.shields.io/npm/l/cypress-localstorage-commands.svg
[license-url]: https://github.com/javierbrea/cypress-localstorage-commands/blob/master/LICENSE
[npm-downloads-image]: https://img.shields.io/npm/dm/cypress-localstorage-commands.svg
[npm-downloads-url]: https://www.npmjs.com/package/cypress-localstorage-commands
[npm-dependencies-image]: https://img.shields.io/david/javierbrea/cypress-localstorage-commands.svg
[npm-dependencies-url]: https://david-dm.org/javierbrea/cypress-localstorage-commands
[quality-gate-image]: https://sonarcloud.io/api/project_badges/measure?project=cypress-localstorage-commands&metric=alert_status
[quality-gate-url]: https://sonarcloud.io/dashboard?id=cypress-localstorage-commands
[release-image]: https://img.shields.io/github/release-date/javierbrea/cypress-localstorage-commands.svg
[release-url]: https://github.com/javierbrea/cypress-localstorage-commands/releases

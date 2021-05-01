# Changelog

All notable changes to this project will be documented in this file. See [standard-version](https://github.com/conventional-changelog/standard-version) for commit guidelines.

## [2.0.0](https://github.com/bjoerge/rxjs-exhaustmap-with-trailing/compare/v1.1.0...v2.0.0) (2021-05-01)


### ⚠ BREAKING CHANGES

* **deps:** Due to a change in the `throttle()` operator in RxJS 7, `exhaustMapWithTrailing()` now guarantees that the final value from the source observable gets emitted, even after the source has completed.

### Features

* **deps:** update rxjs peer dependency to 7.x and update test for trailing emmision ([6a3006a](https://github.com/bjoerge/rxjs-exhaustmap-with-trailing/commit/6a3006a0117f588ec7bf25ae934c1542c1f6903b))

## [1.1.0](https://github.com/bjoerge/rxjs-exhaustmap-with-trailing/compare/v1.0.0...v1.1.0) (2021-04-07)

* feat: defer to avoid sharing subject between subscribers ([959ae75](https://github.com/bjoerge/rxjs-exhaustmap-with-trailing/commit/959ae75))

## [1.0.1](https://github.com/bjoerge/rxjs-exhaustmap-with-trailing/compare/v1.0.0...v1.1.0) (2021-03-26)

* chore: add marble diagram ([aa329bd](https://github.com/bjoerge/rxjs-exhaustmap-with-trailing/commit/aa329bd))
* core: linkify readme, update example and add link to CodeSandbox ([9820a6d](https://github.com/bjoerge/rxjs-exhaustmap-with-trailing/commit/9820a6d))

## [1.0.0](https://github.com/bjoerge/rxjs-exhaustmap-with-trailing/commit/0b8f8de) (2021-03-24)

* initial commit ([0b8f8de](https://github.com/bjoerge/rxjs-exhaustmap-with-trailing/commit/0b8f8de))

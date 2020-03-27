# move-path

**:warning: Project has been transferred to [NexTools metarepo](https://github.com/nextools/metarepo/tree/master/packages/move-path)**

[![npm](https://img.shields.io/npm/v/move-path.svg?style=flat-square)](https://www.npmjs.com/package/move-path) [![linux](https://img.shields.io/travis/deepsweet/move-path/master.svg?label=linux&style=flat-square)](https://travis-ci.org/deepsweet/move-path) [![windows](https://img.shields.io/appveyor/ci/deepsweet/move-path/master.svg?label=windows&style=flat-square)](https://ci.appveyor.com/project/deepsweet/move-path) [![coverage](https://img.shields.io/codecov/c/github/deepsweet/move-path.svg?style=flat-square)](https://codecov.io/github/deepsweet/move-path)

Move path to destination folder.

## Requirements

* Node.js >= 8.6.0

## Install

```sh
$ yarn add move-path
```

## Usage

```js
movePath(from, to)
```

Handles both relative and absolute `from` and `to` and returns an absolute destination path.

```js
import movePath from 'move-path'

movePath('src/foo/bar/index.js', 'build/baz/')
// /absolute/build/baz/foo/bar/index.js

movePath('src/foo/bar/', 'build/baz/')
// /absolute/build/baz/foo/bar/

movePath('src/foo/bar/index.js', 'src/foo/')
// /absolute/src/foo/bar/index.js

movePath('src/foo/bar/', 'src/foo/bar')
// /absolute/src/foo/bar/

movePath('src/foo/bar/index.js', '/build/')
// /build/foo/bar/index.js

movePath('src/foo/bar/index.js', './')
// /absolute/src/foo/bar/index.js
```

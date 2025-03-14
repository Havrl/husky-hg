# Only installs precommit hook and using shell=True to fix npm path in Windows 10. 

# husky-hg [![](http://img.shields.io/npm/dm/husky-hg.svg?style=flat)](https://www.npmjs.org/package/husky-hg) [![npm version](https://badge.fury.io/js/husky-hg.svg)](https://www.npmjs.com/package/husky-hg) [![Mac/Linux Build Status](https://img.shields.io/travis/tobiastimm/husky-hg/master.svg?label=Mac%20OSX%20%26%20Linux)](https://travis-ci.org/tobiastimm/husky-hg) [![Windows Build status](https://img.shields.io/appveyor/ci/tobiastimm/husky-hg/master.svg?label=Windows)](https://ci.appveyor.com/project/tobiastimm/husky-hg/branch/master)

> Git / Mercurial hooks made easy.
>
> `husky-hg` is a fork of `husky`.
> The only difference is, that Mercurial is
> supported as an alternative to git.
>

Husky can prevent bad commit, push and more :dog: _woof!_

## Install

```sh
npm install husky-hg --save-dev
```

```sh
yarn add husky-hg --dev
```

```javascript
// Edit package.json
{
  "scripts": {
    "precommit": "npm test",
    "prepush": "npm test",
    "...": "..."
  }
}
```

```bash
git commit -m "Keep calm and commit"
```

_Existing hooks aren't replaced and you can use [any git/Mercurial hook](HOOKS.md)._

_If you're migrating from `ghooks`, simply run `npm uninstall ghooks --save-dev && npm install husky --save-dev` and edit `package.json`. Husky will automatically migrate `ghooks` hooks._

## Used by

* [jQuery](https://github.com/jquery/jquery)
* [Next.js](https://github.com/zeit/next.js)
* [Hyper](https://github.com/zeit/hyper)
* [Paper.js](https://github.com/paperjs/paper.js)
* [Kibana](https://github.com/elastic/kibana)
* [JSON Server](https://github.com/typicode/json-server)
* [Hotel](https://github.com/typicode/hotel)
* ... and 12000+ [other awesome projects](https://libraries.io/npm/husky/dependent-repositories).

## Uninstall

```sh
npm uninstall husky-hg
```

```sh
yarn remove husky-hg
```

## Tricks

<details>

### Debug hooks easily

If you need to debug hooks, simply use `npm run <script-name>`. For example:

```bash
npm run precommit
```

### Git GUI clients support

If you've installed Node using the [standard installer](https://nodejs.org/en/), [nvm](https://github.com/creationix/nvm) or [homebrew](http://brew.sh/), Git hooks will be executed in GUI applications.

### Working with multiple version of Node

If [`nvm`](https://github.com/creationix/nvm) is installed, husky will try to use the `default`/`current` installed Node version or use the project `.nvmrc`.

__Tip__ to use the system-installed version of node, `nvm` provides a [`system`](https://github.com/creationix/nvm#system-version-of-node) alias

### Accessing Git params

Git params can be found in `GIT_PARAMS` environment variable.

### Setting a different log level

By default, husky will run scripts using `--silent` to make the output more readable. If you want to override this, simply pass a different log level to your scripts:

```json
"precommit": "npm run some-script -q"
```

_`-q/--quiet` is equivalent to `--loglevel warn` which is npm default log level._

### Git submodule and subtree support

Yes

### Mercurial subrepo support

No

### Cygwin support

Yes

### Yarn support

Please use `yarn` `v0.24+`

</details>

## See also

* [pkg-ok](https://github.com/typicode/pkg-ok) - Prevents publishing modules with bad paths
* [please-upgrade-node](https://github.com/typicode/please-upgrade-node) - Show a message to upgrade Node instead of a stacktrace in your CLIs
* [react-fake-props](https://github.com/typicode/react-fake-props) - Fake props for your React tests

## License

MIT

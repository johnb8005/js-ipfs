<p align="center">
<a href="https://js.ipfs.io" title="JS IPFS">
  <img src="https://ipfs.io/ipfs/Qme6KJdKcp85TYbLxuLV7oQzMiLremD7HMoXLZEmgo6Rnh/js-ipfs-sticker.png" alt="IPFS in JavaScript logo" width="244" />
</a>
</p>

<h3 align="center">The JavaScript implementation of the IPFS protocol</h3>

<p align="center">
<a href="https://riot.im/app/#/room/#ipfs-dev:matrix.org"><img src="https://img.shields.io/badge/matrix-%23ipfs%3Amatrix.org-blue.svg?style=flat" /> </a>
<a href="http://webchat.freenode.net/?channels=%23ipfs"><img src="https://img.shields.io/badge/freenode-%23ipfs-blue.svg?style=flat" /></a>
<a href="https://discord.gg/24fmuwR"><img src="https://img.shields.io/discord/475789330380488707?color=blueviolet&label=discord&style=flat" /></a>
<a href="https://github.com/ipfs/team-mgmt/blob/master/MGMT_JS_CORE_DEV.md"><img src="https://img.shields.io/badge/team-mgmt-blue.svg?style=flat" /></a>
</p>

<p align="center">
<a href="https://github.com/ipfs/js-ipfs/tree/master/packages/interface-ipfs-core"><img src="https://img.shields.io/badge/interface--ipfs--core-API%20Docs-blue.svg"></a>
<a href="https://travis-ci.com/ipfs/js-ipfs?branch=master"><img src="https://badgen.net/travis/ipfs/js-ipfs?branch=master" /></a>
<a href="https://codecov.io/gh/ipfs/js-ipfs"><img src="https://badgen.net/codecov/c/github/ipfs/js-ipfs" /></a>
<a href="https://bundlephobia.com/result?p=ipfs"><img src="https://badgen.net/bundlephobia/minzip/ipfs"></a>
<a href="https://david-dm.org/ipfs/js-ipfs?path=packages/ipfs-core"><img src="https://david-dm.org/ipfs/js-ipfs.svg?style=flat&path=packages/ipfs-core" /></a>
<a href="https://github.com/feross/standard"><img src="https://img.shields.io/badge/code%20style-standard-brightgreen.svg?style=flat"></a>
<a href=""><img src="https://img.shields.io/badge/npm-%3E%3D6.0.0-orange.svg?style=flat" /></a>
<a href=""><img src="https://img.shields.io/badge/Node.js-%3E%3D10.0.0-orange.svg?style=flat" /></a>
<a href="https://www.npmjs.com/package/ipfs"><img src="https://img.shields.io/npm/dm/ipfs.svg" /></a>
<a href="https://www.jsdelivr.com/package/npm/ipfs"><img src="https://data.jsdelivr.com/v1/package/npm/ipfs/badge"/></a>
<br>
</p>

# ipfs-core <!-- omit in toc -->

> The IPFS Core API

`ipfs-core` is the implementation of the IPFS Core API. It contains all you need to integrate IPFS into your application.

If you want to run IPFS as a standalone daemon process, see the [ipfs](https://github.com/ipfs/js-ipfs/tree/master/packages/ipfs) module.

## Table of Contents <!-- omit in toc -->

- [Getting Started](#getting-started)
- [Next Steps](#next-steps)
  - [Browser CDN](#browser-cdn)
  - [Browser bundle](#browser-bundle)
- [Want to hack on IPFS?](#want-to-hack-on-ipfs)
- [License](#license)

## Getting Started

The `ipfs-core` package contains all the features of `ipfs` but in a lighter package without the CLI or HTTP servers:

```console
$ npm install ipfs-core
```

Then start a node in your app:

```javascript
import * as IPFS from 'ipfs-core'

const ipfs = await IPFS.create()
const { cid } = await ipfs.add('Hello world')
console.info(cid)
// QmXXY5ZxbtuYj6DnfApLiGstzPN7fvSyigrRee3hDWPCaf
```

## Next Steps

* Look into the [examples](/examples) to learn how to spawn an IPFS node in Node.js and in the Browser
* Read the [Core API docs](https://github.com/ipfs/js-ipfs/tree/master/docs/core-api) to see what you can do with an IPFS node
* Visit https://dweb-primer.ipfs.io to learn about IPFS and the concepts that underpin it
* Head over to https://proto.school to take interactive tutorials that cover core IPFS APIs
* Check out https://docs.ipfs.io for tips, how-tos and more
* See https://blog.ipfs.io for news and more
* Need help? Please ask 'How do I?' questions on https://discuss.ipfs.io

### Browser CDN

You can load IPFS right in your browser by adding the following to your page using the super fast [jsdelivr](https://www.jsdelivr.com) CDN:

```html
<!-- loading the minified version using jsDelivr -->
<script src="https://cdn.jsdelivr.net/npm/ipfs-core/dist/index.min.js"></script>

<!-- loading the human-readable (not minified) version jsDelivr -->
<script src="https://cdn.jsdelivr.net/npm/ipfs-core/dist/index.min.js"></script>
```

Inserting one of the above lines will make an `IpfsCore` object available in the global namespace:

```html
<script>
async function main () {
const node = await window.IpfsCore.create()
// Ready to use!
// See https://github.com/ipfs/js-ipfs#core-api
}
main()
</script>
```

### Browser bundle

Learn how to bundle IPFS into your application with webpack, parceljs and browserify in the [examples](https://github.com/ipfs/js-ipfs/tree/master/examples).

## Want to hack on IPFS?

[![](https://cdn.rawgit.com/jbenet/contribute-ipfs-gif/master/img/contribute.gif)](https://github.com/ipfs/community/blob/master/CONTRIBUTING.md)

The IPFS implementation in JavaScript needs your help!  There are a few things you can do right now to help out:

Read the [Code of Conduct](https://github.com/ipfs/community/blob/master/code-of-conduct.md) and [JavaScript Contributing Guidelines](https://github.com/ipfs/community/blob/master/CONTRIBUTING_JS.md).

- **Check out existing issues** The [issue list](https://github.com/ipfs/js-ipfs/issues) has many that are marked as ['help wanted'](https://github.com/ipfs/js-ipfs/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc+label%3A%22help+wanted%22) or ['difficulty:easy'](https://github.com/ipfs/js-ipfs/issues?q=is%3Aissue+is%3Aopen+sort%3Aupdated-desc+label%3Adifficulty%3Aeasy) which make great starting points for development, many of which can be tackled with no prior IPFS knowledge
- **Look at the [IPFS Roadmap](https://github.com/ipfs/roadmap)** This are the high priority items being worked on right now
- **Perform code reviews** More eyes will help
a. speed the project along
b. ensure quality, and
c. reduce possible future bugs.
- **Add tests**. There can never be enough tests.
- **Join the [Weekly Core Implementations Call](https://github.com/ipfs/team-mgmt/issues/992)** it's where everyone discusses what's going on with IPFS and what's next

## License

[![FOSSA Status](https://app.fossa.io/api/projects/git%2Bgithub.com%2Fipfs%2Fjs-ipfs.svg?type=large)](https://app.fossa.io/projects/git%2Bgithub.com%2Fipfs%2Fjs-ipfs?ref=badge_large)

[![](https://github.com/ipfs/js-ipfs/raw/master/packages/interface-ipfs-core/img/badge.png)](https://github.com/ipfs/js-ipfs/tree/master/packages/interface-ipfs-core)

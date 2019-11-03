---
id: n-version-manager
title: Managing different node versions using n
sidebar_label: Node version management
---

For development purposes, we might have to switch between multiple node.js version when working across different projects. To help managing different node versions, we can use the open source tool called [n](https://github.com/tj/n)

## Installation

If you already have node installed in your project, you can install n using the following command

```sh
npm install -g n
```

If you don't have node installed, you can use one of the third party installers like [n-install](https://github.com/mklement0/n-install) using the following command

```sh
curl -L https://git.io/n-install | bash
```

## Basic Usage

Simply execute `n <version>` to download and install a version of node. If `<version>` has already been downloaded, `n` will install from its cache.

```sh
n 10.16.0
n lts
```

Execute n on its own to view your downloaded versions, and install the selected version.

```
$ n

  node/4.9.1
ο node/8.11.3
  node/10.15.0
```

Use `up`/`down` arrow keys to select a version, return key to install, `d` to delete, `q` to quit
(You can also use `j` and `k` to navigate up or down without using arrows.)

If the active node version does not change after install, try opening a new shell in case seeing a stale version.

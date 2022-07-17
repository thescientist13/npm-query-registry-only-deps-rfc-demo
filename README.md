# npm-query-tarball-test

## Overview

Test repo for npm [RFC for Registry Only Tarballs](https://github.com/npm/rfcs/pull/593/) and testing with a locally linked version of npm with [`npm query`](https://github.com/npm/cli/pull/5000) command.

> `npm query` [RFC for reference](https://github.com/npm/rfcs/pull/564/).

It comes pre-installed with these dependencies, so that `query` can be tested in order to come up with an appropriate API and recommendation for the RFC.
```json
{
  "...": "",
  
  "dependencies": {
    "@babel/cli": "^7.4.0",
    "eslint": "git+https://github.com/eslint/eslint.git"
  }
}
```

## Testing

1. Clone the npm CLI and [follow these steps](https://github.com/npm/cli/blob/latest/CONTRIBUTING.md#development) to get it running locally
1. Run `npm . link`
1. Clone this repo and run `npm ci`

You should now be able to run the `query` command in this repo, e.g.
```sh
$ npm query ":root > *"
```
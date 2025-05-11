[![Release](https://github.com/asd-xiv/ts-config/actions/workflows/release.yml/badge.svg?branch=main)](https://github.com/asd-xiv/ts-config/actions/workflows/release.yml)
[![npm version](https://img.shields.io/npm/v/@asd14/ts-config.svg)](https://www.npmjs.com/package/@asd14/ts-config)

# @asd14/ts-config

> ASD14's reusable TypeScript configurations.

<!-- vim-markdown-toc GFM -->

* [Installation](#installation)
* [Usage](#usage)
* [Targets](#targets)
    * [Common Configuration](#common-configuration)
    * [Node](#node)
    * [React](#react)
    * [Ink](#ink)
* [Peer dependencies](#peer-dependencies)
* [License](#license)

<!-- vim-markdown-toc -->

## Installation

```sh
npm install --save-dev @asd14/ts-config typescript@^5
```

## Usage

In your `tsconfig.json`, extend the desired configuration:

```json
{
  "extends": "@asd14/ts-config/targets/react.json"
}
```

## Targets

There are 3 configurations, each tailored for a specific **target environment**:
`node`, `react` and [`ink`](https://github.com/vadimdemedes/ink).

### Common Configuration

All 3 targets extend a common set of rules:

```json
{
  "allowImportingTsExtensions": true,
  "allowJs": true,
  "checkJs": true,
  "declaration": true,
  "esModuleInterop": true,
  "forceConsistentCasingInFileNames": true,
  "incremental": true,
  "moduleDetection": "force",
  "noFallthroughCasesInSwitch": true,
  "noImplicitOverride": true,
  "noImplicitReturns": true,
  "noPropertyAccessFromIndexSignature": true,
  "noUncheckedIndexedAccess": true,
  "noUnusedLocals": true,
  "noUnusedParameters": true,
  "removeComments": false,
  "resolveJsonModule": true,
  "skipDefaultLibCheck": true,
  "skipLibCheck": true,
  "sourceMap": true,
  "strict": true
}
```

### Node

```json
// @asd14/ts-config/targets/node.json
{
  "module": "nodenext",
  "moduleResolution": "nodenext",
  "target": "es2022",
  "lib": ["es2023"],
  "types": ["node"]
}
```

### React

```json
// @asd14/ts-config/targets/react.json
{
  "module": "esnext",
  "moduleResolution": "bundler",
  "target": "esnext",
  "jsx": "preserve",
  "lib": ["dom", "dom.iterable", "esnext"]
}
```

### Ink

```json
// @asd14/ts-config/targets/ink.json
{
  "module": "esnext",
  "moduleResolution": "nodenext",
  "target": "esnext",
  "jsx": "preserve",
  "lib": ["es2023", "dom"],
  "types": ["node"]
}
```

## Peer dependencies

This package requires and assumes you already installed:

```json
  "peerDependencies": {
    "typescript": "^5"
  },
```

## License

MIT

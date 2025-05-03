# @asd14/ts-config

> ASD14's reusable TypeScript configurations.

<!-- vim-markdown-toc GFM -->

* [Installation](#installation)
* [Usage](#usage)
* [Configuration Details](#configuration-details)
    * [Common Configuration](#common-configuration)
    * [Node Configuration](#node-configuration)
    * [React Configuration](#react-configuration)
    * [Ink Configuration](#ink-configuration)
* [Peer Dependency](#peer-dependency)
* [License](#license)

<!-- vim-markdown-toc -->

## Installation

Install via npm:

```sh
npm install --save-dev @asd14/ts-config
```

## Usage

In your `tsconfig.json`, extend the desired configuration:

```json
{
  "extends": "@asd14/ts-config/targets/react.json"
}
```

Choose from:

- [`@asd14/ts-config/targets/common.json`](/targets/common.json)
- [`@asd14/ts-config/targets/ink.json`](/targets/ink.json)
- [`@asd14/ts-config/targets/node.json`](/targets/node.json)
- [`@asd14/ts-config/targets/react.json`](/targets/react.json)

## Configuration Details

### Common Configuration

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

### Node Configuration

```json
{
  "module": "nodenext",
  "moduleResolution": "nodenext",
  "target": "es2022",
  "lib": ["es2023"],
  "types": ["node"]
}
```

### React Configuration

```json
{
  "module": "esnext",
  "moduleResolution": "bundler",
  "target": "esnext",
  "jsx": "preserve",
  "lib": ["dom", "dom.iterable", "esnext"]
}
```

### Ink Configuration

```json
{
  "module": "esnext",
  "moduleResolution": "nodenext",
  "target": "esnext",
  "jsx": "preserve",
  "lib": ["es2023", "dom"],
  "types": ["node"]
}
```

## Peer Dependency

- **TypeScript**: This config requires TypeScript version ^5.

## License

MIT

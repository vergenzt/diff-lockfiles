# diff-lockfiles

Note: this is a fork of <https://github.com/mxweaver/lock-diff>, but it
operates on Git commit ranges rather than on files.

[![npm](https://img.shields.io/npm/v/diff-lockfiles)](https://www.npmjs.com/package/diff-lockfiles)
[![airbnb-style](https://img.shields.io/badge/style-airbnb-blue.svg)](https://github.com/airbnb/javascript)

## Example

```sh
npm install
diff-lockfiles origin/main dependabot/branch
```

## Usage

```text
Usage:  auto-lock-diff.js [options] <from> <to>

diff all changed package-lock.json files in repo

Options:
  -V, --version          output the version number
  -f, --format <format>  changes the output format (default: "text")
  -m, --max-buffer       maximum read buffer size
  -c, --color            colorizes certain output formats (default: false)
  -h, --help             display help for command
```

### `--format=text` (default)

```text
$ diff-lockfiles.js --format text HEAD~1 HEAD
node_modules/@jest/console 29.6.2 -> 29.6.3
node_modules/@jest/core 29.6.2 -> 29.6.3
node_modules/@jest/environment 29.6.2 -> 29.6.3
node_modules/@jest/expect 29.6.2 -> 29.6.3
node_modules/@jest/expect-utils 29.6.2 -> 29.6.3
node_modules/@jest/fake-timers 29.6.2 -> 29.6.3
node_modules/@jest/globals 29.6.2 -> 29.6.3
node_modules/@jest/reporters 29.6.2 -> 29.6.3
node_modules/@jest/schemas 29.6.0 -> 29.6.3
node_modules/@jest/source-map 29.6.0 -> 29.6.3
node_modules/@jest/test-result 29.6.2 -> 29.6.3
node_modules/@jest/test-sequencer 29.6.2 -> 29.6.3
node_modules/@jest/transform 29.6.2 -> 29.6.3
node_modules/@jest/types 29.6.1 -> 29.6.3
node_modules/@types/babel__core 7.20.0 -> 7.20.1
node_modules/@types/babel__traverse 7.18.2 -> 7.20.1
node_modules/babel-jest 29.6.2 -> 29.6.3
node_modules/babel-plugin-jest-hoist 29.5.0 -> 29.6.3
node_modules/babel-preset-jest 29.5.0 -> 29.6.3
node_modules/dedent 1.3.0 -> 1.5.1
node_modules/diff-sequences 29.4.3 -> 29.6.3
node_modules/expect 29.6.2 -> 29.6.3
node_modules/fsevents 2.3.2 -> 2.3.3
node_modules/is-core-module 2.12.1 -> 2.13.0
node_modules/jest 29.6.2 -> 29.6.3
node_modules/jest-changed-files 29.5.0 -> 29.6.3
node_modules/jest-circus 29.6.2 -> 29.6.3
node_modules/jest-cli 29.6.2 -> 29.6.3
node_modules/jest-config 29.6.2 -> 29.6.3
node_modules/jest-diff 29.6.2 -> 29.6.3
node_modules/jest-docblock 29.4.3 -> 29.6.3
node_modules/jest-each 29.6.2 -> 29.6.3
node_modules/jest-environment-node 29.6.2 -> 29.6.3
node_modules/jest-get-type 29.4.3 -> 29.6.3
node_modules/jest-haste-map 29.6.2 -> 29.6.3
node_modules/jest-leak-detector 29.6.2 -> 29.6.3
node_modules/jest-matcher-utils 29.6.2 -> 29.6.3
node_modules/jest-message-util 29.6.2 -> 29.6.3
node_modules/jest-mock 29.6.2 -> 29.6.3
node_modules/jest-regex-util 29.4.3 -> 29.6.3
node_modules/jest-resolve 29.6.2 -> 29.6.3
node_modules/jest-resolve-dependencies 29.6.2 -> 29.6.3
node_modules/jest-runner 29.6.2 -> 29.6.3
node_modules/jest-runtime 29.6.2 -> 29.6.3
node_modules/jest-snapshot 29.6.2 -> 29.6.3
node_modules/jest-util 29.6.2 -> 29.6.3
node_modules/jest-validate 29.6.2 -> 29.6.3
node_modules/jest-watcher 29.6.2 -> 29.6.3
node_modules/jest-worker 29.6.2 -> 29.6.3
node_modules/pretty-format 29.6.2 -> 29.6.3
node_modules/resolve 1.22.2 -> 1.22.4
node_modules/@jest/reporters/node_modules/istanbul-lib-instrument added
```

### `--format=json`

`diff-lockfiles.js --format text HEAD~1 HEAD`

```json
{
  "node_modules/@jest/console": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/@jest/core": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/@jest/environment": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/@jest/expect": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/@jest/expect-utils": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/@jest/fake-timers": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/@jest/globals": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/@jest/reporters": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/@jest/schemas": [
    "29.6.0",
    "29.6.3"
  ],
  "node_modules/@jest/source-map": [
    "29.6.0",
    "29.6.3"
  ],
  "node_modules/@jest/test-result": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/@jest/test-sequencer": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/@jest/transform": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/@jest/types": [
    "29.6.1",
    "29.6.3"
  ],
  "node_modules/@types/babel__core": [
    "7.20.0",
    "7.20.1"
  ],
  "node_modules/@types/babel__traverse": [
    "7.18.2",
    "7.20.1"
  ],
  "node_modules/babel-jest": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/babel-plugin-jest-hoist": [
    "29.5.0",
    "29.6.3"
  ],
  "node_modules/babel-preset-jest": [
    "29.5.0",
    "29.6.3"
  ],
  "node_modules/dedent": [
    "1.3.0",
    "1.5.1"
  ],
  "node_modules/diff-sequences": [
    "29.4.3",
    "29.6.3"
  ],
  "node_modules/expect": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/fsevents": [
    "2.3.2",
    "2.3.3"
  ],
  "node_modules/is-core-module": [
    "2.12.1",
    "2.13.0"
  ],
  "node_modules/jest": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-changed-files": [
    "29.5.0",
    "29.6.3"
  ],
  "node_modules/jest-circus": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-cli": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-config": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-diff": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-docblock": [
    "29.4.3",
    "29.6.3"
  ],
  "node_modules/jest-each": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-environment-node": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-get-type": [
    "29.4.3",
    "29.6.3"
  ],
  "node_modules/jest-haste-map": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-leak-detector": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-matcher-utils": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-message-util": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-mock": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-regex-util": [
    "29.4.3",
    "29.6.3"
  ],
  "node_modules/jest-resolve": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-resolve-dependencies": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-runner": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-runtime": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-snapshot": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-util": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-validate": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-watcher": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/jest-worker": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/pretty-format": [
    "29.6.2",
    "29.6.3"
  ],
  "node_modules/resolve": [
    "1.22.2",
    "1.22.4"
  ],
  "node_modules/@jest/reporters/node_modules/istanbul-lib-instrument": [
    null,
    "6.0.0"
  ]
}
```

### `--format=table`

```texst
$ diff-lockfiles.js --format table HEAD~1 HEAD
╔═══════════════════════════════════════════════════════════════════╤═════════════╤═════════════╗
║ package-lock.json                                                 │             │             ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ package                                                           │ old version │ new version ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/@jest/console                                        │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/@jest/core                                           │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/@jest/environment                                    │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/@jest/expect                                         │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/@jest/expect-utils                                   │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/@jest/fake-timers                                    │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/@jest/globals                                        │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/@jest/reporters                                      │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/@jest/schemas                                        │ 29.6.0      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/@jest/source-map                                     │ 29.6.0      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/@jest/test-result                                    │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/@jest/test-sequencer                                 │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/@jest/transform                                      │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/@jest/types                                          │ 29.6.1      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/@types/babel__core                                   │ 7.20.0      │ 7.20.1      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/@types/babel__traverse                               │ 7.18.2      │ 7.20.1      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/babel-jest                                           │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/babel-plugin-jest-hoist                              │ 29.5.0      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/babel-preset-jest                                    │ 29.5.0      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/dedent                                               │ 1.3.0       │ 1.5.1       ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/diff-sequences                                       │ 29.4.3      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/expect                                               │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/fsevents                                             │ 2.3.2       │ 2.3.3       ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/is-core-module                                       │ 2.12.1      │ 2.13.0      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest                                                 │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-changed-files                                   │ 29.5.0      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-circus                                          │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-cli                                             │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-config                                          │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-diff                                            │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-docblock                                        │ 29.4.3      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-each                                            │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-environment-node                                │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-get-type                                        │ 29.4.3      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-haste-map                                       │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-leak-detector                                   │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-matcher-utils                                   │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-message-util                                    │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-mock                                            │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-regex-util                                      │ 29.4.3      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-resolve                                         │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-resolve-dependencies                            │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-runner                                          │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-runtime                                         │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-snapshot                                        │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-util                                            │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-validate                                        │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-watcher                                         │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/jest-worker                                          │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/pretty-format                                        │ 29.6.2      │ 29.6.3      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/resolve                                              │ 1.22.2      │ 1.22.4      ║
╟───────────────────────────────────────────────────────────────────┼─────────────┼─────────────╢
║ node_modules/@jest/reporters/node_modules/istanbul-lib-instrument │ null        │ 6.0.0       ║
╚═══════════════════════════════════════════════════════════════════╧═════════════╧═════════════╝
```

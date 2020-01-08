Minimal repro of (https://github.com/nestjs/nest-cli/issues/523)[https://github.com/nestjs/nest-cli/issues/523]

To repro, clone this repository, then run:

```
$ yarn
$ yarn server build
yarn run v1.19.0
$ yarn workspace cli-bug-repro-server build
$ rimraf dist
$ nest build
src/app.controller.ts:10:28 - error TS1109: Expression expected.

10     return this.appService?.getHello();
                              ~
src/app.controller.ts:10:39 - error TS1005: ':' expected.

10     return this.appService?.getHello();
                                         ~

Found 2 error(s).

error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
error Command failed.
Exit code: 1
Command: /usr/local/Cellar/node/12.9.0/bin/node
Arguments: /Users/davidgolightly/.yarn/lib/cli.js build
Directory: /Users/davidgolightly/dev/cli-bug-repro/server
Output:

info Visit https://yarnpkg.com/en/docs/cli/workspace for documentation about this command.
error Command failed with exit code 1.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.

❗ [Wed Jan  8 13:46:38 PST 2020]
```
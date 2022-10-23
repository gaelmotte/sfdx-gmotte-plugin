# @gaelmotte/gmotte-sfdx-plugin

[![Version](https://img.shields.io/npm/v/@gaelmotte/gmotte-sfdx-plugin.svg)](https://npmjs.org/package/@gaelmotte/gmotte-sfdx-plugin)
[![CircleCI](https://circleci.com/gh/gaelmotte/gmotte-sfdx-plugin/tree/main.svg?style=shield)](https://circleci.com/gh/gaelmotte/gmotte-sfdx-plugin/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/@gaelmotte/gmotte-sfdx-plugin.svg)](https://npmjs.org/package/@gaelmotte/gmotte-sfdx-plugin)
[![License](https://img.shields.io/npm/l/@gaelmotte/gmotte-sfdx-plugin.svg)](https://github.com/gaelmotte/gmotte-sfdx-plugin/blob/main/package.json)

Personal sfdx plugin to ease my everyday life

<!-- toc -->
* [@gaelmotte/gmotte-sfdx-plugin](#gaelmottegmotte-sfdx-plugin)
* [Debugging your plugin](#debugging-your-plugin)
* [GitFlow](#gitflow)
<!-- tocstop -->
      <!-- install -->
      <!-- usage -->
```sh-session
$ npm install -g @gaelmotte/gmotte-sfdx-plugin
$ sfdx COMMAND
running command...
$ sfdx (--version)
@gaelmotte/gmotte-sfdx-plugin/0.5.0-alpha.0 linux-x64 node-v19.0.0
$ sfdx --help [COMMAND]
USAGE
  $ sfdx COMMAND
...
```
<!-- usagestop -->
<!-- commands -->
* [`sfdx gmotte:org:switch [-g] [--json] [--loglevel trace|debug|info|warn|error|fatal|TRACE|DEBUG|INFO|WARN|ERROR|FATAL]`](#sfdx-gmotteorgswitch--g---json---loglevel-tracedebuginfowarnerrorfataltracedebuginfowarnerrorfatal)

## `sfdx gmotte:org:switch [-g] [--json] [--loglevel trace|debug|info|warn|error|fatal|TRACE|DEBUG|INFO|WARN|ERROR|FATAL]`

Interractively switch default username and default devhub

```
USAGE
  $ sfdx gmotte:org:switch [-g] [--json] [--loglevel
    trace|debug|info|warn|error|fatal|TRACE|DEBUG|INFO|WARN|ERROR|FATAL]

FLAGS
  -g, --global                                                                      Set the configuration variables
                                                                                    globally, so they can be used from
                                                                                    any Salesforce DX project.
  --json                                                                            format output as json
  --loglevel=(trace|debug|info|warn|error|fatal|TRACE|DEBUG|INFO|WARN|ERROR|FATAL)  [default: warn] logging level for
                                                                                    this command invocation

DESCRIPTION
  Interractively switch default username and default devhub

EXAMPLES
  $ sfdx gmotte:org:switch

  $ sfdx gmotte:org:switch -g
```

_See code: [src/commands/gmotte/org/switch.ts](https://github.com/gaelmotte/gmotte-sfdx-plugin/blob/v0.5.0-alpha.0/src/commands/gmotte/org/switch.ts)_
<!-- commandsstop -->
<!-- debugging-your-plugin -->

# Debugging your plugin

We recommend using the Visual Studio Code (VS Code) IDE for your plugin development. Included in the `.vscode` directory of this plugin is a `launch.json` config file, which allows you to attach a debugger to the node process when running your commands.

To debug the `gmotte:org:switch` command:

1. Start the inspector

If you linked your plugin to the sfdx cli, call your command with the `dev-suspend` switch:

```sh-session
$ sfdx gmotte:org:switch --dev-suspend
```

Alternatively, to call your command using the `bin/run` script, set the `NODE_OPTIONS` environment variable to `--inspect-brk` when starting the debugger:

```sh-session
$ NODE_OPTIONS=--inspect-brk bin/run gmotte:org:switch
```

2. Set some breakpoints in your command code
3. Click on the Debug icon in the Activity Bar on the side of VS Code to open up the Debug view.
4. In the upper left hand corner of VS Code, verify that the "Attach to Remote" launch configuration has been chosen.
5. Hit the green play button to the left of the "Attach to Remote" launch configuration window. The debugger should now be suspended on the first line of the program.
6. Hit the green play button at the top middle of VS Code (this play button will be to the right of the play button that you clicked in step #5).
   <br><img src=".images/vscodeScreenshot.png" width="480" height="278"><br>
   Congrats, you are debugging!

# GitFlow

document me

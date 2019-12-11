# typescript-dev

This repository contains all the boilerplate settings you need to allow a ready-to-go development environment of Typescript using vscode. 
You get the following:
1. Static code analysis - using [gts](https://github.com/google/gts) and [tslint](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-typescript-tslint-plugin)
1. Continous testing - using [Jest](https://github.com/facebook/jest)
1. Instant code coverage feedback - via [Jest vscode plugin](https://marketplace.visualstudio.com/items?itemName=Orta.vscode-jest)
1. Style guide auto correction on save - using [prettier](https://marketplace.visualstudio.com/items?itemName=esbenp.prettier-vscode)
1. Debugging of tests - choose task "Jest Test"
1. Debug current Typescript file - choose task "Current TS File"

There is also a git hook that will ensure quality by the following means:
1. Reject code if:
    1. Compilation failed
    1. Test failed
    1. Lint failed
    1. Code coverage threshold is not high enough (can be configured in jest.config.js)
1. Automatically format code to adhere to styling code of prettier

## Usage:
Clone the repo. run "npm i"

That's it. You're ready to start developing.

## Known issues:
first time you open the project, you will have to manually choose Typescript version 3.7 via vscode. 
Unfortunately, there seems currently there is no way to [enforce Typescript workspace version](https://github.com/microsoft/vscode/issues/65546).
However, once vscode will support Typescript 3.7 out of the box this won't be necessary.

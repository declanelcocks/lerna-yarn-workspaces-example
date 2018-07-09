Lerna and Yarn Workspaces Concepts
===============

**Packages:**
- _temp-utils:_ Package containing temperature conversion utilities. Has an external dependency to `lodash`.
- _weather-app:_ A cmd-line app that uses the `temp-utils` package.

**Lerna & Yarn:**

The key to setting up a Lerna/Yarn workspace is the `lerna.json` file. This tells Lerna to use independent versions for each package and enable integration with Yarn workspaces.

After creating this file on a new project, you can run `yarn` and Yarn will analyze all your packages, download dependences from `npm` and create symlinks for internal dependencies. You'll notice that Yarn will create one global `node_modules` folder too.

Thanks to Lerna, we can also run `yarn build` and it will run this command in all packages using Babel:

```bash
lerna exec -- babel src -d dist --ignore test.js
```

Tech Stack
===============
- React
- MobX
- MobX State Router
- Material-UI

Getting Started
===============
```bash
$ yarn
$ yarn build
$ yarn start
```

Prettify the entire monorepo
===============
```bash
$ yarn format
```

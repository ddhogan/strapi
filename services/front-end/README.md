# Forum One Next.js Starter App

This is a starter app for [Next.js](https://nextjs.org/) (bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app)) that includes the following features:
* [TypeScript](https://www.typescriptlang.org/)
* [Emotion](https://emotion.sh/docs/introduction)
* [ESLint](https://eslint.org/)
* [Prettier](https://prettier.io/)

Note that Next v11 comes with the following installed already:
* [Webpack v5](https://webpack.js.org/concepts/)
* [Babel v7](https://babeljs.io/docs/en/)

## Getting Started

Ensure that you are using the proper Node version for this app. We currently use v16. Assuming you have [nvm](https://github.com/nvm-sh/nvm) installed locally, you can simply run:

```bash
nvm use
```

This will set your Node version to match the `.nvmrc` file.

To run the [development server](https://nextjs.org/docs/api-reference/cli#development):

```bash
npm run dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

## Other Commands

### Build production application

```bash
npm run build
```
Runs `next build`, which builds the production application in the `.next` folder. For more information, see the [Next.js CLI documentation](https://nextjs.org/docs/api-reference/cli#build).

### Start application in production mode

```bash
npm run start
```

Runs `next start`, which starts a Node.js server that supports [hybrid pages](https://nextjs.org/docs/basic-features/pages), serving both statically generated and server-side rendered pages. Note that `npm run build` should be ran first. For more information, see the [Next.js CLI documentation](https://nextjs.org/docs/api-reference/cli#production).

### Export application to static HTML

```bash
npm run export
```

Runs `next build && next export`. This allows you to export your app to static HTML (exported in the `out` folder), which can be run standalone without the need of a Node.js server. For more information, see the [Next.js Static HTML Export documentation](https://nextjs.org/docs/advanced-features/static-html-export).

### Run linter

```bash
npm run lint
```

Runs `next lint`, which runs the ESLint command. This is useful to catch lint errors that you might miss during development. For more information, see the [Next.js ESLint documentation](https://nextjs.org/docs/basic-features/eslint).

### Run prettier

```bash
npm run prettier
```

Runs `prettier --write`, which will find and fix all prettier issues found within the `pages` and `source` directories. Note that this will automatically overwrite your files.

### Run TypeScript compiler (tsc)

```bash
npm run tsc
```

Runs `tsc --noEmit`, which will compile the TypeScript code without emitting files. This acts as a TS error check in your CLI. This is useful to catch TS errors that you might miss during development. For more information, see the [TypeScript Compiler (tsc) documentation](https://www.typescriptlang.org/docs/handbook/compiler-options.html).

## Notes

* Code for the app is currently configured to go into the `pages` directory (for [Next.js pages](https://nextjs.org/docs/basic-features/pages)) and `source` for theming, components, providers, helpers, etc.
* Starting in Next.js v9.4, TypeScript errors do not show up in your browser when running the dev server (i.e. `npm run dev`). However, TS errors will prevent `next build` (i.e. `npm run build`) from running successfully. Be sure to run `npm run lint` and `npm run tsc` before committing and pushing code. This will give you lint and TS errors that will most likely cause your builds to fail.
  * For discussion: should we include a [TS checker in the config](https://github.com/vercel/next.js/issues/12735#issuecomment-629404102)? Note that a Next.js dev warns that [this will greatly slow development](https://github.com/vercel/next.js/issues/12735#issuecomment-629404842).
* The current favicon implementation will probably not display correctly locally in Chrome (v94), but does display correctly in Firefox and Safari. Note that the favicon _does_ display correctly once deployed. Not sure why.
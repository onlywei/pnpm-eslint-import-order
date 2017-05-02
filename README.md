The purpose of this repository is to serve as a reproducible test case for a specific interaction
between `pnpm@0.66.2` and `eslint-plugin-import@2.2.0`. To see the failure in action, follow these
instructions:

1. Clone this repo.
2. Execute `npm install` inside the repo directory.
3. Execute `npm run test` and notice that there is nothing wrong.
4. Now, reset the repo: `rm -rf node_modules/`
5. This time, execute `pnpm install`
6. Execute `pnpm run test`.
7. Notice we have the error:
```
 1:1  error  Resolve error: unable to load resolver "node"  import/order
```

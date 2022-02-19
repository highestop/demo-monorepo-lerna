# demo-monorepo

```
yarn install

yarn add lerna -W
yarn lerna init
yarn lerna bootstrap --npm-client yarn --use-workspaces

yarn lerna create app
yarn lerna create demo

yarn add typescript -W
yarn workspace @monorepo/app add typescript@4.3.5 --dev
yarn workspace @monorepo/demo add jest
yarn workspace @monorepo/demo add @types/jest --dev

yarn workspaces info
(cd packages/project-app && yarn why typescript)

yarn lerna run build --stream --sort
yarn workspaces run build

yarn lerna version
yarn lerna publish

yarn lerna clean
yarn workspaces run clean
```
# Monorepo | yarn + lerna

## Init yarn workspaces

### Step1

init project via `yarn init`

### Step2

make `packages` folder and make some diff dir in it

just like

```text
|- packages
|--- common
|--- server
```

better write some demo code to reference the other package(remind to change the `package.json` dependencies)

// the `@hdemo` is custom name by your prefer

```json
{
  "dependencies": {
    "@hdemo/common": "0.0.1"
  }
}
```

### Step3

change the root `package.json`, add `workspaces` field and set `private` to `true`

```json
{
  "private": true,
  "workspaces": [
    "packages/*"
  ],
}
```

### Step4

run `yarn install` or `yarn` in the project root

## add Lerna

```shell
npx lerna init
```

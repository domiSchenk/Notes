

# PNPM

## Fast CLI
=> pnpx 

## Commands
### Add
| npm command     | pnpm equivalent  |
| --------------- | ---------------- |
| `npm install`   | `pnpm install`   |
| `npm i <pkg>`   | `pnpm add <pkg>` |
| `npm run <cmd>` | `pnpm <cmd>`     |


| Command              | Meaning                        |     |
| -------------------- | ------------------------------ | --- |
| `pnpm add sax`       | Save to `dependencies`         |     |
| `pnpm add -D sax`    | Save to `devDependencies`      |     |
| `pnpm add -O sax`    | Save to `optionalDependencies` |     |
| `pnpm add sax@next`  | Install from the `next` tag    |     |
| `pnpm add sax@3.0.0` | Specify version `3.0.0`        |     |

### Update
  
| Command               | Meaning                                                                  |
| --------------------- | ------------------------------------------------------------------------ |
| `pnpm up`             | Updates all dependencies, adhering to ranges specified in `package.json` |
| `pnpm up --latest`    | Updates all dependencies, ignoring ranges specified in `package.json`    |
| `pnpm up foo@2`       | Updates `foo` to the latest version on v2                                |
| `pnpm up "@babel/\*"` | Updates all dependencies under the `@babel` scope                        |

#### Interactive
`--interactive, -i`


### Remove
Aliases: rm, uninstall, un

Removes packages from `node_modules` and from the project's `package.json`.


#### Options

##### --recursive, -r
When used inside a workspace, removes a dependency (or dependencies) from every workspace package.

When used not inside a workspace, removes a dependency (or dependencies) from
every package found in subdirectories.

##### --global
Remove a global package.

##### --save-dev, -D
Only remove the dependency from `devDependencies`.

##### --save-optional, -O
Only remove the dependency from `optionalDependencies`.

##### --save-prod, -P
Only remove the dependency from `dependencies`.

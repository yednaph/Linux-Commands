Search for a command
=============================
This repository is forked from <https://github.com/cheat/cheatsheets>. You may refer
to the original one.

### Access cheat from your browser
Visit <https://pranabdas.github.io/cheatsheets/>

### Update the react app
```js
npx npm-check-updates --target minor
npx npm-check-updates --upgrade --target minor
```

### Install cheat
```sh
pip3 install cheat
```

Then look for cheat directories and put the cheatsheets there: 
```sh
cheat -d
```
### Format ###
Cheatsheets are plain-text files that begin with an optional "front matter"
header in YAML format. The header may be used to assign "tags" to a sheet, and
to specify the sheet's syntax (`bash`, `python`, `go`, etc).

When possible, cheatsheets should conform to this format:

```sh
---
syntax: bash
tags: [ vcs, development ]
---
# To stage all changes in the current directory:
git add --all

# To commit staged changes:
git commit -m <message>
```

As a guideline, it is preferred to use [docopt][] syntax when specifying
parameter placeholders. In edge-cases where that syntax may cause confusion, it
is permissible to use placeholder values (`foo.txt`, `example.com`, etc.) as necessary.

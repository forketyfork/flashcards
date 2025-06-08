START
Basic
Front: 
How to check for outdated packages in yarn and update them?
Back: 
To check for outdated packages in yarn:
```shell
yarn outdated
```

To update a particular package:
```shell
yarn upgrade esbuild
```

This will only upgrade the package within the range defined in `package.json`. If you need to update it to the latest, do the following:

```shell
yarn add esbuild@latest
# or, for devDependencies:
yarn add -D esbuild@latest
```
END

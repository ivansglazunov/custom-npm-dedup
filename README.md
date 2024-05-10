Returns json with:

```
{
    [duplicatedPackageName]: [
        ...
        {
            parent: parentPackageNameWhereIdDuplicated,
            version: versionOfDuplicatedPackageInParentPackage
        },
    ],
}
```

How to use

```
npx --yes custom-npm-dedup
ONLYP='@deep' IGNOREP='["@deep-foundation/deeplinks"]' npx --yes custom-npm-dedup
```

Envs

```
ONLYP='@deep' # ignore duplicated packages in parents names not contains substring @deep
IGNOREP='["@deep-foundation/deeplinks"]' # full ignore parent names
```
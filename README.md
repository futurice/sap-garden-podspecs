# sap-garden-podspecs

A collection of pod specs for private and forked pods.

### How to support additional Gigya Pod versions

1. Under `Specs/Gigya/` add a folder of the version number that should be added.
1. Within the created folder create a new file `Gigya.podspec.json`. Use (copy-paste) the original podspec file from https://github.com/CocoaPods/Specs/tree/master/Specs/f/e/c/Gigya as a basis and adjust the attributes `source.tag` and `source.branch`, e.g.

```
"source": {
    "git": "https://github.com/futurice/gigya-swift-sdk.git",
    "branch": "fix/reflection-with-custom-module-name-v[VERSION_NUMBER]"
}
```

1. In the project `https://github.com/futurice/gigya-swift-sdk` checkout the tag `chore/v[VERSION_NUMBER]`.
1. Create a new branch e.g. `fix/reflection-with-custom-module-name-v[VERSION_NUMBER]`
1. Cherry pick all commits that adjust the Gigya Pod (e.g. commit 6d267ac9d285d7f533a3bd0be6eb33e54eb3187b)
1. Push the branch

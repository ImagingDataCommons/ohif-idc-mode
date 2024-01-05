# IDC Mode

This mode adds the following functionalities to OHIF viewer:
- Automatic loading of the latest derived display set of active series (no need to double-click the derived display set thumbnail in the left panel)

## Using mode
- Update OHIF's app package.json file to include this mode as a dependency, pointing to a branch since this mode is not being published to NPM
```js 
# platform/app/package.json
  "dependencies": {
    "ohif-idc-mode": "https://github.com/ImagingDataCommons/ohif-idc-mode#main-1.0.3",
    ...
```

- Update OHIF's plugin file to load this mode (version here does not matter since we are using a branch name to define this mode dependency instead of npm publishing)
```js
# platform/app/pluginConfig.json
 "modes": [
    ...
    {
      "packageName": "ohif-idc-mode",
      "version": "0.0.1"
    },
   ...
```

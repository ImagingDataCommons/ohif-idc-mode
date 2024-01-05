# GCP Mode

This mode adds the following functionalities to your OHIF viewer fork:
- Automatic load of the latest derived display set of active series (no need to double-click the derived display set (e.g. SRs, SEGs) thumbnail in the left panel to render a derived display set)

## Adding the mode to your OHIF fork
1. Update OHIF's app package.json file to include this mode as a dependency, pointing to a branch since this mode is not being published to NPM:
```js
/** File: platform/app/package.json */

"dependencies": {
  "ohif-idc-mode": "https://github.com/ImagingDataCommons/ohif-idc-mode#main", /** You can use any valid branch name here (#main or #master or #your-branch) */
  ...
```

2. Update OHIF's plugin file to load this mode:
```js
/** File: platform/app/pluginConfig.json */

"modes": [
  ...
  {
    "packageName": "ohif-idc-mode",
    "version": "0.0.1" /** The version here does not matter since we are using a branch name to define this mode dependency instead of npm publishing */
  },
 ...
```

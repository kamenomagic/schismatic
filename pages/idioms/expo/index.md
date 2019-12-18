---
layout: page
title: Expo
---

## Icons:
[Shown below: https://expo.github.io/vector-icons/](https://expo.github.io/vector-icons/)
<iframe width="100%" height="500px" src="https://expo.github.io/vector-icons/" frameborder="0"
allowfullscreen></iframe>


## Clearing the entire cache:
[Random forum that these directions are from:
https://forums.expo.io/t/how-to-clear-the-react-native-packager/1352](https://forums.expo.io/t/how-to-clear-the-react-native-packager/1352)

These instructions are for macOS and Linux, but the general ideas apply to Windows as well.

1. Stop XDE/exp, which should also stop the packager. Check your list of running processes to ensure these processes
are not running.
2. Delete node\_modules in your project
3. If your project depends on other local projects (e.g. has a file: URI in its dependencies), clear those local
project’s node\_modules directories too for good measure even though it’s probably unnecessary.
4. Clear your Yarn or npm cache, depending on which you’re using, with yarn cache clean or npm cache clean
5. Run yarn or npm i to install your dependencies again
6. Run watchman watch-del-all to clear Watchman’s state
7. Kill the watchman daemon process
8. Delete the packager’s cache directory with rm -fr $TMPDIR/metro\*
9. Start XDE or exp (With exp, run exp r -c for good measure
10. And just to be sure, force quit the Expo client on your phone or simulator and re-open it.

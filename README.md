# Chromium patches from Kiwi Browser, ported to an actual Chromium source

Assembled from [Kiwi Patches](https://github.com/kiwibrowser/patches), [Kiwi Source](https://github.com/kiwibrowser/src) and a few hours of my life.

How to use:
* Get [Chromium source](https://chromium.googlesource.com/chromium/src/+/master/docs/android_build_instructions.md#Updating-your-checkout)
* Switch to the supported version (corresponding to a git tag)
* Build, using gn flags from `GN_FLAGS` file

Options:
* with plugins flag (some parts are heavily patched)
* without plugins flag (according to Kiwi devs it may be broken because `extension && (~plugins)` combination is not supported by Google

Works:
* compilation
* browser startup (release builds only)
* browser (at least sites tested)
* Chrome Web Store (it does not report success for the first installed extension)
* `chrome://extensions`
* uBlock Origin (partially)
* uMatrix (partially)
* Dark Reader

Does not work:
* anything (debug builds)
* element picking in UBO
* page refresh from UBO
* extension sideloading :(

Not tested:
* anything else

Copyright:

These patches are free software and are licensed under terms of GNU General Public License, Version 3.
A copy of the license should be present in the repository. [LICENSE](LICENSE)

Some code under [BSD-style license](https://github.com/kiwibrowser/src/blob/10b24a37e87cadcce2f5c18e85723ccc7359c1c6/LICENSE) from Chromium and Kiwi is used.

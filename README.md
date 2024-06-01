This repository is used to build Simutrans for Steam. The process is quite simple:

1. Change the revision number in revision.txt
2. Commit & push
3. Wait for the pipelines to build the revision

The builds are updated and deployed to Steam every night automatically, or manually if it is a release, making use of the [simutrans-deploy](https://github.com/simutrans/simutrans-deploy) helper scripts.

The pipelines to build Simutrans for Steam are very similar to those of the GitHub mirror of Simutrans. The key differences are:

* They fetch Simutrans from the SVN. There's no Simutrans code in this repository.
* They use the CMake option -DSIMUTRANS_STEAM_BUILT, which makes the build to link against the Steam SDK included in this repository.
* The Windows builds are dinamically compiled and fluidsynth-powered.
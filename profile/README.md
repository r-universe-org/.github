# R-universe infrastructure code

This organization holds all infrastructure code used to run [r-universe.dev](https://r-universe.dev). Here you can find:

 - [`/help`](https://github.com/r-universe-org/help): central [issue tracker](https://github.com/r-universe-org/help/issues) and [discussion](https://github.com/r-universe-org/help/discussions) forum.
 - [`/frontend`](https://github.com/r-universe-org/frontend): the central server that runs r-universe.dev. It consists of express/mongodb stack that stores all R packages and metadata in a database, and renders the frontend, cran-like repos, etc.
 - [`/workflows`](https://github.com/r-universe-org/workflows): reusable GHA workflows that get triggered in the [monorepos](https://github.com/r-universe) to sync and build R packages.
 - [`/actions`](https://github.com/r-universe-org/actions): scripts used by the [build workflow](https://github.com/r-universe-org/workflows/blob/v1/.github/workflows/build.yml) to prepare, build, and check packages on all platforms.
 - [`/base-image`](https://github.com/r-universe-org/base-image): docker image (with sysdeps) used to build packages on Linux, including the initial source package.
 - [`/build-source`](https://github.com/r-universe-org/build-source) the action used by the [build workflow](https://github.com/r-universe-org/workflows/blob/v1/.github/workflows/build.yml) to build an R source package from an upstream git repo.
 - [`/cran-to-git`](https://github.com/r-universe-org/cran-to-git): where we keep track of the upstream git home for CRAN packages as guessed by our [cranscraper](https://github.com/r-universe-org/cranscraper).
 - [`/build-wasm`](https://github.com/r-universe-org/build-wasm): container action that the build workflow uses for WebAssembly binaries.
 - [`/sync`](https://github.com/r-universe-org/sync): action used by the [sync workflow](https://github.com/r-universe-org/workflows/blob/v1/.github/workflows/sync.yml) to update packages submodules in the [monorepos](https://github.com/r-universe).
 - [`/macos-libs`](https://github.com/r-universe-org/macos-libs) a bundle with MacOS system libraries copied from [mac.r-project.org](https://mac.r-project.org/bin/darwin20/). These libraries are the same as used by CRAN and are automatically available when packages get built for MacOS on r-universe.
 - [`/docs`](https://github.com/r-universe-org/docs): source code for the quarto [documentation](https://docs.r-universe.dev/) site.


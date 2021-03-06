---
title: Native Quickstart
---

##  [esy](http://esy.sh)

Esy (pronounced "easy") is a package manager for native Reason applications. It allows you to consume opam packages, and publish your own native packages to npm.

**Install esy:**

```sh
npm install -g esy
```

> **Note:** Make sure you have the latest `esy` installed. If in doubt, run `npm remove -g esy && npm install -g esy@latest`.

**Using esy:**

Clone any esy project and run the `esy` command inside of it. This will install all dependencies and build everything.

```
git clone git@github.com:esy-ocaml/hello-reason.git
cd hello-reason
esy
```

**Adding dependencies:**

To add native Reason packages that happen to be hosted on npm, run `esy add npm-package-name`.

```
esy add refmterr
```

**Opam integration:**

`esy` treats the npm scope `@opam` specially. `esy` will install any package name with the `@opam` scope directly from [opam](https://opam.ocaml.org/packages/). This is the only scope with special meaning. All other package names are assumed to be hosted on npm.

```
esy add @opam/bos
```

**Advanced esy configuration:**

See the [configuration](https://esy.sh/docs/en/configuration.html) section from the complete `esy` docs.

**Editor support:**

See the [native project](https://reasonml.github.io/docs/en/editor-plugins#native-project-development-community-supported) section of the Reason editor support doc.

**Compatibility:**

In addition to supporting `esy` specific packages hosted on npm, `esy` also supports any opam package or ocaml native compiler. It [can also be used](https://esy.sh/docs/en/node-compatibility.html) to develop JavaScript npm projects that are compatible with [Yarn Plug'n'Play](https://yarnpkg.com/lang/en/docs/pnp/) (that includes most JS projects). [This Github issue](https://github.com/BuckleScript/bucklescript/issues/3276) is tracking the required bucklescript features to enable support for managing BuckleScript projects using `esy`.

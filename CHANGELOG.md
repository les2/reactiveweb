# Changelog
## Release (2024-01-16)

reactiveweb 1.1.1 (patch)

#### :bug: Bug Fix
* `reactiveweb`, `test-app`
  * [#57](https://github.com/universal-ember/reactiveweb/pull/57) docs: correct import lines in code example ([@Techn1x](https://github.com/Techn1x))

#### Committers: 1
- Brad Overton ([@Techn1x](https://github.com/Techn1x))
## Release (2024-01-13)

reactiveweb 1.1.0 (minor)

#### :rocket: Enhancement
* `reactiveweb`, `test-app`
  * [#45](https://github.com/universal-ember/reactiveweb/pull/45) Migrate `trackedTask`'s implementation to use function-based resources ([@NullVoxPopuli](https://github.com/NullVoxPopuli))
  * [#55](https://github.com/universal-ember/reactiveweb/pull/55) Update the service implementation to not require knowledge of a specific class-based resource implementation ([@NullVoxPopuli](https://github.com/NullVoxPopuli))
  * [#54](https://github.com/universal-ember/reactiveweb/pull/54) Refactor the map util to not be a resource, it never needed to be ([@NullVoxPopuli](https://github.com/NullVoxPopuli))

#### :bug: Bug Fix
* `reactiveweb`
  * [#50](https://github.com/universal-ember/reactiveweb/pull/50) Fix in-editor docs ([@NullVoxPopuli](https://github.com/NullVoxPopuli))

#### :house: Internal
* `reactiveweb`, `test-app`
  * [#56](https://github.com/universal-ember/reactiveweb/pull/56) Upgrade eslint-plugin-ember ([@NullVoxPopuli](https://github.com/NullVoxPopuli))
* `reactiveweb`
  * [#53](https://github.com/universal-ember/reactiveweb/pull/53) Update compilation tools, now using decorator-transforms ([@NullVoxPopuli](https://github.com/NullVoxPopuli))
* `test-app`
  * [#52](https://github.com/universal-ember/reactiveweb/pull/52) Upgrade test-apps to ember-resources@6.5.1 to test against deprecations ([@NullVoxPopuli](https://github.com/NullVoxPopuli))
  * [#51](https://github.com/universal-ember/reactiveweb/pull/51) Use correct import paths ([@NullVoxPopuli](https://github.com/NullVoxPopuli))

#### Committers: 1
- [@NullVoxPopuli](https://github.com/NullVoxPopuli)
## Release (2024-01-09)

reactiveweb 1.0.0 (major)

#### :boom: Breaking Change
* `reactiveweb`
  * [#42](https://github.com/universal-ember/reactiveweb/pull/42) Change the description of the npm package ([@NullVoxPopuli](https://github.com/NullVoxPopuli))

#### :rocket: Enhancement
* `reactiveweb`, `test-app`
  * [#39](https://github.com/universal-ember/reactiveweb/pull/39) Copy alternate `modifier` and `service` implementations from ember-resources ([@NullVoxPopuli](https://github.com/NullVoxPopuli))
  * [#36](https://github.com/universal-ember/reactiveweb/pull/36) Add `@link` ([@NullVoxPopuli](https://github.com/NullVoxPopuli))
  * [#34](https://github.com/universal-ember/reactiveweb/pull/34) Add sync ([@NullVoxPopuli](https://github.com/NullVoxPopuli))
  * [#31](https://github.com/universal-ember/reactiveweb/pull/31) Add the helper from ember-resources ([@NullVoxPopuli](https://github.com/NullVoxPopuli))
* `reactiveweb`
  * [#35](https://github.com/universal-ember/reactiveweb/pull/35) Widen the ember-source peerDep to >= 3.28 ([@NullVoxPopuli](https://github.com/NullVoxPopuli))

#### :bug: Bug Fix
* `reactiveweb`
  * [#43](https://github.com/universal-ember/reactiveweb/pull/43) Fix import paths in inline docs ([@NullVoxPopuli](https://github.com/NullVoxPopuli))
  * [#33](https://github.com/universal-ember/reactiveweb/pull/33) Remove note from ember-resources in the helper jsdoc ([@NullVoxPopuli](https://github.com/NullVoxPopuli))
  * [#30](https://github.com/universal-ember/reactiveweb/pull/30) Fix typo in ember-concurrency docs ([@NullVoxPopuli](https://github.com/NullVoxPopuli))
* `reactiveweb`, `test-app`
  * [#32](https://github.com/universal-ember/reactiveweb/pull/32) Fix issue with initial values in `keepLatest` and clarify behavior ([@NullVoxPopuli](https://github.com/NullVoxPopuli))

#### :memo: Documentation
* `docs`
  * [#41](https://github.com/universal-ember/reactiveweb/pull/41) Add multiple entrypoints to the api docs ([@NullVoxPopuli](https://github.com/NullVoxPopuli))

#### :house: Internal
* `reactiveweb`, `test-app`
  * [#44](https://github.com/universal-ember/reactiveweb/pull/44) Do not allow deprecations to exist ([@NullVoxPopuli](https://github.com/NullVoxPopuli))
* `test-app`
  * [#40](https://github.com/universal-ember/reactiveweb/pull/40) Split test apps into separate CI jobs. ([@NullVoxPopuli](https://github.com/NullVoxPopuli))
  * [#29](https://github.com/universal-ember/reactiveweb/pull/29) Setup glint in test app ([@NullVoxPopuli](https://github.com/NullVoxPopuli))
  * [#26](https://github.com/universal-ember/reactiveweb/pull/26) Setup release-plan ([@NullVoxPopuli](https://github.com/NullVoxPopuli))
* Other
  * [#37](https://github.com/universal-ember/reactiveweb/pull/37) CI: use --ignore-scripts during the setup job ([@NullVoxPopuli](https://github.com/NullVoxPopuli))

#### Committers: 1
- [@NullVoxPopuli](https://github.com/NullVoxPopuli)

## 0.1.1

### Patch Changes

- 72d6797: Add support for ember-source 3.28 and 5.4

## 0.1.0

### Minor Changes

- d3f5ea4: Copy utilities from ember-resources -- no other changes to the utilities.
  The ember-resources utilities/examples will be be deprecated and removed in a major release.
  However, the migration path is a find and replace:

  Find:

  ```
  'ember-resources/util/
  ```

  Replace:

  ```
  'reactiveweb/
  ```

  Of note:

  - `trackedTask` no longer will support ember-concurrency@v2, so if you need ember-concurrency@v2, it'll be safer to stick with the `trackedTask` from ember-resources@v6.
  - `helper` has been removed, as it's had basically no usage, and wasn't all that useful anyway -- if folks still need the behavior, they can use `invokeHelper` directly.

### Patch Changes

- 881b791: Rename to reactiveweb

## 0.0.3

### Patch Changes

- ee946b1: Fix types

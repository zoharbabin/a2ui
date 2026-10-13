## Unreleased

- The data transformation functions (`jmespath`, `split`, `regexCapture`, `regexReplace`, `updateDataModel`) are no longer part of the package or of the v1 catalog schema. Hosts that need them register their own; the repository's filesystem community sample carries an implementation. [#3171](https://github.com/a2ui-project/a2ui/pull/3171)

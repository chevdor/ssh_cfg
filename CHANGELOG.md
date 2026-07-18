# Changelog

## 0.4.0 (2026-07-18)

First release of the `chevdor` fork, published on crates.io as `ssh_cnfg`
(the library import name remains `ssh_cfg`).

### Added

* `SshSection` to switch between different kinds of SSH sections. ([#3], [#4])
* Parse top-level `Include` and `Match` directives (outside a `Host` block).

### Changes

* ***Breaking:*** `SshHostConfig` renamed to `SshSectionConfig`.
* ***Breaking:*** `SshConfig` stores `IndexMap<SshSection, _>` instead of `IndexMap<String, _>`.
* ***Breaking:*** `Error::SshOptionBeforeHost` renamed to `Error::SshOptionBeforeHostOrMatch`.
* The example no longer mislabels the first section as a `Host`.
* Updated to edition 2021 and refreshed dependencies (`async-fs` 2, `dirs` 6, `indexmap` 2).

[#3]: https://github.com/azriel91/ssh_cfg/issues/3
[#4]: https://github.com/azriel91/ssh_cfg/pull/4


## 0.3.0

### Added

* Support parsing SSH configuration files with only `Host` configurations.


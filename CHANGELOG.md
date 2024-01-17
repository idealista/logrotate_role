# Change Log

All notable changes to this project will be documented in this file.
This project adheres to [Semantic Versioning](http://semver.org/) and [Keep a changelog](https://github.com/olivierlacan/keep-a-changelog).

## Added
- *[PLATFORM-3582]- Add ".gitattributes" file for linguist detection.* @ygomezsaiz

## [Unreleased](https://github.com/idealista/logrotate_role/tree/develop)

<!-- ### Fixed

### Added

### Changed

### Removed -->

## [3.0.2](https://github.com/idealista/logrotate_role/tree/3.0.2)

### Fixed

- Change molecule priviliged to false

### Added

- Add Debian 11 bullseye support
- Dockerfiles update to accomodate Debian 11

### Changed

- Update .ansible-lint
- Update .yamllint
- Update .travis.yml dist
- Add scenarios for bullseye
- Upgrade test requirements and pipfile
- Update molecule.yml for different scenarios
- Update some verify tasks

### Removed

## [3.0.1](https://github.com/idealista/logrotate_role/tree/3.0.1)
### Fixed

- *[#4](https://github.com/idealista/logrotate_role/issues/4) [BUG] Error in logrotate installation on Debian 10* @emepege
## [3.0.0](https://github.com/idealista/logrotate_role/tree/3.0.0)
### Added

- *[#1](https://github.com/idealista/logrotate_role/issues/1) [SUPPORT] Logrotate in Debian 10 (Buster)* @emepege

## [2.0.0]

### Changed

- *Cleanup of legacy stuff. Upgraded to molecule 3.0, goss 0.13, etc*

## [1.0.0]

### Added

- *First release*

[Unreleased]: http://git/projects/AS/repos/logrotate_role/compare/commits?targetBranch=refs/heads/master&sourceBranch=refs/heads/develop
[1.0.0]: http://git/projects/AS/repos/logrotate_role/compare/commits?sourceBranch=refs/tags/1.0.0&targetBranch=refs/tags/1.0.0

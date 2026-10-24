## [unreleased]

- **CHANGED**: Updated the Zebra 3 skill guide for releases 3.0.1 and 3.0.2: added a version note and a section on post-beta changes (Controls A–D macros stored in presets, MSEG global trigger, MPE smoothing, lifted FMO and envelope modulation limits), corrected modulation-source index 14 to `Voice Index` per a rev 20399 preset, and added an editing rule to resolve source indexes from each file's own `#ms=` list

## [1.2.0]

- **FIXED**: CLI startup and config parsing by centralizing the yargs parser, handling numeric overrides consistently, and using a dedicated direct-execution helper for the CLI entrypoint
- **FIXED**: WSL preset detection now checks per-user Windows u-he preset roots under `/mnt/c/Users`
- **FIXED**: Preset library loading now stays within explicit preset directories instead of accidentally pulling `.h2p` files from unrelated folders such as `Modules`
- **CHANGED**: `scripts/compact-params-model.mjs` now produces both `tmp/paramsModel.compact.json` and `tmp/paramsModel.compact.min.json` with more aggressive model compaction
- **CHANGED**: Reworked the Zebra 3 skill documentation with manual-grounded module guidance, parameter norms from `tmp/paramsModel.compact.json`, stronger sound-design hints, and leaner Markdown formatting
- **FIXED**: narrowDownByAuthor function: Removed the incorrect `!el.categories.length` check that was preventing presets without categories from being included when they had author metadata
- **FIXED**: The narrowDownByFavoritesFile function was returning all presets when a favorites file wasn't found, instead of an empty array. This was dangerous behavior that could silently include unintended presets.

## [1.1.2]

- Added documentation skill and command
- Cleaned up code around user third party
- Added user third party support
- Analyzed and improved preset randomization logic
- Migrated from simple-git-hooks to lefthook

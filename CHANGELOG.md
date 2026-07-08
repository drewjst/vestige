# Changelog

## [0.2.0](https://github.com/drewjst/vestige/compare/vestige-web-v0.1.0...vestige-web-v0.2.0) (2026-07-08)


### Features

* add events filter panel shell (no filtering logic yet) ([735cf35](https://github.com/drewjst/vestige/commit/735cf35e97c01f21020a2361af21d116159cf1fd))
* add filter reset control ([aee3e1d](https://github.com/drewjst/vestige/commit/aee3e1df65c776b8707712aff0a343d01082ac13))
* light theme toggle with persistence ([63697f5](https://github.com/drewjst/vestige/commit/63697f5f57a50332023ed326b6327ddb83238392))
* preconnect hints, esc/click-away panel dismissal, honest loading state ([e44ffac](https://github.com/drewjst/vestige/commit/e44ffac2d12d44a5697f7bf605fce3ff0582263c))
* theme tokens + themed map layer factory ([add4128](https://github.com/drewjst/vestige/commit/add4128cb30afdc4a667d2a99f784bc7d31b54d5))
* wire hazard-type filter to the map ([90665e0](https://github.com/drewjst/vestige/commit/90665e0f4a936c672cefb9b2dc75415bd7050803))
* wire time-range filter to the map ([31a890e](https://github.com/drewjst/vestige/commit/31a890e939fbab730bf0f949c225b3c776b11e4c))


### Bug Fixes

* idempotent addDataLayers — stale style.load listener double-fire on recovery toggle ([543d457](https://github.com/drewjst/vestige/commit/543d4571658e4f5b8b4e3f6714db35e2ee201c6a))
* revised light beacon contrast + theme-toggle failure recovery ([78b1c49](https://github.com/drewjst/vestige/commit/78b1c49e322364003095a8b7de0f8590f073765b))
* validate events response, honest map-load failure states, guarded filters during swap ([d8f85b3](https://github.com/drewjst/vestige/commit/d8f85b344f7a91fc4c806898d7da30743f3b44e8))


### Performance Improvements

* defer MapLibre script load ([07039e0](https://github.com/drewjst/vestige/commit/07039e0d325e55b3ddb056710dfdcd5fc5a9452f))

## [0.1.0](https://github.com/drewjst/vestige/compare/vestige-web-v0.0.1...vestige-web-v0.1.0) (2026-07-07)


### Features

* county dossier + deduped county rendering ([1e69686](https://github.com/drewjst/vestige/commit/1e696860fe988ea0e85785e10de34c10eb72bf10))
* docs site (MkDocs) + Pages/deploy/release-please CI ([41c3f0a](https://github.com/drewjst/vestige/commit/41c3f0af1a7d83a081e67da11056e744eb3267a0))
* dossier shows 'record reaches back to YYYY' from record_begins ([331e435](https://github.com/drewjst/vestige/commit/331e435cc2d7e4fbe5fd2d5ee8f1e06fc8c26835))
* itemized impact dossier + county attribution layer ([90f2b6f](https://github.com/drewjst/vestige/commit/90f2b6f7e14d76e0e4308e45c02741a5b49b4177))
* landing page; move map to /app ([12a8066](https://github.com/drewjst/vestige/commit/12a80664f62909fd7c98e0617ba0fe120337fa49))
* live coverage line on landing from /api/coverage ([5e7b693](https://github.com/drewjst/vestige/commit/5e7b693f571c4e1ec28c64c5414bebee91de0b0e))
* point web at the live Cloud Run API in prod ([ecb42da](https://github.com/drewjst/vestige/commit/ecb42da008066c224e68bdf8908522e071958e53))
* real place dossier — replace invented Houston with live records ([3911e75](https://github.com/drewjst/vestige/commit/3911e757ed13a07abcf0d2b26807c33d908e03fd))

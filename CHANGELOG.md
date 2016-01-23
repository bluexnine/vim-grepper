# Change Log

All notable changes to this project will be documented in this file. (Thus, it
won't list single bugfixes or improved documentation.)

## [Unreleased]

## [1.2] - 2016-01-23

This is mainly a bugfix release and the last release before 2.0 that will bring
quite some changes.

### Changed

- The default order of the tools is this now: `['ag', 'ack', 'grep', 'findstr',
  'sift', 'pt', 'git']`. This was done because not everyone is a git nut like
  me.

## [1.1] - 2016-01-18

50 commits.

### Added
- `CHANGELOG.md` according to [keepachangelog.com](http://keepachangelog.com)
- Support for [sift](https://sift-tool.org)
- `<esc>` can be used to cancel the prompt now (in addition to `<c-c>`)
- `-grepprg` flag (allows more control about the exact command used)
- For ag versions older than 0.25, `--column --nogroup --noheading` is used
  automatically instead of `--vimgrep`
- FAQ (see `:h grepper-faq`)
- Mappings in quickfix window: `o`, `O`, `S`, `v`, `V`, `T` (see `:h
  grepper-mappings`)
- using `-dispatch` implies `-quickfix`
- The quickfix window uses the full width at the bottom of the screen. Location
  lists are opened just below their accompanying windows instead.

### Changed
- Option "open" enabled by default
- Option "switch" enabled by default
- Option "jump" disabled by default
- The "!" for :Grepper was removed. Use `:Grepper -jump` instead.
- improved vim-dispatch support
- `g:grepper.tools` had to contain executables before. It takes arbitrary names
  now.
- Never forget query when switching tools (previously we remembered the query
  only when the operator was used)

## [1.0] - 2015-12-09
First release!

[Unreleased]: https://github.com/mhinz/vim-grepper/compare/v1.2...HEAD
[1.1]: https://github.com/mhinz/vim-grepper/compare/v1.1...v1.2
[1.1]: https://github.com/mhinz/vim-grepper/compare/v1.0...v1.1
[1.0]: https://github.com/mhinz/vim-grepper/compare/8b9234f...v1.0
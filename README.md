# Homebrew Tap

This repository publishes the Homebrew formula for Agent Feed.

## Install

```sh
brew install fqmyysjjd/tap/agent-feed
```

## Upgrade

```sh
brew update
brew upgrade agent-feed
```

## Formula Source

`Formula/agent-feed.rb` installs Agent Feed from the published PyPI source
distribution. The formula should always point at an immutable PyPI `sdist` and
its matching `sha256`, not a local build artifact or a moving branch archive.

## Release Flow

The main `fqmyysjjd/agent-feed` release workflow updates this tap after a
GitHub Release publishes the package to PyPI:

```txt
GitHub Release -> PyPI publish -> update Formula/agent-feed.rb -> brew install works
```

Manual formula updates should follow the same order: wait for the PyPI package,
update the formula URL and checksum, regenerate Python resources, then validate
with Homebrew.

## Maintainer Checks

```sh
brew style fqmyysjjd/tap/agent-feed
brew install --build-from-source fqmyysjjd/tap/agent-feed
brew test fqmyysjjd/tap/agent-feed
brew audit --strict --online fqmyysjjd/tap/agent-feed
```

# SpineSkeletonDataConverterPreBuilt

Pre-built binaries auto-built from https://github.com/wang606/SpineSkeletonDataConverter

A scheduled workflow polls the upstream repo for new releases and builds Linux x64, Linux ARM64 (old GLIBC compatible) and Windows x64 binaries for each new tag, publishing them as a GitHub Release here.

## Why this repo exists

This repo exists to serve as a pre-built binary source for automation pipelines, so they don't need to build the tool from source on every run (saves time and avoids needing a build toolchain on the runner).

Each release publishes binaries with a fixed naming pattern per platform, so pipelines can fetch the right asset directly via the GitHub Releases API without guessing filenames.

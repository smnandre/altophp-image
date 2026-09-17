# Image

ALTO Image provides immutable image requests, predictable geometry, and shared
decoding for multiple outputs. Start with the common workflow, then use the
task guides or API reference as needed.

The original stays unchanged. A single source can produce several sizes through
[Image sets](image-sets.md), sharing its decoded pixels within one render batch.
Lazy requests defer pixel work until an output is requested; inspection can
project geometry first. Formats and exact behavior depend on the chosen driver.

![An 800 by 450 cover generated from the first tutorial source](assets/examples/first-cover.webp)

[Getting started](getting-started.md) with a complete, reproducible script.

## Introduction

- [Installation](installation.md)
- [Getting started](getting-started.md)

## Guides

- [Encoding](encoding.md)
- [Image sets](image-sets.md)
- [Storage](storage.md)
- [Metadata](metadata-and-safety.md)
- [Image analysis](analysis.md)
- [Command line](command-line.md)

## Operations

- [All operations](transformations.md)

## Drivers

- [Driver selection](drivers/index.md)

## Reference

- [Public API](api/index.md)
- [Core API](api/core.md)
- [Extension contracts](api/extension-contracts.md)
- [Exceptions](api/exceptions.md)

See the [security policy](https://github.com/altophp/image/blob/main/SECURITY.md)
for deployment boundaries.

## Package

- [Changelog](https://github.com/altophp/image/blob/main/CHANGELOG.md)
- [Contributing](https://github.com/altophp/image/blob/main/CONTRIBUTING.md)
- [Support](https://github.com/altophp/image/blob/main/SUPPORT.md)

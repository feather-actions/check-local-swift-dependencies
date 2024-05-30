# Check Local Swift Dependencies Action

This GitHub Action checks for local Swift package dependencies in your repository’s Package.swift files. It ensures that no local package references are present.

## Usage

Include the action in your workflow (make sure that a Swift 5.6+ toolchain is on your PATH, on macOS this should be given, but on Linux you may need to first install it e.g. using [`setup-swift`](https://github.com/fwal/setup-swift)):

```yaml
- uses: feather-actions/check-local-swift-dependencies@0.0.1
```
Full example:

```yaml
on: [push]

jobs:
  check-local-swift-dependencies:
    runs-on: macos-latest

    steps:
      - name: Checkout
        uses: actions/checkout@v4
        with:
          fetch-depth: 1
  
      - name: Check Local Swift Dependencies
        uses: feather-actions/check-local-swift-dependencies@0.0.1
```


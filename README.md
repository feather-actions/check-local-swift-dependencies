# Check Local Swift Dependencies Action

This GitHub Action checks for local Swift package dependencies in your repository’s Package.swift files. It ensures that no local package references are present.

## Usage

Include the action in your workflow.

```yaml
- uses: feather-actions/check-local-swift-dependencies@0.0.3
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
        uses: feather-actions/check-local-swift-dependencies@0.0.3
```


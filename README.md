# Setup Anchor using cargo

An optimized action for installing [Anchor](https://www.anchor-lang.com/).

## Usage

Here's an example workflow:

```yaml
name: example-workflow
on: [push]
jobs:
  run-anchor-build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v4
      # TODO: Update action name
      - uses: /setup-anchor
      - run: anchor build
        shell: bash
```

This will use the default versions of Node.js, the Solana CLI tools and Anchor, which are 22.14.0, 2.2.3, and 0.31.0 respectively. You can also configure these versions like so:

```yaml
steps:
  - uses: actions/checkout@v4
  # TODO: Update action name
  - uses: /setup-anchor
    with:
      anchor-version: '0.30.1'
      solana-cli-version: '1.18.18'
      node-version: '20.16.0'
```

## License

The scripts and documentation in this project are released under the [MIT License](LICENSE).

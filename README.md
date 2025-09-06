# Setup Rust Toolchain

Simple action for setting up Rust toolchain, with `tool_cache` respected.

## Why

Existing actions (like [this one](https://github.com/dtolnay/rust-toolchain/) or [this one](https://github.com/actions-rust-lang/setup-rust-toolchain)) don't respect the tool cache (more specifially, `${{ runner.tool_cache }}`), instead they download and install the toolchain to `$HOME` every time.

You may find this useful if you are self-hosting [Gitea Action Runners](https://docs.gitea.com/usage/actions/act-runner), which are often constrained by limited network bandwidth, etc.

## Usage

```yml
steps:
  uses: bsdayo/setup-rust@v1
  with:
    toolchain: nightly   # default to stable
```

## License

[MIT](LICENSE)

# Pop CLI

<img src=".icons/logo.jpeg"></img>

<div align="center">
  
[![Twitter URL](https://img.shields.io/twitter/follow/Pop?style=social)](https://x.com/onpopio/)
[![Twitter URL](https://img.shields.io/twitter/follow/R0GUE?style=social)](https://twitter.com/gor0gue)
[![Telegram](https://img.shields.io/badge/Telegram-gray?logo=telegram)](https://t.me/onpopio)



> An all-in-one tool for Polkadot development.

</div>




## Installation

You can install Pop CLI from [crates.io](https://crates.io/crates/pop-cli):

```shell
cargo install --force --locked pop-cli
```

You can also install Pop CLI using the [Pop CLI GitHub repo](https://github.com/r0gue-io/pop-cli):

```shell
cargo install --locked --git https://github.com/r0gue-io/pop-cli
```

> :information_source: For detailed instructions on how to install Pop CLI, please refer to our
> documentation: https://learn.onpop.io/v/cli/installing-pop-cli

### Telemetry

Pop CLI collects anonymous usage metrics to help us understand how the tool is being used and how we can improve it.
We do not collect any personal information. If you wish to disable telemetry
or read more about our telemetry practices please see
our [telemetry](crates/pop-telemetry/README.md) documentation.

## Documentation

On the [Pop Docs website](https://learn.onpop.io) you will find:
* 👉 [Get Started with Pop CLI](https://learn.onpop.io/v/cli)

## Building Pop CLI locally

Build the tool locally with all the features:

```sh
cargo build --all-features
```

Build the tool only for Parachain functionality:

```sh
cargo build --no-default-features --features parachain
```

Build the tool only for Smart Contracts functionality:

```sh
cargo build --no-default-features --features contract
```

## Testing Pop CLI

To test the tool locally. Due to the time it can take to build a Parachain or a Smart Contract, some tests have been
separated from the normal testing flow into integration tests.

Run the unit tests only:

```sh
cargo test --lib
```

To run the integration tests relating to Smart Contracts:

```sh
cargo test --test contract
```

To run the integration tests relating to Parachains:

```sh
cargo test --test parachain
```

Run all tests (unit + integration):

```sh
cargo test
```

## Acknowledgements

Pop CLI would not be possible without these awesome crates!

- Local network deployment powered by [zombienet-sdk](https://github.com/paritytech/zombienet-sdk)
- [cargo contract](https://github.com/use-ink/cargo-contract) a setup and deployment tool for developing Wasm based
  Smart Contracts via ink!

## License

The entire code within this repository is licensed under the [GPLv3](LICENSE).

Please [contact us](https://r0gue.io/contact) if you have questions about the licensing of our products.

# Block-STM

This repository implements and benchmarks **Block-STM** and other baselines for the paper [Block-STM: Scaling Blockchain Execution by Turning Ordering Curse to a Performance Blessing](https://arxiv.org/abs/2203.06871).
The implementation of Block-STM has been merged on the main branch of the Diem blockchain open source code-base, see [PR](https://github.com/diem/diem/pull/10173).

## Run Block-STM with Aptos peer-to-peer transactions:
1. `./scripts/dev_setup.sh`
2. `cd aptos-move/aptos-transaction-benchmarks/src`
3. `cargo run --release main`

Use `taskset` commands to run experiments with different threads number. Set parameters (number of accounts/transactions/warmup-runs/runs) in `aptos-move/aptos-transaction-benchmarks/src/main.rs`.

    let acts = [2, 10, 100, 1000, 10000];
    let txns = [1000, 10000];
    let num_warmups = 2;
    let num_runs = 10;

## Run sequential baseline with Aptos peer-to-peer transactions:
1. `./scripts/dev_setup.sh`
2. `cd aptos-move/aptos-transaction-benchmarks/benches`
3. `cargo bench peer_to_peer`

Set parameters (number of accounts/transactions) in `aptos-move/aptos-transaction-benchmarks/src/transactions.rs`.

    /// The number of accounts created by default.
    pub const DEFAULT_NUM_ACCOUNTS: usize = 100;

    /// The number of transactions created by default.
    pub const DEFAULT_NUM_TRANSACTIONS: usize = 1000;
    

---

<a href="https://aptos.dev">
	<img width="100%" src="./.assets/aptos_banner.png" alt="Aptos Banner" />
</a>

---

[![Aptos Rust Crate Documentation (main)](https://img.shields.io/badge/docs-main-59f)](https://aptos.github.io/aptos/)
[![License](https://img.shields.io/badge/license-Apache-green.svg)](LICENSE)
[![CircleCI](https://circleci.com/gh/aptos-labs/aptos-core/tree/main.svg?style=shield&circle-token=d248cf1c0580eb69a507a71c0d238e1eaf193767)](https://circleci.com/gh/aptos-labs/aptos-core/tree/main)
[![grcov](https://img.shields.io/badge/Coverage-grcov-green)](https://ci-artifacts.aptoslabs.com/coverage/unit-coverage/latest/index.html)
[![test history](https://img.shields.io/badge/Test-History-green)](https://ci-artifacts.aptoslabs.com/testhistory/aptos/aptos/auto/ci-test.yml/index.html)
[![Automated Issues](https://img.shields.io/github/issues-search?color=orange&label=Automated%20Issues&query=repo%3Aaptos%2Faptos%20is%3Aopen%20author%3Aapp%2Fgithub-actions)](https://github.com/aptos-labs/aptos-core/issues/created_by/app/github-actions)
[![Discord chat](https://img.shields.io/discord/945856774056083548?style=flat-square)](https://discord.gg/aptoslabs)


Aptos-core strives towards being the safest and most scalable layer one blockchain solution. Today, this powers the Aptos Devnet, tomorrow Mainnet in order to create universal and fair access to decentralized assets for billions of people.

## Getting Started

* [Aptos Labs](https://aptoslabs.com/)
* [Aptos Developer Network](https://aptos.dev)
* [Getting Started](https://aptos.dev/tutorials/getting-started)
* [Life of a Transaction](https://aptos.dev/transactions/basics-life-of-txn)
* Join us on the [Aptos Discord](https://discord.gg/aptoslabs).

## Contributing

To begin contributing, [sign the CLA](https://github.com/aptos-labs/aptos-core/tree/main/documentation/contributing). You can learn more about contributing to the Aptos project by reading our [Contribution Guide](https://github.com/aptos-labs/aptos-core/blob/main/CONTRIBUTING.md) and by viewing our [Code of Conduct](https://github.com/aptos-labs/aptos-core/blob/main/CODE_OF_CONDUCT.md).

Aptos Core is licensed as [Apache 2.0](https://github.com/aptos-labs/aptos-core/blob/main/LICENSE).

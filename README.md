# Monero

[![Language](https://img.shields.io/badge/language-C%2B%2B17-111827?style=for-the-badge)](./CMakeLists.txt)
[![Build](https://img.shields.io/badge/build-CMake-1f2937?style=for-the-badge)](./CMakeLists.txt)
[![Network](https://img.shields.io/badge/network-Monero-b45309?style=for-the-badge)](#project-scan)
[![License](https://img.shields.io/badge/license-BSD--3--Clause-374151?style=for-the-badge)](./LICENSE)

```text
Privacy-first codebase. Full node, wallet tools, and core protocol logic in one tree.
```

## Project Scan

This repository contains the Monero core source tree: the daemon, wallet CLI, wallet RPC service, tests, build tooling, and supporting docs.
It is not a thin client and not a UI wrapper. It is the main implementation layer.

| Area | Value |
| --- | --- |
| Runtime | Native binaries |
| Stack | `C++17`, `C11`, `CMake` |
| Main targets | `monerod`, `monero-wallet-cli`, `monero-wallet-rpc` |
| Core code | [`src/`](/home/frank/githubs/GITS/electrum-xmr-/src) |
| Docs and tooling | [`docs/`](/home/frank/githubs/GITS/electrum-xmr-/docs), [`contrib/`](/home/frank/githubs/GITS/electrum-xmr-/contrib), [`utils/`](/home/frank/githubs/GITS/electrum-xmr-/utils) |

## What Is Here

- `src/daemon/` for node and daemon-side logic
- `src/simplewallet/` for the command-line wallet
- `src/wallet/` for wallet internals and RPC wallet service
- `tests/` for regression and behavior coverage
- `external/` and `.gitmodules` for bundled dependency surface

## Quick Build

```bash
git submodule update --init --recursive
cmake -S . -B build
cmake --build build -j
```

## Quick Run

```bash
./build/bin/monerod
./build/bin/monero-wallet-cli
```

## Why This README Is Lean

Upstream Monero already has extensive documentation.
This front page keeps only the essentials: what the repository is, where the important code lives, and how to build it fast.

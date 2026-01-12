# Pezkuwi Solochain Template

A minimal, ready-to-use solochain template built with the **Pezkuwi SDK**. This template provides a starting point for building custom blockchains (Solochains) within the Pezkuwi ecosystem using **Bizinikiwi** (our Substrate fork) and **Pezframe**.

## 🚀 Getting Started

Follow these steps to get started with the Pezkuwi Solochain Template:

### 1. Prerequisites

Ensure you have the following installed:
- Rust (stable and nightly)
- Clang and LLVM
- Pezkuwi SDK environment (see [docs.pezkuwichain.io](https://docs.pezkuwichain.io))

### 2. Build

Build the node in release mode:

```sh
cargo build --release
```

### 3. Run

Run the temporary node in developer mode:

```sh
./target/release/pez-solochain-template-node --dev
```

This command will:
- Start a single-node development chain.
- Keep the state in a temporary directory.
- Expose RPC and WebSocket ports.

## 🏗️ Structure

This repository is structured as follows:

- **`node/`**: The blockchain node logic (CLI, RPC, Service).
- **`runtime/`**: The runtime logic, aggregating all pezpallets.
- **`pallets/`**: Custom runtime modules (Pezpallets).
    - **`template/`**: A sample pezpallet demonstrating storage, events, and errors.

## 🛠️ Customization

To customize this template:

1.  **Modify the Runtime:** Edit `runtime/src/lib.rs` to add or remove pezpallets.
2.  **Add Logic:** Modify `pallets/template/src/lib.rs` to implement your custom business logic.
3.  **Chain Spec:** Update `node/src/chain_spec.rs` to define your chain's genesis state.

## 📚 Documentation

- [Pezkuwi Documentation](https://docs.pezkuwichain.io)
- [Pezkuwi SDK Repository](https://github.com/pezkuwichain/pezkuwi-sdk)

## 📜 License

Unlicense
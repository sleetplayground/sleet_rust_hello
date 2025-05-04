# sleet_rust_hello

🦀 a near hello smart contract written in rust


---

### Build and Test

```bash
# CARGO COMMANDS
cargo check
cargo test
cargo clean

# CUSTOM SCRIPTS
./build_cargo.sh
./build_reproducible.sh
./clean.sh # Just cleans the .wasm files and the custom build directories
```

DOCKER
<br/>
check docker for latest image and to pull
<br/>
https://hub.docker.com/r/sourcescan/cargo-near/tags

TEMPLATE
```sh
cargo generate --git https://github.com/sleetplayground/sleet_rust_hello --name <new-project-name>
```


###  How to Deploy?

```bash
# Deploy to testnet
near deploy <your-account>.testnet build_near/sleet_rust_hello.wasm

# For mainnet deployment
near deploy <your-account>.near build_near/sleet_rust_hello.wasm
```

---


### Contract Methods

The smart contract provides two main methods:

- **get_greeting()**
  - Returns the current greeting stored in the contract
  - Example: Returns "Hello" by default

- **set_greeting(greeting: String)**
  - Updates the greeting stored in the contract
  - Logs the new greeting
  - Example: Can set greeting to "howdy" or any other string

These methods allow you to store and retrieve a simple greeting message on the NEAR blockchain.

```sh
near call <your-account>.near set_greeting '{"greeting":"❄️ Hello!"}' --accountId <your-account>.near

near view <your-account>.near get_greeting
```




---

copyright 2025 by sleet.near

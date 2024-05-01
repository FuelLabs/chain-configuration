# The configuration of the Ignition-dev network

## Chain config
- The initial `privileged_address` which can perform the network upgrade: 1d5adf1197c4f48dfa642261e98fcefedd2ccd805dbbd2c574ddf3ed6dc66b5a
- The public address of the authority node that produces blocks: f16d5b417b27cf129f8b770df5f77fa7b0c389e159d79cc4aa896d92d5dd9ea8
- The block gas limit is `100000000`.

### Gas costs

The gas costs was created from the [benchmarks_fuel_core_0_26_0.json](benchmarks_fuel_core_0_26_0.json) benchmark results.
The `new_storage_per_byte` is manually set to be `63`.
The `vm_initialization.gas_per_unit` is manually set to be `0`.

### State transition
The state transition bytecode from [`0.26.0` release](https://github.com/FuelLabs/fuel-core/releases/download/v0.26.0/fuel-core-0.26.0-aarch64-apple-darwin.tar.gz).
This state transition function is used for any blocks produced with the `state_transition_bytecode_version` equal to `0`.

## State config
- The `coinbase` address hard coded in the genesis contract: b8c51c5445496a8958efd56fc88dc4171d804488a114cd9512d327f371e64707
- Contains 5 wallets with fake ETHs:
  - Wallet 1: 30933b5ded63688f5ec23c0d2f5f9d1a753a7de154c348d54ff03a95114906fb
  - Wallet 2: 004595fd2cc6593b6a035959da64b833b6d7f233c2df63fc7a6b2391f4355776
  - Wallet 3: a6a654c90bbbb2cda9b6aa1fa9a9c49e0c381aa74e8b882a42fa97868ed1793f
  - Wallet 4: 6f4abcee5d1b72cf56c7cafbf0c328039887e5a9dfaee4bdb1e7c5ecab7b0de9
  - Wallet 5: fbf651f3ac57542b7baf016646b7dce0c4fdfdad0a6ef65cb699073a340377cd

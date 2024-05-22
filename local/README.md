# The configuration of the Local network

## Chain config
- The initial `privileged_address` which can perform the network upgrade:
    ```shell
    {"address":"9f0e19d6c2a6283a3222426ab2630d35516b1799b503f37b02105bebe1b8a3e9","secret":"d80a243ef91956f626d1dad2f23bdfeb73fd0b363282b1eb2227ac5964144afb","type":"block_production"}
    ```
- The public address of the authority node that produces blocks: 
    ```shell
    {"address":"e0a9fcde1b73f545252e01b30b50819eb9547d07531fa3df0385c5695736634d","secret":"4dd0cdca64ef56a01fc81891f9beb6d898f19a22b2e287bce91d807fdf46589a","type":"block_production"}
    ```
- The block gas limit is `100000000`.

### Gas costs

The gas costs was created from the [benchmarks_fuel_core_0_26_0.json](benchmarks_fuel_core_0_26_0.json) benchmark results.
The `new_storage_per_byte` is manually set to be `63`.
The `vm_initialization.gas_per_unit` is manually set to be `0`.

### State transition
The state transition bytecode from [`0.26.0` release](https://github.com/FuelLabs/fuel-core/releases/download/v0.26.0/fuel-core-0.26.0-aarch64-apple-darwin.tar.gz).
This state transition function is used for any blocks produced with the `state_transition_bytecode_version` equal to `0`.

## State config
- The `coinbase` address hard coded in the genesis contract: 
    ```shell
    {"address":"7b4b30b2437b0073e5ba5a9324cf55831d180a89f66332b541827e12e647b751","secret":"9e24cfa071f6c1c4984a17ecf18061a8d0c9c304e7dd7703788bd122bd578650","type":"block_production"}
    ```
- Contains 1 wallet with fake ETHs:
  - Wallet 1:
    ```shell
    {"address":"00fd9e57550aa0064a87b8e5fb9a7759cc74c989f3206b6760972533db41d077","secret":"9205b6c4d6408445ae5f0850c1fc07611fe0ec4fad14305a20add72931492732","type":"block_production"}
    ```
- The base asset contract source code is taken from [here](https://github.com/FuelLabs/fuel-bridge/tree/b0ebf0b01a903f1866156b7c370ff03d6fb4ec49/packages/base-asset).
  - The `ContractId` of the contract is `0x7e2becd64cd598da59b4d1064b711661898656c6b1f4918a787156b8965dc83c`.
  - The derived(`SubId` is `0000000000000000000000000000000000000000000000000000000000000000`) base `AssetId` from this contract is `0xf8f8b6283d7fa5b672b530cbb84fcccb4ff8dc40f8176ef4544ddb1f1952ad07`.

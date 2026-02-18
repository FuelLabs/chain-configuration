# The configuration of the Ignition-dev network

## Chain config
- The `ChainId` is `1119889111`.
- The initial `privileged_address` which can perform the network upgrade: b0c319eb0751b33b57e3b3fcc1a960ca5a1e239cccc1b45ce40fdae8fcb989d7
- The public address of the authority node that produces blocks: afaf07e77aab90b59556f990bf9b3dc5a242f0dac680908fec7e79bb0cdc9027
- The block gas limit is `42000000`.

### State transition
The state transition bytecode from [`0.47.1` release](https://github.com/FuelLabs/fuel-core/releases/download/v0.47.1/fuel-core-0.47.1-aarch64-apple-darwin.tar.gz).
This state transition function is used for any blocks produced with the `state_transition_bytecode_version` equal to `32` - release `0.47.1`.

## State config
- The `coinbase` address hard coded in the genesis contract: b8c51c5445496a8958efd56fc88dc4171d804488a114cd9512d327f371e64707
- Contains 5 wallets with fake ETHs:
  - Wallet 1: 30933b5ded63688f5ec23c0d2f5f9d1a753a7de154c348d54ff03a95114906fb
  - Wallet 2: 004595fd2cc6593b6a035959da64b833b6d7f233c2df63fc7a6b2391f4355776
  - Wallet 3: a6a654c90bbbb2cda9b6aa1fa9a9c49e0c381aa74e8b882a42fa97868ed1793f
  - Wallet 4: 6f4abcee5d1b72cf56c7cafbf0c328039887e5a9dfaee4bdb1e7c5ecab7b0de9
  - Wallet 5: fbf651f3ac57542b7baf016646b7dce0c4fdfdad0a6ef65cb699073a340377cd
- The base asset contract source code is taken from [here](https://github.com/FuelLabs/fuel-bridge/tree/b0ebf0b01a903f1866156b7c370ff03d6fb4ec49/packages/base-asset).
  - The `ContractId` of the contract is `0x7e2becd64cd598da59b4d1064b711661898656c6b1f4918a787156b8965dc83c`.
  - The derived(`SubId` is `0000000000000000000000000000000000000000000000000000000000000000`) base `AssetId` from this contract is `0xf8f8b6283d7fa5b672b530cbb84fcccb4ff8dc40f8176ef4544ddb1f1952ad07`.

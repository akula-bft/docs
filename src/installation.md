## Installlation
### NOTE: Unix-only

Akula **only** runs on Unix-based platforms (Linux, macOS). Do not expect any help for issues on Windows.

### Building the source

Requirements:
- libclang-dev
- pkg-config

Install `rustup` from rustup.rs.

```ignore
git clone https://github.com/akula-bft/akula

cd akula

cargo build --all --profile=production
```

You can find built binaries in `target/production` folder.

### Docker
Latest builds are available on [Docker Hub](https://hub.docker.com/repository/docker/vorot93/akula).

## Running

* `akula` is the main binary that runs as full node:

```ignore
akula --datadir=<path to Akula database directory>
```

For Beacon-based networks (Ethereum, Sepolia, Goerli) you also need to run Lighthouse:

```
git clone https://github.com/sigp/lighthouse

cargo run --release --bin lighthouse -- beacon_node --execution-endpoints=http://127.0.0.1:8551 --execution-jwt=<path to Akula database directory>/jwt.hex --checkpoint-sync-url="https://mainnet.checkpoint.sigp.io" --purge-db
```

* `akula-rpc` is the RPC daemon, which can provide JSONRPC and gRPC endpoints based on Akula's database.

* `akula-sentry` is the P2P node.

* `akula-toolbox` provides various helper commands to check and manipulate Akula's database. Please consult its help for more info:
```ignore
akula-toolbox --help
```

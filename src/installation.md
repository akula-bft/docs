## Building the source

Requirements:
- clang 12+
- libext2fs-dev / e2fsprogs-devel

Install `rustup` from rustup.rs.

```ignore
git clone https://github.com/akula-bft/akula

cd akula

cargo build --all --profile=production
```

You can find built binaries in `target/production` folder.

## Running

* `akula` is the main binary that runs as full node, requires `akula-sentry`:

```ignore
akula --datadir=<path to Akula database directory>
```

* `akula-sentry` is the P2P node.

* `akula-toolbox` provides various helper commands to check and manipulate Akula's database. Please consult its help for more info:
```ignore
akula-toolbox --help
```

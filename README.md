# nakatoshi

![](https://github.com/ndelvalle/nakatoshi/workflows/Rust/badge.svg)

A [Bitcoin Vanity Address](https://github.com/bitcoinbook/bitcoinbook/blob/develop/ch04.asciidoc#vanity-addresses) generator.

nakatoshi accepts as input a "starts with" string to search for, and produces an address and private / public keys. The amount of time required to find a given pattern depends on how long the string is, the speed of your computer, and whether you get lucky.

## Installation

```shell
$ cargo install nakatoshi
```

## Development

```shell
# Build
$ cargo build

# Run
$ cargo run

# Example using a start with string
$ cargo run 1Ki

#    Finished dev [unoptimized + debuginfo] target(s) in 0.16s
#     Running `target/debug/nakatoshi 1Ki`
#Private key:  L5cwwXrcbLLibKmPgCewh2ueGCV6nV1zm1aUFRgW5q8mg2ufdEcc
#Public key:   020e225a9d3c700a2544af1d9bd935aac380dee6c5716b19d5d26e6fe3d415310b
#Address:      1KioF2fBWMmrHZy8ctGBQgmkjpcqTw4j3c
#Time elapsed: 45.551637ms

# Help
$ cargo run -- -help
```

## TODOs

- [ ] Create a release build
- [ ] Improve API adding more options
- [ ] Add more tests
- [X] Add commandline argument for case-insensitive option (`-i`)
- [ ] Add commandline argument to keep going after finding an address (`-k`)
- [ ] Add commandline argument for saving results to file (`-o results.txt`)
- [ ] Add commandline argument for using a file as input (`-f addresses.txt`)
- [ ] Add commandline argument for Bech32 `bc1q` addresses (`-b`)
[![](https://img.shields.io/crates/v/cyborgtime-serde.svg)][crates-io]
[![](https://docs.rs/cyborgtime-serde/badge.svg)][api-docs]
[![Apache 2.0 licensed](https://img.shields.io/badge/license-Apache2.0-blue.svg)](./LICENSE-APACHE)
[![MIT licensed](https://img.shields.io/badge/license-MIT-blue.svg)](./LICENSE-MIT)

# cyborgtime-serde

Serde support for the `cyborgtime` crate.

This is the cybernetic fork of [`humantime-serde`](https://github.com/jean-airoldie/humantime-serde).

## Example
```rust
use serde::{Serialize, Deserialize};
use std::time::{Duration, SystemTime};

#[derive(Serialize, Deserialize)]
struct Foo {
    #[serde(with = "cyborgtime_serde")]
    timeout: Duration,
    #[serde(default)]
    #[serde(with = "cyborgtime_serde")]
    time: Option<SystemTime>,
}
```

## License

Licensed under either of

 * Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or http://opensource.org/licenses/MIT)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally
submitted for inclusion in the work by you, as defined in the Apache-2.0
license, shall be dual licensed as above, without any additional terms or
conditions.

[crates-io]: https://crates.io/crates/cyborgtime-serde
[api-docs]: https://docs.rs/cyborgtime-serde

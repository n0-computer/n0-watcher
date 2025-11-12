# n0-watcher

> Watchable values.

A `Watchable` exists to keep track of a value which may change over time.  It allows
observers to be notified of changes to the value.  The aim is to always be aware of the
**last** value, not to observe *every* value change.

In that way, a `Watchable` is like a `tokio::sync::broadcast::Sender`, except that there's no risk
of the channel filling up, but instead you might miss items.

See [the module documentation][https://docs.rs/n0-watcher] for more information.


## Note to Maintainers: Creating a release

- Make sure to have `git-cliff`, `cargo-release` and `cargo-semver-checks` installed.
- Figure out whether this release is major/minor/patch by running `cargo semver-checks check-release --release-type=major/minor/patch` and see which one fits
- Use `git-cliff` to generate the changelog
- Bump the version by major/minor/patch in `Cargo.toml` and create a release prep PR. Make sure to prefix the release prep PR name with `chore(release):`.
- Review and merge the PR.
- Run `cargo release` to check if the release would go through well.
- Run `cargo release --execute` to run the release


## License

Copyright 2025 N0, INC.

This project is licensed under either of

 * Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or
   http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or
   http://opensource.org/licenses/MIT)

at your option.

## Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted for inclusion in this project by you, as defined in the Apache-2.0 license, shall be dual licensed as above, without any additional terms or conditions.

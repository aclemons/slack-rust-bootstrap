slack-rust-bootstrap
====================

Bootstrap Rust on Slackware using [mrustc](https://github.com/thepowersgang/mrustc)

Until recently, the only way to bootstrap rust was to download a precompiled
rust stage0 compiler of the previous rust release and use it to compile the
current release from source.

mrustc is an alternative rust compiler written in C++ which can be used to
bootstrap rust completely from source (given you have a C++ compiler).

mrustc targets rust 1.19.0, so this script will build mrustc, use it to build a
stage0 1.19.0 rust and stdlib, use this stage0 to build 1.20.0 from source
(full-bootstrap) and using that step through each release up to the latest
release, which is currently 1.37.0.

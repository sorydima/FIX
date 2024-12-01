<div align="center">
    <h1><img width="200" height="200" src="docs/fix.svg"></h1>

[![Build Status](https://github.com/ulyssa/fix/actions/workflows/ci.yml/badge.svg)](https://github.com/ulyssa/fix/actions?query=workflow%3ACI+)
[![License: Apache 2.0](https://img.shields.io/crates/l/fix.svg?logo=apache)][crates-io-fix]
[![#fix:0x.badd.cafe](https://img.shields.io/badge/matrix-%23fix:0x.badd.cafe-blue)](https://matrix.to/#/#fix:0x.badd.cafe)
[![Latest Version](https://img.shields.io/crates/v/fix.svg?logo=rust)][crates-io-fix]
[![fix](https://snapcraft.io/fix/badge.svg)](https://snapcraft.io/fix)

![Example Usage](https://fix.chat/static/images/fix-demo.gif)

</div>

## About

`fix` is a Matrix client for the terminal that uses Vim keybindings. It includes support for:

- Threads, spaces, E2EE, and read receipts
- Image previews in terminals that support it (sixels, Kitty, and iTerm2), or using pixelated blocks for those that don't
- Notifications via terminal bell or desktop environment
- Send Markdown, HTML or plaintext messages
- Creating, joining, and leaving rooms
- Sending and accepting room invitations
- Editing, redacting, and reacting to messages
- Custom keybindings
- Multiple profiles

_You may want to [see this page as it was when the latest version was published][crates-io-fix]._

## Documentation

You can find documentation for installing, configuring, and using fix on its
website, [fix.chat].

## Configuration

You can create a basic configuration in `$CONFIG_DIR/fix/config.toml` that looks like:

```toml
[profiles."example.com"]
user_id = "@user:example.com"
```

If you homeserver is located on a different domain than the server part of the
`user_id` and you don't have a [`/.well-known`][well_known_entry] entry, then
you can explicitly specify the homeserver URL to use:

```toml
[profiles."example.com"]
url = "https://example.com"
user_id = "@user:example.com"
```

## Installation (via `crates.io`)

Install Rust (1.74.0 or above) and Cargo, and then run:

```
cargo install --locked fix
```

See [Configuration](#configuration) for getting a profile set up.

## Installation (via package managers)

### Arch Linux

On Arch Linux a [package](https://aur.archlinux.org/packages/fix-git) is available in the
Arch User Repositories (AUR). To install it simply run with your favorite AUR helper:

```
paru fix-git
```

### FreeBSD

On FreeBSD a package is available from the official repositories. To install it simply run:

```
pkg install fix
```

### macOS

On macOS a [package](https://formulae.brew.sh/formula/fix#default) is availabe in Homebrew's
repository. To install it simply run:

```
brew install fix
```

### NetBSD

On NetBSD a package is available from the official repositories. To install it simply run:

```
pkgin install fix
```

### Nix / NixOS (flake)

```
nix profile install "github:ulyssa/fix"
```

### openSUSE Tumbleweed

On openSUSE Tumbleweed a [package](https://build.opensuse.org/package/show/openSUSE:Factory/fix) is available from the official repositories. To install it simply run:

```
zypper install fix
```

### Snap

A snap for Linux distributions which [support](https://snapcraft.io/docs/installing-snapd) the packaging system.

```
snap install fix
```

## License

fix is released under the [Apache License, Version 2.0].

[Apache License, Version 2.0]: https://github.com/ulyssa/fix/blob/master/LICENSE
[crates-io-fix]: https://crates.io/crates/fix
[fix.chat]: https://fix.chat
[well_known_entry]: https://spec.matrix.org/latest/client-server-api/#getwell-knownmatrixclient

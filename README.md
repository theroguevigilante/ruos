# ruos

**ruos** is a small operating system written in Rust, inspired by the *Writing an OS in Rust* series by Philipp Oppermann. The project is in its early stages and currently focuses on booting and printing text to the screen through VGA text mode. It is intended as a learning project for exploring low-level development in Rust without relying on an existing operating system.

## Current Status

ruos currently supports:
- Booting into 64-bit long mode
- Running without the Rust standard library (`no_std` + `no_main`)
- Writing text to the screen using the VGA text buffer

## Planned Features

Future development goals include:
- Interrupt Descriptor Table (IDT) and basic interrupt handling
- Memory management and paging setup
- Keyboard input and simple drivers
- Expanded bootloader configuration and hardware access
- Initial tasking and kernel structure

## Requirements

To build and run ruos, the following dependencies are required:

- Rust nightly toolchain
- `rust-src` component
- `llvm-tools-preview` component
- `bootimage` for generating a bootable binary

Install and configure:

```bash
rustup toolchain install nightly
rustup component add rust-src --toolchain nightly
rustup component add llvm-tools-preview --toolchain nightly
cargo install bootimage

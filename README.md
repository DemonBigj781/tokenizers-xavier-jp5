# Tokenizers - Xavier JP5

This fork provides the Rust-backed tokenizer runtime used by the Xavier transformer and diffusion dependency stack.

## Role in the Xavier stack

- Targets Python 3.10 on AArch64.
- Keeps tokenizer ABI and Transformers compatibility pinned for Worker v13.
- Uses the installed Rust toolchain for reproducible native builds when needed.
- Avoids treating a desktop wheel as automatically compatible with JetPack 5.

## Project status

This is an experimental integration fork. Successful native packaging does not establish full model compatibility.

## Build discipline

Rust and native builds must use exactly one compiler worker, including `CARGO_BUILD_JOBS=1`.

## Upstream

Forked from `huggingface/tokenizers`. General Tokenizers development and documentation remain upstream.

# plugnrust

I am not affiliated with [Blue Cat Audio](https://www.bluecataudio.com), so
please report issues with this template here.

This is a rust version of the headers and reference script of [Blue Cat's Plug'n
Script](https://www.bluecataudio.com/Products/Product_PlugNScript/). I am
using this for my project, but I haven't used everything yet, so there might
still be bugs. Issues and contributions are welcome.

For documentation please consult the
[headers](https://github.com/bluecataudio/plugnscript/tree/master/NativeSource/include)
and the [reference
script](https://www.bluecataudio.com/Doc/Product_PlugNScript/#NativeReference.ScriptC).

It is not my goal to create a state of the art rust-crate, I am totally ok with
some unsafe here and there.

## Repository Status: Sharing / Inactive

This repository hosts code that I’ve chosen to share publicly for educational,
demonstration, or archival purposes. Please note the following:

- **No Active Maintenance**: This project is not actively maintained or updated.
  It serves primarily as a snapshot of a certain stage of development for those
  who might find parts of the code useful or interesting. I try to accept pull-
  request, but do not expect anything. If interest in the project increases, I
  might change the repository status.
- **No Support Provided**: As this is an inactive project, I’m unable to provide
  support, answer issues, or accommodate pull requests.
- **Use at Your Own Risk**: While you’re welcome to explore, fork, or use the
  code in your own projects, please do so with the understanding that this
  repository is provided as-is, without any guarantees on its functionality or
  security.

Feel free to explore the code and utilize it under the terms of the license
attached to this repository!

# Linking

Rust cannot create macOS shared-libraries for `dlopen` (bundles). The official way
to create bundles is to create a static-library and link it with `clang`. As I
do in the Makefile.

The makefile builds a universal (x86_64 and arm64) binary. add the other target
with:

`rustup target add x86_64-apple-darwin`

or

`rustup target add aarch64-apple-darwin`

I will look into Windows, once my project is past alpha.

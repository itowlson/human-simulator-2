# human-simulator-2

A WASM hello-world with a publish action

You will need:
* Rust: https://www.rust-lang.org/tools/install
* The `wasm32-wasi` target: `rustup target add wasm32-wasi`

To build:
* VS Code: `Run Task > Rust: Build WASM`
* Command line: `cargo build-wasm`

To run:
* VS Code: go to Run/Debug pane, select `Debug WASM` and run
* Command line: `wasmtime ./target/wasm32-wasi/debug/human-simulator-2.wasm`


## Dev releases

* **You will need the Hippo uploader to publish dev builds.** Download this from
  https://github.com/deislabs/hippofactory/releases and install on your path.

## CI releases

The release workflow depends on two variable and two secrets:

* **HIPPO_URL** (defined in .github/workflows/release.yml): the
  URL of the Hippo where you'd like to
  publish releases. We've set this up for you.
* **BINDLE_SERVICE_URL** (defined in .github/workflows/release.yml): the
  URL of the Bindle server where your Hippo server
  gets modules from. We've set this up for you.
* **HIPPO_USERNAME** (secret you need to create in GitHub): the ID
  of a user with write permissions on the Hippo service.
* **HIPPO_PASSWORD** (secret you need to create in GitHub): the
  password of the user identified in HIPPO_USERNAME.

See https://bit.ly/2ZqS3cB for more information about creating the
secrets in your GitHub repository.

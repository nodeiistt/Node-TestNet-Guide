
# Building the prover

## 1. Install Rust
DO NOT install Rust using things like apt install rust.

If rust is already installed: Make sure you have at least Rust 1.65. Check with rustc --version.

Install the latest version of Rust using rustup. Run the following line:
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```
Accept default options by pressing Enter or customize if you need to.

Log out and log in again to finish the installation, or follow the instructions by rustup.

## 2. Install dependencies
```
sudo apt update
sudo apt install git clang libssl-dev pkg-config --no-install-recommends
```
## 3. Clone and build the prover
Unless absolutely necessary, DO NOT run anything with sudo. You don't need root permission from now on.

### Clone the prover repo:
```
git clone https://github.com/HarukaMa/aleo-prover -b testnet3-new
```
```
cd aleo-prover
```
### Build the prover using cargo:
```
cargo build --release
```
####If the build successes, Run the prover:
```
Screen -S Aleo
```
```
cargo run --release -- -a aleo1your_address_here -p pool.hamp.app:4444
```

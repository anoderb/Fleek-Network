# fleek Network

# Environment

|  Component   |        Spesification          |
| ------------ | ----------------------------- |
| CPU          | Intel Core i7-8700 Hexa-Core  |
| RAM          | DDR4 64 GB                    |
| Penyimpanan  | 2x1 TB NVMe SSD               |
| koneksi      | Port 1 Gbit/dtk               |
| OS           | UBUNTU                        |


# Install dependencies

```
sudo apt update -y
sudo apt upgrade -y
sudo apt install build-essential -y
sudo apt install libssl-dev pkg-config libclang-dev -y
```

# Install Rust

```
curl https://sh.rustup.rs -sSf > RUSTUP.sh
sh RUSTUP.sh -y
rm RUSTUP.sh
source "$HOME/.cargo/env"
```

# Install sccache

```
cargo install sccache
```

# Install cmake

```
cd /tmp
```
```
wget https://github.com/Kitware/CMake/releases/download/v3.25.1/cmake-3.25.1.tar.gz
```
```
tar -xvzf cmake-3.25.1.tar.gz
```
```
cd cmake-3.25.1
```
```
./bootstrap
```
```
make
```
```
sudo make install
```

# Install Ursa

```
git clone https://github.com/fleek-network/ursa
```
```
cd ursa
```
```
make install
```
# Simple test
car file from from getting started guide
```
curl https://ipfs.io/ipfs/bafybeidqdywrzg7c3b4dmm332m4b7uiakgitplz2pep2zntederxpj3odi -o basic.car
```
```
ursa rpc put basic.car
```
```
ursa rpc get bafybeifyjj2bjhtxmp235vlfeeiy7sz6rzyx3lervfk3ap2nyn4rggqgei ./output
```

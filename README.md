

VizzoTop is a secure project aims to integrate cryptocurrencies in a real environment.




### How to install

Updating Ubuntu system
```sh
sudo apt-get update
sudo apt-get upgrade
sudo apt-get dist-upgrade
```

Installing new packages
```sh
sudo apt-get install -y build-essential libssl-dev libboost-all-dev git libdb5.3++-dev libminiupnpc-dev screen
```

Creating folder on root structure and give permission
```sh
sudo mkdir /wallets
sudo chmod 777 /wallets
```

Downloading source code
```sh
git clone https://github.com/vizzotopdev/vizzotop.git vizzotop
cd vizzotop
```

Changing permission and compiling LevelDB
```sh
cd ./src/leveldb
chmod +x build_detect_platform
make libleveldb.a libmemenv.a
cd ../..
```

Changing permission and compiling SECP256K1
```sh
cd ./src/secp256k1
chmod +x autogen.sh
./autogen.sh
./configure
make
cd ../..
```

Compiling daemon
```sh
cd ./src
make -f makefile.unix
  or
make -f makefile.unix "USE_UPNP=-" # without support to UPNP
```



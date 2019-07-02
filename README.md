Welcome to the swap-blockchain-explorer wiki!

## Swap Block Explorers (version 3):
1. https://explorer.xwp.fyi
2. https://explorer2.xwp.fyi

## **Compiling swap daemon on Ubuntu 18.04**

``sudo apt update``

``sudo apt-get install build-essential cmake pkg-config libboost-all-dev libssl-dev libzmq3-dev libunbound-dev libsodium-dev libreadline6-dev libpgm-dev libnorm-dev``

``cd ~``

``git clone --recursive https://github.com/swap-dev/swap``

``cd swap``

``USE_SINGLE_BUILDDIR=1 make -j<number of threads>``

The binaries compiled at ``~/swap/build/release/bin/``

***

## Compile and run the swapblocks

    cd ~
    git clone https://github.com/swap-dev/swap-blockchain-explorer swapblock
    cd swapblock
    mkdir build && cd build
    cmake ..
    make -j<number of threads>
    
    # run the explorer:
    ./swapblocks -x 127.0.0.1 --testnet-url https://swaptest.coinscope.cc --enable-emission-monitor --enable-autorefresh- 
    option --enable-block-cache --enable-tx-cache --enable-json-api --enable-pusher

Open explorer with your browser:
http://127.0.0.1:8081


[README_original.md](README_original.md)

# petroleum-blockchain (XPT)

![IMG_4734](https://github.com/petroleum-network/petroleum-blockchain-gui/raw/main/src/assets/img/chia_circle.png)

Petroleum(XPT) is a modern cryptocurrency built from scratch, designed to be efficient, decentralized, and secure. Here are some of the features and benefits:
* [Proof of space and time](https://docs.google.com/document/d/1tmRIb7lgi4QfKkNaxuKOBHRmwbVlGL4f7EsBDr_5xZE/edit) based consensus which allows anyone to farm with commodity hardware
* Very easy to use full node and farmer GUI and cli (thousands of nodes active on mainnet)
* Simplified UTXO based transaction model, with small on-chain state
* Lisp-style Turing-complete functional [programming language](https://chialisp.com/) for money related use cases
* BLS keys and aggregate signatures (only one signature per block)
* [Pooling protocol](https://github.com/Chia-Network/chia-blockchain/wiki/Pooling-User-Guide) that allows farmers to have control of making blocks
* Support for light clients with fast, objective syncing
* A growing community of farmers and developers around the world
* Combining Proof-of-Work and Proof-of-Stake Securely

## Installing

Please visit our wiki for more information:
[wiki](https://github.com/petroleum-network/petroleum-blockchain/wiki).

## Resource Links

[ChiaHub](https://www.chia-hub.com/)

[Chia Forks Calculator](https://chiaforkscalculator.com/)

[Chiaforks Blockchain](https://chiaforksblockchain.com/)

[TokenDock](https://tokendock.io/)

## How to staking

1. Query the staking addresses according to your farming plot list:

   ```
   $ petroleum farm summary
   ...
   Staking addresses:
     xpt1x6jjvepyvjv7395nmtywvx9mknshgy78dsmuu38m0e9grxr080nsltjugr (balance: 0, plots: 27)
   ...
   ```

2. Deposit coins to the staking address:

   ```
   $ petroleum wallet send -t xpt1x6jjvepyvjv7395nmtywvx9mknshgy78dsmuu38m0e9grxr080nsltjugr -a 1
   ```

   Wait for the transaction get confirmed, query staking balance again:

   ```
   $ petroleum farm summary
   ...
   Staking addresses:
     xpt1x6jjvepyvjv7395nmtywvx9mknshgy78dsmuu38m0e9grxr080nsltjugr (balance: 1, plots: 27)
   ...
   ```

3. Withdraw coins from the staking address:

   ```
   $ petroleum wallet send_from -s xpt1x6jjvepyvjv7395nmtywvx9mknshgy78dsmuu38m0e9grxr080nsltjugr -t $RECEIVER -a 10
   ```

   Do a transaction to transfer the coins from the staking address to any receive address.

   Make sure to choose the wallet that contains the plot farmer key.

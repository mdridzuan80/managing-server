# Setup geth private network

## Create a directory and its sub-directories

`mkdir eth-net`

To create a network with three (3) nodes, create 3 sub-directories under `eth-net`

`cd eth-net`

`mkdir node1 node2 node3`

## Create account for each node

Make sure you are in the `/eth-net` working directory.

1- Create a new account for `node1`

`geth account new --datadir node1`

2- Copy the public key into an `account` file for safe-keeping

`echo "0x..." > node1/account`

3- likewise, for password

`echo "Password123" > node1/password`

Repeat the steps 1,2 and 3 for `node2` and `node3`.

## Create a new genesis file

`puppeth`

- name the network as `genesis` or whatever you want;
- use public keys you stored in the previous [step](#create-account-for-each-node)
- you can arbitrarily choose a number for the network id, for example `2022`

## Initialise node

Change into `node1` directory

`geth init --datadir node1 genesis.json`

Then change into `node2` directory and do

`geth init --datadir node2 genesis.json`

Repeat for `node3`.

## Start the node

Change into `node1` directory, and do

```
geth --datadir . --networkid 2022 --syncmode "full" --verbosity 3 --port 30310 --http --http.addr "localhost" --http.port 8545 --http.corsdomain "*" --http.vhosts "*" --http.api "admin,eth,web3,personal,miner,net,txpool,clique" --mine --miner.gasprice "0" --allow-insecure-unlock --unlock "0x..." --password password --nat=extip:127.0.0.1
```

Change into `node2` directory, and do

```
geth --datadir . --networkid 2022 --syncmode "full" --verbosity 3 --port 30311 --http --http.addr "localhost" --http.port 8546 --authrpc.port 8552 --http.corsdomain "*" --http.vhosts "*" --http.api "admin,eth,web3,personal,miner,net,txpool,clique" --mine --miner.gasprice "0" --allow-insecure-unlock --unlock "0x..." --password password --nat=extip:127.0.0.1
```

Change into `node3` directory, and do

```
geth --datadir . --networkid 2022 --syncmode "full" --verbosity 3 --port 30312 --http --http.addr "localhost" --http.port 8547 --authrpc.port 8553 --http.corsdomain "*" --http.vhosts "*" --http.api "admin,eth,web3,personal,miner,net,txpool,clique" --mine --miner.gasprice "0" --allow-insecure-unlock --unlock "0x..." --password password --nat=extip:127.0.0.1

```

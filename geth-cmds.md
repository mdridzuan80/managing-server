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

New
```
geth --datadir node2 --networkid 31081957 --syncmode "full" --verbosity 3 --port 30314 --http --http.addr "127.0.0.1" --http.port 8546 --authrpc.port 8556 --http.corsdomain "*" --http.vhosts "*" --http.api "admin,eth,web3,personal,miner,net,txpool,clique" --mine --miner.gasprice "0" --miner.etherbase "0x41b5Ef72d94269cFd18CF712eD8c42BF82811140" --allow-insecure-unlock --unlock "0x41b5Ef72d94269cFd18CF712eD8c42BF82811140" --password node2/password --nodiscover
```

## OPTIONAL: Start node with influxdb

```
geth --datadir geth-net/node1 --networkid 2022 --syncmode "full" --verbosity 3 --port 30310 --http --http.addr "localhost" --http.port 8545 --http.corsdomain "*" --http.vhosts "*" --http.api "admin,eth,web3,personal,miner,net,txpool,clique" --mine --miner.gasprice "0" --allow-insecure-unlock --unlock "0xAe18E0CA7b92E2190C431566719417762205b623" --password geth-net/node1/password --nat=extip:127.0.0.1 --metrics --metrics.influxdbv2 --metrics.influxdb.organization thuleen --metrics.influxdb.token o0Zzfgkbww5gb5VlBGJedYDQr8gpY37TECYxtR-WujESXAZEpevk3x4jp_bGnDE-1YqUYAhQ-r3QJ4_lZkNwJQ== --metrics.influxdb.bucket geth
```

List of options that were added above were:

- `--metrics`
- `--metrics.influxdbv2`
- `--metrics.influxdb.organization`
- `--metrics.influxdb.token`
- `--metrics.influxdb.bucket`

> Replace the value for `metrics.influxdb.token` option with your token value. If you lost it you can create it in the Influxdb WebUI at `localhost:8086`.

## Attach JS console to the nodes

Change into `node1` directory

`cd node1`

then,

`geth attach --datadir .`

Open a new terminal and repeat for each node.

## Get the `enode` value

In the JS console, do

`admin.nodeInfo.enode`

Repeat for each node.

## Add peers to a node

For example for `node1`, in its JS console do,

```
admin.addPeer("<enode_node2>")
```

```
admin.addPeer("<enode_node3>")
```

## Transfer fund to an account via geth ipc console

```
geth --datadir . attach geth.ipc
```

```
eth.sendTransaction({from: "0x_node_1_account",to: "0x_poor_thing_account", value: "100000000000000000"})
```

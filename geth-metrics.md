# Geth dashboard 

There are five (5) sections of geth dashboard. Each section have their respective panels and each panel have their respective meansurement(s). Each measurement is associated with a field, for example `value`, or `mean` or `m1` or `count`.

1. [System](#system)
2. [Network](#network)
3. [Blockchain](#blockchain)
4. [Database](#database)
5. [Light server](#light-server)

## System

### CPU

| Measurement | Field |
|-------------|-------|
|geth.system/cpu/sysload.gauge | value |
|geth.system/cpu/sysload.gauge | value |
|geth.system/cpu/procload.gauge| value |

### Memory

| Measurement | Field |
|-------------|-------|
|geth.system/memory/allocs.meter| mean |
|geth.system/memory/used.gauge| mean |
|geth.system/memory/held.gauge| mean |

### Disk

## Network

### Traffic
### Peers
### Ingress data rate
### Egress data rate
### Ingress traffic
### Egress traffic

## Blockchain

### Data rate

```
geth.p2p/ingress/eth/63/0x00.meter
geth.p2p/ingress/eth/64/0x00.meter
geth.p2p/ingress/eth/65/0x00.meter
geth.p2p/ingress/eth/63/0x01.meter
geth.p2p/ingress/eth/64/0x01.meter
geth.p2p/ingress/eth/65/0x01.meter
geth.p2p/ingress/eth/63/0x02.meter
geth.p2p/ingress/eth/64/0x02.meter
geth.p2p/ingress/eth/65/0x02.meter
geth.p2p/ingress/eth/63/0x03.meter
geth.p2p/ingress/eth/64/0x03.meter
geth.p2p/ingress/eth/65/0x03.meter
geth.p2p/ingress/eth/63/0x04.meter
geth.p2p/ingress/eth/64/0x04.meter
geth.p2p/ingress/eth/65/0x04.meter
geth.p2p/ingress/eth/63/0x05.meter
geth.p2p/ingress/eth/64/0x05.meter
geth.p2p/ingress/eth/65/0x05.meter
geth.p2p/ingress/eth/63/0x06.meter
geth.p2p/ingress/eth/64/0x06.meter
geth.p2p/ingress/eth/65/0x06.meter 
geth.p2p/ingress/eth/63/0x07.meter
geth.p2p/ingress/eth/64/0x07.meter
geth.p2p/ingress/eth/65/0x07.meter    
geth.p2p/ingress/eth/65/0x08.meter
geth.p2p/ingress/eth/65/0x09.meter
geth.p2p/ingress/eth/65/0x0a.meter
geth.p2p/ingress/eth/63/0x0d.meter
geth.p2p/ingress/eth/64/0x0d.meter
geth.p2p/ingress/eth/65/0x0d.meter
geth.p2p/ingress/eth/63/0x0e.meter
geth.p2p/ingress/eth/64/0x0e.meter
geth.p2p/ingress/eth/65/0x0e.meter
geth.p2p/ingress/eth/63/0x0f.meter
geth.p2p/ingress/eth/64/0x0f.meter
geth.p2p/ingress/eth/65/0x0f.meter
geth.p2p/ingress/eth/63/0x10.meter
geth.p2p/ingress/eth/64/0x10.meter
geth.p2p/ingress/eth/65/0x10.meter
```

### Block processing

```
geth.chain/execution.timer
geth.chain/validation.timer
geth.chain/write.timer
geth.chain/account/reads.timer
geth.chain/account/updates.timer
geth.chain/account/hashes.timer
geth.chain/account/commits.timer
geth.chain/storage/reads.timer
geth.chain/storage/updates.timer
geth.chain/storage/hashes.timer
geth.chain/storage/commits.timer
geth.chain/snapshot/account/reads.timer
geth.chain/snapshot/storage/reads.timer
geth.chain/snapshot/commits.timer
```

### Transactions processing

```
geth.txpool/known.meter
geth.txpool/valid.meter
geth.txpool/invalid.meter
geth.txpool/underpriced.meter
geth.txpool/pending/discard.meter
geth.txpool/pending/replace.meter
geth.txpool/pending/ratelimit.meter
geth.txpool/pending/nofunds.meter
geth.txpool/queued/discard.meter
geth.txpool/queued/replace.meter
geth.txpool/queued/ratelimit.meter
geth.txpool/queued/nofunds.meter
```

### Block propagation

```
geth.eth/fetcher/block/announces/in.meter
geth.eth/fetcher/block/announces/drop.meter
geth.eth/fetcher/block/announces/dos.meter
geth.eth/fetcher/block/broadcasts/in.meter
geth.eth/fetcher/block/broadcasts/drop.meter
geth.eth/fetcher/block/broadcasts/dos.meter
```

### Transaction propagation

```
geth.eth/fetcher/transaction/announces/in.meter
geth.eth/fetcher/transaction/announces/known.meter
geth.eth/fetcher/transaction/announces/underpriced.meter
geth.eth/fetcher/transaction/announces/dos.meter
geth.eth/fetcher/transaction/broadcasts/in.meter
geth.eth/fetcher/transaction/broadcasts/known.meter
geth.eth/fetcher/transaction/broadcasts/underpriced.meter
geth.eth/fetcher/transaction/broadcasts/otherreject.meter
geth.eth/fetcher/transaction/request/out.meter
geth.eth/fetcher/transaction/request/done.meter
geth.eth/fetcher/transaction/request/fail.meter
geth.eth/fetcher/transaction/request/timeout.meter
geth.eth/fetcher/transaction/replies/in.meter
geth.eth/fetcher/transaction/replies/known.meter
geth.eth/fetcher/transaction/replies/underpriced.meter
geth.eth/fetcher/transaction/replies/otherreject.meter
```

### Block forwarding


```
geth.eth/fetcher/block/announces/out.timer
geth.eth/fetcher/block/broadcasts/out.timer
```

### Transaction fetcher


```
geth.eth/fetcher/transaction/waiting/hashes.gauge
geth.eth/fetcher/transaction/queueing/hashes.gauge
geth.eth/fetcher/transaction/fetching/hashes.gauge
```

### Data rate

```
geth.eth/db/chaindata/disk/read.meter
geth.eth/db/chaindata/disk/write.meter m1/mean
geth.eth/db/chaindata/ancient/read.meter
geth.eth/db/chaindata/ancient/write.meter
geth.eth/db/chaindata/compact/input.meter mean
geth.eth/db/chaindata/compact/output.meter
```

### Session total

```
geth.eth/db/chaindata/disk/read.meter
geth.eth/db/chaindata/disk/write.meter
geth.eth/db/chaindata/ancient/read.meter
geth.eth/db/chaindata/ancient/write.meter
geth.eth/db/chaindata/compact/input.meter
geth.eth/db/chaindata/compact/output.meter

```

## Database

### Compaction count

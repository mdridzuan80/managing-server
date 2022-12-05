# Geth dashboard

There are 59 panels and there are categorised into 5 following sections. Each panel can one or more measurements and each measurement has a field.

1. System (3 panels)
2. Network (6 panels)
3. Blockchain (24 panels)
4. Database (3 panels)
5. Light server (23 panels)

| No  | Panel                                   | Section    |
| --- | --------------------------------------- | ---------- |
| 01  | [CPU](#cpu)                             | System     |
| 02  | [Memory](#memory)                       | System     |
| 03  | [Disk](#disk)                           | System     |
| 04  | [Traffic](#traffic)                     | Network    |
| 05  | [Peers](#peers)                         | Network    |
| 06  | [Ingress data rate](#ingress-data-rate) | Network    |
| 07  | [Egress data rate](#egress-data-rate)   | Network    |
| 08  | [Ingress traffic](#ingress-traffic)     | Network    |
| 09  | [Egress traffic](#egress-traffic)       | Network    |
| 10  | [Latest header](#latest-header)         | Blockchain |
| 11  | [Latest receipt](#latest-receipt)       | Blockchain |
| 12  | [Latest block](#latest-block)           | Blockchain |
| 13  | [Chain head](#chain-head)               | Blockchain |

### CPU

| No  | Measurement                      | Field |
| --- | -------------------------------- | ----- |
| 01  | `geth.system/cpu/sysload.gauge`  | value |
| 02  | `geth.system/cpu/sysload.gauge`  | value |
| 03  | `geth.system/cpu/procload.gauge` | value |

### Memory

| No  | Measurement                       | Field |
| --- | --------------------------------- | ----- |
| 01  | `geth.system/memory/allocs.meter` | mean  |
| 02  | `geth.system/memory/used.gauge`   | mean  |
| 03  | `geth.system/memory/held.gauge`   | mean  |

### Disk

| No  | Measurement | Field |
| --- | ----------- | ----- |

### Traffic

| No  | Measurement | Field |
| --- | ----------- | ----- |

### Peers

| No  | Measurement | Field |
| --- | ----------- | ----- |

### Ingress data rate

| No  | Measurement                          | Field |
| --- | ------------------------------------ | ----- |
| 01  | `geth.p2p/ingress/eth/63/0x00.meter` | m1    |
| 02  | `geth.p2p/ingress/eth/64/0x00.meter` | m1    |
| 03  | `geth.p2p/ingress/eth/65/0x00.meter` | m1    |
| 04  | `geth.p2p/ingress/eth/63/0x01.meter` | m1    |
| 05  | `geth.p2p/ingress/eth/64/0x01.meter` | m1    |
| 06  | `geth.p2p/ingress/eth/65/0x01.meter` | m1    |
| 07  | `geth.p2p/ingress/eth/63/0x02.meter` | m1    |
| 08  | `geth.p2p/ingress/eth/64/0x02.meter` | m1    |
| 09  | `geth.p2p/ingress/eth/65/0x02.meter` | m1    |
| 10  | `geth.p2p/ingress/eth/63/0x03.meter` | m1    |
| 11  | `geth.p2p/ingress/eth/64/0x03.meter` | m1    |
| 12  | `geth.p2p/ingress/eth/65/0x03.meter` | m1    |
| 13  | `geth.p2p/ingress/eth/63/0x04.meter` | m1    |
| 14  | `geth.p2p/ingress/eth/64/0x04.meter` | m1    |
| 15  | `geth.p2p/ingress/eth/65/0x04.meter` | m1    |
| 16  | `geth.p2p/ingress/eth/63/0x05.meter` | m1    |
| 17  | `geth.p2p/ingress/eth/64/0x05.meter` | m1    |
| 18  | `geth.p2p/ingress/eth/65/0x05.meter` | m1    |
| 18  | `geth.p2p/ingress/eth/63/0x06.meter` | m1    |
| 19  | `geth.p2p/ingress/eth/64/0x06.meter` | m1    |
| 20  | `geth.p2p/ingress/eth/65/0x06.meter` | m1    |
| 21  | `geth.p2p/ingress/eth/63/0x07.meter` | m1    |
| 22  | `geth.p2p/ingress/eth/64/0x07.meter` | m1    |
| 23  | `geth.p2p/ingress/eth/65/0x07.meter` | m1    |
| 24  | `geth.p2p/ingress/eth/65/0x08.meter` | m1    |
| 25  | `geth.p2p/ingress/eth/65/0x09.meter` | m1    |
| 26  | `geth.p2p/ingress/eth/65/0x0a.meter` | m1    |
| 27  | `geth.p2p/ingress/eth/63/0x0d.meter` | m1    |
| 28  | `geth.p2p/ingress/eth/64/0x0d.meter` | m1    |
| 29  | `geth.p2p/ingress/eth/65/0x0d.meter` | m1    |
| 30  | `geth.p2p/ingress/eth/63/0x0e.meter` | m1    |
| 31  | `geth.p2p/ingress/eth/64/0x0e.meter` | m1    |
| 32  | `geth.p2p/ingress/eth/65/0x0e.meter` | m1    |
| 33  | `geth.p2p/ingress/eth/63/0x0f.meter` | m1    |
| 34  | `geth.p2p/ingress/eth/64/0x0f.meter` | m1    |
| 35  | `geth.p2p/ingress/eth/65/0x0f.meter` | m1    |
| 36  | `geth.p2p/ingress/eth/63/0x10.meter` | m1    |
| 37  | `geth.p2p/ingress/eth/64/0x10.meter` | m1    |
| 38  | `geth.p2p/ingress/eth/65/0x10.meter` | m1    |

### Egress data rate

-TODO-

### Ingress traffic

-TODO-

### Egress traffic

-TODO-

### Latest header

| No  | Measurement                    | Field |
| --- | ------------------------------ | ----- |
| 01  | `geth.chain/head/header.gauge` | value |

### Latest receipt

| No  | Measurement                     | Field |
| --- | ------------------------------- | ----- |
| 01  | `geth.chain/head/receipt.gauge` | value |

### Latest block

| No  | Measurement                   | Field |
| --- | ----------------------------- | ----- |
| 01  | `geth.chain/head/block.gauge` | value |

### Chain head

| No  | Measurement                     | Field |
| --- | ------------------------------- | ----- |
| 01  | `geth.chain/head/header.gauge`  | value |
| 02  | `geth.chain/head/receipt.gauge` | value |
| 03  | `geth.chain/head/block.gauge`   | value |

### Block processing

| No  | Measurement                             | Field |
| --- | --------------------------------------- | ----- |
| 01  | geth.chain/execution.timer              | mean  |
| 02  | geth.chain/validation.timer             | mean  |
| 03  | geth.chain/write.timer                  | mean  |
| 04  | geth.chain/account/reads.timer          | mean  |
| 05  | geth.chain/account/updates.timer        | mean  |
| 06  | geth.chain/account/hashes.timer         | mean  |
| 08  | geth.chain/storage/reads.timer          | mean  |
| 09  | geth.chain/storage/updates.timer        | mean  |
| 10  | geth.chain/storage/hashes.timer         | mean  |
| 11  | geth.chain/storage/commits.timer        | mean  |
| 12  | geth.chain/snapshot/account/reads.timer | mean  |
| 13  | geth.chain/snapshot/storage/reads.timer | mean  |

### Transactions processing

| No  | Measurement                         | Field |
| --- | ----------------------------------- | ----- |
| 01  | geth.txpool/known.meter             |
| 02  | geth.txpool/valid.meter             |
| 03  | geth.txpool/invalid.meter           |
| 04  | geth.txpool/underpriced.meter       |
| 05  | geth.txpool/pending/discard.meter   |
| 06  | geth.txpool/pending/replace.meter   |
| 07  | geth.txpool/pending/ratelimit.meter |
| 08  | geth.txpool/pending/nofunds.meter   |
| 09  | geth.txpool/queued/discard.meter    |
| 10  | geth.txpool/queued/replace.meter    |
| 11  | geth.txpool/queued/ratelimit.meter  |
| 12  | geth.txpool/queued/nofunds.meter    |

### Block propagation

| No  | Measurement                                  | Field |
| --- | -------------------------------------------- | ----- |
| 01  | geth.eth/fetcher/block/announces/in.meter    | mean  |
| 02  | geth.eth/fetcher/block/announces/drop.meter  | mean  |
| 03  | geth.eth/fetcher/block/announces/dos.meter   | mean  |
| 04  | geth.eth/fetcher/block/broadcasts/in.meter   | mean  |
| 05  | geth.eth/fetcher/block/broadcasts/drop.meter | mean  |
| 06  | geth.eth/fetcher/block/broadcasts/dos.meter  | mean  |

### Transaction propagation

| No  | Measurement | Field |
| --- | ----------- | ----- |

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

### Compaction count

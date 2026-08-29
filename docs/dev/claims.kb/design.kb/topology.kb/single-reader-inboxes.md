---
label: SINGLE_READER
standing: agent
---

# Every inbox has exactly one reader

An inbox directory is consumed by exactly one session; work
distribution happens by addressing — one inbox per worker — never by a
shared claim-queue. With one reader there are no claim races, so the
`read/` move stays advisory and no transport needs atomic rename. The
declined alternative, a shared queue with claim semantics, buys load
balancing at the cost of a locking protocol every transport must
honor — which weak mounts (S3 and kin) cannot.

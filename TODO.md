# Project TODO

Systems-level project ideas: database internals, concurrency, distributed systems, networking.

## Flagship

- [ ] Raft-replicated KV store with a real storage engine (LSM-tree or B+Tree + WAL/crash recovery), exposed over a custom TCP/gRPC protocol.

## Database internals

- [ ] Mini LSM-tree engine in Rust (memtable -> SSTable flush -> compaction).
- [ ] B+Tree on-disk index with WAL-based crash recovery, in C.
- [ ] Simple SQL query planner/executor on top of either engine.

## Concurrency

- [ ] Lock-free concurrent hash map or queue in Rust/C using atomics (CAS, hazard pointers / epoch-based reclamation).
- [ ] Work-stealing thread pool / scheduler in Go or C.
- [ ] Channels/mutexes/semaphores from scratch on top of raw futex/atomic primitives.

## Distributed systems

- [ ] Raft in isolation (leader election + log replication), tested with simulated network partitions/packet loss.
- [ ] Distributed task queue with leader election via gossip/heartbeat protocol.
- [ ] Consistent hashing ring for sharding + toy distributed cache.

## Networking

- [ ] HTTP/1.1 server from raw TCP sockets in C (parsing, keep-alive, chunked encoding).
- [ ] Custom binary RPC protocol over TCP in Go (framing, multiplexing, backpressure).
- [ ] Simple L4 load balancer / reverse proxy with health checks.

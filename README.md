## LogPress — Lightweight Distributed Logging
Pattern-aware compression + index-free, high-speed querying for large-scale, distributed logs.

### Why LogPress?
Traditional log stacks pay heavy costs in storage and indexing. LogPress compresses logs as they arrive using pattern-aware structuring and dictionary-based encoding, then serves fast queries without external indexes via schema-aware grouping and time partitioning.

### Features
1. Distributed ingestion: shard-friendly writers for high-throughput, real-world workloads.
2. Pattern-aware compression: tokenization + dictionaries tuned for log structure (keys, enums, IDs).
3. Index-free querying: schema-aware grouping + time partitions → low-latency scans without a separate index.
4. Pluggable storage: local FS or object stores (S3-style paths).
5. Simple APIs: CLI + Python client for ingest/search.

### How it works?
1. Ingest: logs → normalized schema (ts, source, level, msg, fields…).
2. Structure: split into stable templates and variable fields (pattern extraction).
3. Compress: dictionary + RLE/varint packing (message templates stored once).
4. Lay out: time-based partitions (e.g., hourly) with small, contiguous segments.
5. Query: push down predicates (time, level, source, field filters) → scan only relevant segments.
6. Return: reconstruct messages on the fly from template + fields.

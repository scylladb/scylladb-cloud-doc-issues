# Fix: Quick Start Guide to Vector Search - Use Default Replication

**Page**: https://cloud.docs.scylladb.com/master/vector-search/vector-search-quick-start

## Problem

The page shows an explicit replication configuration that is not needed for ScyllaDB Cloud, where replication is managed automatically:

```cql
CREATE KEYSPACE myapp
WITH replication = {
  'class': 'NetworkTopologyStrategy',
  'replication_factor': 3
};
```

## Fix

Use the default replication, which ScyllaDB Cloud manages automatically:

```cql
CREATE KEYSPACE myapp;
```

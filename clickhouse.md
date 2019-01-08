# [ClickHouse](https://clickhouse.yandex/)

## Resources

- [Building Multi-Petabyte Data Warehouses with ClickHouse](https://www.percona.com/live/e17/sessions/building-multi-petabyte-data-warehouses-with-clickhouse)
- [Graphite Monitoring](https://www.altinity.com/blog/2018/4/20/clickhouse-monitoring-with-graphite)
- [Ultimate Helm Chart](https://github.com/plutov/clickhouse-helm)

## UI

[https://tabix.io](https://tabix.io)

## Best Practices
- For small amounts of data (up to \~200 GB compressed), it is best to use as much memory as the volume of data. For large amounts of data and when processing interactive (online) queries, you should use a reasonable amount of RAM (128 GB or more) so the hot data subset will fit in the cache of pages. Even for data volumes of \~50 TB per server, using 128 GB of RAM significantly improves query performance compared to 64 GB.
- We should make bulk inserts. Preferably ~ 10000 rows at a time.
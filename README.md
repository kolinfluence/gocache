# Fastest Zero Allocation LRU Cache for Golang 
(for key, value pairs in []byte)

## cxlrubytes

Supposingly having the best cache hit ratio (in zero allocation class) with "optimum" memory usage.

Please contribute to make it better.
Feedback / comments / suggestions on improvement appreciated (stars too).

Check [lru/bytes](https://github.com/cloudxaas/gocache/tree/main/lru/bytes) for details for key, value in []byte (tested).

Check [lru](https://github.com/cloudxaas/gocache/tree/main/lru) for untested Any type details (tested).

## Motivation

Most current (year 2024) golang lru implementations are either not as fast as this, or needed capacity count of items as input parameter, this can result in "OOM" or not being able to fully utilize the memory capacity available.

cxlrubytes thus is designed for:
1. High performance
2. Zero allocation (so no garbage collection)
3. Maximizing memory usage (but not being limited by item capacity)

Will do other input parameters in future but currently, converting everything to []byte and using this gives wonderful results.

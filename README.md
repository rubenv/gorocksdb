# gorocksdb, a Go wrapper for RocksDB

[![Build Status](https://travis-ci.org/rubenv/gorocksdb.png)](https://travis-ci.org/rubenv/gorocksdb) [![GoDoc](https://godoc.org/github.com/rubenv/gorocksdb?status.png)](http://godoc.org/github.com/rubenv/gorocksdb)

## Install

There exist two options to install gorocksdb.
You can use either a own shared library or you use the embedded RocksDB version from [CockroachDB](https://github.com/cockroachdb/c-rocksdb).

To install the embedded version (default, it might take a while):

    go get github.com/rubenv/gorocksdb

If you want to go the way with the shared library you'll need to build
[RocksDB](https://github.com/facebook/rocksdb) before on your machine.
If you built RocksDB you can install gorocksdb now:

    CGO_CFLAGS="-I/path/to/rocksdb/include" \
    CGO_LDFLAGS="-L/path/to/rocksdb -lrocksdb -lstdc++ -lm -lz -lbz2 -lsnappy -llz4" \
      go get -tags=dynamic github.com/rubenv/gorocksdb

## Relation to [tecbot/gorocksdb](https://github.com/tecbot/gorocksdb)

This version of gorocksdb uses the embedded version by default.

The version by [tecbot](https://github.com/tecbot/gorocksdb) is still
considered the upstream: please submit fixes and pull requests there. I'll
periodically merge changes back to this repository.

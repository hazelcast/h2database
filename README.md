# Welcome to H2, the Java SQL database. [![Build Status](https://travis-ci.org/h2database/h2database.svg?branch=master)](https://travis-ci.org/h2database/h2database)

## Building H2 for using in Hazelcast Management Center

This branch of H2DB contains patches to fix several security vulnerabilities. We build and use the patched version in
Hazelcast Management Center. The output file contains no reference to `1.4.197` as it triggers security scanners and
cause the artifact to be marked vulnerable.

To build and update the version used in Management Center, execute the following command (remember to change the target
directory according to your local):

```shell
./build.sh clean
./build.sh mavenInstallLocal
```

## The main features of H2 are:

1. Very fast, open source, JDBC API
2. Embedded and server modes; in-memory databases
3. Browser based Console application
4. Small footprint: around 2 MB jar file size

More information: http://h2database.com

## Features

| | [H2](http://www.h2database.com/) | [Derby](http://db.apache.org/derby) | [HSQLDB](http://hsqldb.org) | [MySQL](https://www.mysql.com/) | [PostgreSQL](https://www.postgresql.org) |
|--------------------------------|---------|---------|---------|-------|---------|
| Pure Java                      | Yes     | Yes     | Yes     | No    | No      |
| Memory Mode                    | Yes     | Yes     | Yes     | No    | No      |
| Encrypted Database             | Yes     | Yes     | Yes     | No    | No      |
| ODBC Driver                    | Yes     | No      | No      | Yes   | Yes     |
| Fulltext Search                | Yes     | No      | No      | Yes   | Yes     |
| Multi Version Concurrency      | Yes     | No      | Yes     | Yes   | Yes     |
| Footprint (embedded database)  | ~2 MB   | ~3 MB   | ~1.5 MB | —     | —       |
| Footprint (JDBC client driver) | ~500 KB | ~600 KB | ~1.5 MB | ~1 MB | ~700 KB |

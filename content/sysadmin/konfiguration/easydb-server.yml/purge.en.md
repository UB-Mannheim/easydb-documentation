---
title: yaml configuration for frontend purging
layout: config
menu:
  main:
    name: "configure purge"
    identifier: "sysadmin/konfiguration/easydb-server.yml/purge"
    parent: "sysadmin/konfiguration/easydb-server.yml"
easydb-server.yml:
---

# Allow to empty the database

To be able to replace the database with a fresh, empty one, via the webfrontend, add this to your `easydb-server.yml`:

## easydb-server.yml

```yaml
server:
  api:
    settings:
      purgedata: true
```

The default is: `false`, or in other words: disabled.

`easydb-server.yml` is part of the directory `config` in your central data storage directory which was set up during [installation](../../../installation).

> Warning: Using the now enabled feature is destructive and cannot be undone (better have backups at hand).

# Allow to empty the database and schema


To be able to replace the database with a fresh, empty one, via the webfrontend, and at the same time reset the database schema to a that of a fresh installation, add this to your `easydb-server.yml`:

## easydb-server.yml

```yaml
server:
  api:
    settings:
      purgeall: true
```

The default is: `false`, or in other words: disabled.

`easydb-server.yml` is part of the directory `config` in your central data storage directory which was set up during [installation](../../../installation).

> Warning: Using the now enabled feature is destructive and cannot be undone (better have backups at hand).

# further reading

* [Documentation of the feature in the frontend](../../../../webfrontend/administration/server-status/)

* [List of all configuration directives](../)

* [List of configuration files](../../)


---
menu:
  main:
    name: "5.98 (April 2022)"
    identifier: "5.98"
    parent: "releases599"
    weight: -598
---

> This version **does not require a new index build**

# Version 5.98.2

*Released on 19.04.2022*

## Webfrontend

### Fixed

* **CSV importer**: fix cascaded nested fields
* **Export**: fix selection of custom fields

## Server

### Fixed

* **Export**: error with non-unique file names fixed
* **EAS**: fix zoomer requests

# Version 5.98.1

*Released on 08.04.2022*

## Webfrontend

### Fixed

* **Filter Tree**: fixed count of filters after adding more than one filter
* **Expert search**: removed a wrong check to show the 'without' label for nested tables
* **Collection Presentation**: fixed CSS for background of images and black slides

# Version 5.98.0

*Released on 06.04.2022*

> A security issue has been resolved with this release. We are happy to share details upon request to support@programmfabrik.de.

## Webfrontend

### Improved

* **Common**: consistent use of thousands separator for numbers
* **Filter**: improved titles of linked objects
* **Base configuration**: Ace library not loaded from external resources anymore

### Fixed

* **CSV importer**: fix problem with system object ID in hierarchies
* **CSV importer**: fix preview of linked objects
* **JSON importer**: fix error when using lookup feature and more than 1000 IDs in search
* **Editor/detail**: mask options for display of object type and pool fixed for linked objects
* **Search**: fix error for assets in cascaded linked objects
* **Editor**: don't set pool for reverse-nested parent objects
* **Metadata mapping**: don't limit available fields by mask

## Server

### New

* **/api/v1/event**: read-only requests except polling now require system right `system.api.event.get`, deleting events requires `system.api.event.delete`

### Improved

* **/api/v1/objecttype**: further performance improvements
* **Pool**: allow comments
* **custom datatype updater**: abort batch after 10 failures

### Fixed

* **Export**: limit length of download names to 100 characters to prevent hitting filesystem limits
* **Export**: error fetching files from EAS does not abort whole export
* **Index**: fix sorting of `_standard.eas` when nested fields are used
* **Suggest**: completion of linked objects now requires all tokens to be included in suggested object
* **custom datatype updater**: fix number of objects in batch after a failed attempt
* **Session**: correctly merge string parameters of system rights, metadata parameters in groups sometimes had no effect

# Checksums

Here are the checksums of our Docker images (latest version):

```ini
docker.easydb.de/pf/chrome               sha256:451a6d6e05936ed704277c6842b4ad3119f25a2ed5631734f71049f3b8069cc4
docker.easydb.de/pf/eas                  sha256:aa78b6a8cc56b74b351e4d14b1b8cb51ec74e9ce9dfec23f3f142abb5909f852
docker.easydb.de/pf/elasticsearch        sha256:bac077eb81d38b8f6e6506ffea7a5c26e5043832e6747886b2e7b12484cc57d7
docker.easydb.de/pf/fylr                 sha256:b3bfa2edbaad51563d8165fd52c7c0ab8cdf78ac2f42cd62e511487bb5d5e279
docker.easydb.de/pf/postgresql-11        sha256:b3562998e544ca25271b15a46ca10cf53025798cf7b9707e758063252b936986
docker.easydb.de/pf/server-base          sha256:6037f74655fe928713b4b505fce26c8d590daadecd8ed3118b1e187e8cdbecb3
docker.easydb.de/pf/server-base-py3      sha256:ee5cc91b4f691fa4c6664cb96f13e80c802d44c213866e9e134ec6db9f74bb65
docker.easydb.de/pf/webfrontend          sha256:3d779d99b61d4e019009dc26662fb21f52e96a21ca66a6ed9116f3d37095e1e1
```

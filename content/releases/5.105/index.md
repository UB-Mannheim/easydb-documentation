---
menu:
  main:
    name: "5.105 (Ende August 2022)"
    identifier: "5.105"
    parent: "releases"
    weight: -605
---

> Diese Version benötigt **keinen neuen** Index-Aufbau

# Version 5.105.0

*Veröffentlicht am 31.08.2022*

# Webfrontend

## Neu

* **Änderungshistorie**: Pools in alten Objektversionen, die inzwischen gelöscht wurde, werden jetzt als *"Ohne Pool"* angezeigt

## Verbessert

* Timestamps im Format `"YYYY-MM-DDTHH:mm:ss.SSSSZ"` können jetzt ebenfalls geparst werden

## Behoben

* **Gespeicherte Suchen**: Bugfix beim Laden von Daten für den Filter
* **Drucken**: Bugfix im Pulldown-Menü für PDF-Vorlagen
* Bugfix bei der Darstellung von *Custom Fields* und leeren Mask-Splittern

# Server

## Neu

* **Janitor**: in der Basiskonfiguration kann eingestellt werden, dass *alle* Ereignistypen nach einer bestimmten Zeit gelöscht werden

## Verbessert

* **Custom Data Types**:
  * Kompatibilität für Custom Data Types aus Plugins
  * behebt Probleme im Datenmodell, die entstehen können, wenn der Typ von Plugins zwischen `base` und `extension` geändert wurde
* **Rechtemanagement**: für Objekte mit revers verlinkten Objekten gelten die Rechte am Hauptobjekt auch für sämtliche revers verlinkten Objekte

## Behoben

* **Änderungshistorie:** inzwischen gelöschte Pools in alten Objektversionen werden als `null` zurückgegeben, um sie als gelöscht zu markieren


# Prüfsummen

Hier die Prüfsummen unserer Docker-Images (neueste Version):

```ini
docker.easydb.de/pf/chrome               sha256:c148459d9c44b1862f54dabe6d5c9548e3a22871640be42558b5a3bf5696c162
docker.easydb.de/pf/eas                  sha256:7f197576091088a8876d39021b97a05e175c8d6908c5faa233045de2a37fe81f
docker.easydb.de/pf/elasticsearch        sha256:8c60a124e33167925eb772d277df818786af7a2a6479ae4c0e35cce45a1fa6a0
docker.easydb.de/pf/fylr                 sha256:6106612af4eaeff6311fad03708e61745a52e21aaccc9ea557ea8d49601bb774
docker.easydb.de/pf/postgresql-11        sha256:ec0d1d09dfff4bb3f4dd659e8ef7b8e4c66d72f6414283a9b824cc8bbfcc2458
docker.easydb.de/pf/postgresql-14        sha256:e807fe051782b693d970bc5938a78a896a6d042efc82e0ba08af6a9ce3f4d719
docker.easydb.de/pf/server-base          sha256:e65da2cfa31d0a6044f54e27650049838bdee4991aaa33952ad06abfba90f412
docker.easydb.de/pf/webfrontend          sha256:77ce3b215e35b6bf486591d2340db876a296ab73348faba387dc4dbed0253516
```
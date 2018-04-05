## Export und OAI/PMH

easydb stellt verschiedene Arten des unauthentifizierten Zugriffs auf die Dateien und Daten bereit. Für die Zugriffe stehen zum einen Deep-Links und zum anderen OAI/PMH zur Verfügung.

Nutzen Sie Deep-Links wenn es darum geht eine Ressource aus der easydb direkt im Zugriff zu haben, OAI/PMH kann genutzt werden um mehrere Ressourcen und auch Veränderungen an Ressourcen zu überwachen und zu laden.

### Deep-Link

Die Deep-Link-Freigaben sind technisch über die API-Schnittstelle [/api/objects](https://docs.easydb.de/en/technical/api/objects/objects.html) gelöst. Dort finden sich explizite Informationen über den Aufbau der URL. Im Frontend finden Sie an verschiedenen Stellen diese Deep-Links [Detail(Teilen)]() und im [EAS-Column(Teilen/) und im [EAS-Column(Teilen.html)](). Deep-Links werden immer über den Benutzer *DeepLink* authentifiziert. Geben Sie diesem Benutzer die nötigen Rechte an den Daten, damit der Zugriff von außen erfolgen kann.


|Einstellung | Erläuterung |
|----|---|
|erlauben| An- und Ausschalten der Deep-Link-Schnittstelle. |
|inklusive sichtbarer Referenz auf ID| Erlaubt einen direkt Zugriff per Objekt-ID. Da diese Objekt-IDs fortlaufend vergeben werden, kann es ein Sicherheitsrisiko sein, diese Option freizuschalten. Ein Benutzer dem ein Deep-Link bekannt gemacht wird, kann durch probieren weitere Deep-Links erraten. Für alle Deep-Links gilt aber immer, dass der *DeepLink*-Benutzer auf die Objekte Zugriff haben muss, damit sie funktionieren. |
|inklusive sichtbarer Referenz auf ein eindeutiges Feld| Wie die Referenz auf ID legen sie hiermit fest, ob über eineindeutige Datenfelder ein Deep-Link-Zugriff erfolgen darf oder nicht.|
|EAS-URLs anzeigen|Mit dieser Option werden direkte Datei-Links in der z. B. XML Ausgabe der Deep-Links geschrieben. Diese Links zielen direkt auf eine Datei und sind nicht mehr rechte-gemanagt. Diese URLs verlieren nie ihre Gültigkeit. Ohne diese Option stehen im XML noch anderen URLs für den Zugriff auf Dateien zur Verfügung. |
| Verlinkte Datensätze einbetten | Verlinkte Objekte sind, wie beim XML-Export, standardmäßig nicht im XML-Dokument enthalten. Wird die Option "Nicht in der Hauptsuche enthaltene Datensätze" gewählt, werden während des Exports alle verlinkten Objekte, die nicht in der Hauptsuche enthalten sind, nachgeladen und im XML eingebettet. Wird "Keine" ausgewählt, werden keine verlinkten Datensätze nachgeladen, sondern nur der Standard wird exportiert. |

### OAI/PMH

Die OAI/PMH-Schnittstelle ist eine Harvesting-Schnittstelle. Mehr Informationen dazu finden Sie in der [Protokoll-Beschreibung](https://docs.easydb.de/en/technical/protocols/oai-pmh/oai-pmh.html) und auf [Openarchives](http://www.openarchives.org/).

Die Suchen die die Schnittstelle durchführt, werden mit dem System-Benutzer *OAI/PMH* durchgeführt. Geben Sie diesem Benutzer die Rechte Daten zu sehen.

|Einstellung | Erläuterung |
|----|---|
|Freigeben| An- und Ausschalten der OAI/PMH-Schnittstelle. |
|Repository-Name| Name des OAI/PMH-Repository. |
|Administrator-E-Mail| Email die in den OAI-Antworten angegeben ist.|
|Namespace| Frei definierbarer OAI-Identifier-Namespace. Objekte können beispielsweise über `oai:<namespace>:<uuid>` in der URL angefordert werden. |
|Tag-Sets|Definieren Sie hier Tagfilter, um neue OAI/PMH-Sets zu erzeugen. Sie können damit z.B. alle Objekte zusammenfassen, die den Tag *Internet* haben. |
|EAS-URLs anzeigen|Wie bei den Deep-Links wird damit festgelegt, ob die direkten Datei-Links im XML ausgeben werden oder nicht. Siehe Deep-Link.|

#### XSLT-Formate

Die OAI/PMH-Schnittstelle kann neben dem Standard-easydb-Format und [Dublin-Core](http://dublincore.org/) (das ist Pflicht bei OAI-PMH) eigen definierte Formate bereitstellen (z.B. LIDO). Um Dublin Core zu nutzen, muss im Bereich [Metadaten-Mapping](../profiles/profiles.html) ein Dublin-Core-Mapping eingerichtet werden. Darüber hinaus muss dieses im Anschluss beim entsprechenden [Objekttyp](../datamodel/objecttype/objecttype.html) verknüpft werden. Für diese Formate muss ein XSLT erstellt werden, welches das Standard-easydb-Format umwandelt. Die OAI/PMH-Schnittstelle stellt je hochgeladenem XSLT ein Metadaten-Format bereit.


|Einstellung | Erläuterung |
|----|---|
|OAI/PMH-Präfix| Technischer Name des Formates in der OAI/PMH-Schnittstelle. |
|Anzeigename| Anzeigenname des Formates im XML der OAI/PMH-Schnittstelle. |
|Beschreibung| Beschreibung des Formates im XML der OAI/PMH-Schnittstelle. |
|XSLT| XSLT-Datei zur Tranformation der Daten. |
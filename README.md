# SVP 6000

Das SVP 6000 kann als selbsschließendes Anti-Panik-Schloss mit elektrisch einkuppelbarer Außenklinke verwendet werden um im Bereich von Smart-Home Anwendungen Türen "smart" zu öffnen.

## Dokumentation Anschluss

Dokumentation Stecker für Kabel Dorma A 1000. Draufsicht auf Schloss.

![SVP 6000](/SVP-6000.svg)

An allen "Doppelpfeilen" kann jeweils zwischen dem jeweilgen Anschluss und dem dazugehörigen COM den Zustand des Schlosses bestimmen.

NO = Normally open, NC = Normally Closed.

Der Grounding Loop wird **immer** benötigt wenn  die Tür als solches und damit auch das Schloss nicht geerdet sind (bspw. Holztüren).

Zum Einklinken der Türklinke müssen nur GND und der Türöffner PIN (beispielsweise über einen Schalter) verbunden werden.

Die Sabotagelinie wird idR nicht benötigt und dient nur der Überwachung ob das Kabel oder Schloss manipuliert wurde.

Weitere Doku: [Dorma Webseite](https://www.dormakaba.com/resource/blob/189714/53452861bc0772204e3593a7126a24f6/svp-a-1000-svp-4xxx-svp-6xxx-ch-12-pdf-data.pdf) - [WebArchive](https://web.archive.org/web/20220605210129/https://www.dormakaba.com/resource/blob/189714/53452861bc0772204e3593a7126a24f6/svp-a-1000-svp-4xxx-svp-6xxx-ch-12-pdf-data.pdf)

## Empfehlung Setup

Bei uns wird das Schloss über Ethernet angesprochen und per PoE mit Strom versorgt. Als Microcontroller wird ein WT32-ETH01 Microcontroller eingesetzt. Dieser baut auf dem bekannten ESP32 auf, verfügt aber auch über einen LAN Port. Als Firmware kommt [Tasmota](https://templates.blakadder.com/wireless_tag_WT32-ETH01.html) zum Einsatz das dann auch die einfache Integration in [Homeassistant](https://www.home-assistant.io/) erlaubt. Angebunden wird das Schloss über ein Relais. Das Auslesen des Schlosses erfolgt über Optokoppler

- [PoE Splitter PLANET POE-162S](https://amzn.to/38Qictl)
- [Mikrocontroller WT32-ETH01](https://amzn.to/3mhNoF5)
- [Optokoppler Modul](https://amzn.to/3NlAgdP)
- [Relais](https://amzn.to/3MftlBP)


Alle Links sind Amazon Affiliate-Links. Ich empfehle aber eine Preisrecherche vor dem Kauf!
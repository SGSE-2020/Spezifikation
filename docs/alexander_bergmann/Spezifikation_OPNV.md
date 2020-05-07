# ‚Anforderungs- und Entwurfsspezifikation ("Pflichtenheft")

* __Titel:__ SmartCity-ÖPNV
* __Author:__ Alexander Bergmann
* __Source Code:__ [Repo MS_OPNV](https://github.com/SGSE-2020/MS_OPNV.git), [Repo Spezifikation](https://github.com/SGSE-2020/Spezifikation/tree/master/docs/alexander_bergmann), [Repo Projekttagebuch](https://github.com/SGSE-2020/Praktikumstagebuch/tree/master/alexander_bergmann)

# 1 Einführung

## 1.1 Beschreibung

Die Plattform für den öffentlichen Personennahverkehr der Smart City bietet nicht nur die möglichkeit zum Erwerb von Fahrkarten für Buse und Bahnen, sondern bezieht auch moderne Fortbewegungsmöglichkeiten ein. Das mieten von City Rollern oder Angebote zum Carsharing können einfach über dieses Portal verwaltet werden. Zudem ist das Informationsangebot rund um den allgemeinen Personenverkehr in der Stadt sehr Vielfältig. Es werden Informationen zu den Verfügbaren Taxiunternehmen der Stadt aufgelistet und allgemeine Verkehrsinformationen angezeigt. Außerdem können freie Parkplätze schnell und einfach eingesehen werden. Die Werbeflächen auf Bussen und Bahnen können Unternehmen der Stadt ebenfalls über dieses Portal buchen. Der Micro Service ÖPNV dient dem Bürger der Smart City als zentrale Anlaufstelle in Sachen Fortbewegung.

## 1.2 Ziele

Ziel dieses Microservices ist die Bereitstellung einer einheitlichen Plattform in Sachen Personennahverkehr für die Bürger der Smart City. Außerdem ist die vollständig digitale Abwicklung der Angebote umzusetzen(digitale Tickets für Bus/ Bahn, ... ), da man so etwas gegen die Umweltbelastung der Stadt tun kann.

# 2 Anforderungen

## 2.1 Stakeholder

| Funktion / Relevanz | Name | Kontakt / Verfügbarkeit | Wissen  | Interessen / Ziele  |
|---|---|---|---|---|
| Bürgermeister der Smart City | Konrad Bürgermeister | boss@smartcity.io | Kennt die Probleme des ÖPNV und die Politischen Interessen | Möchte das die Bürger zufrieden mit dem Angebot des ÖPNV sind |
| Leiter ÖPNV | Bernd Bus | bb@opnv.smartcity.io | 25 Jahre Erfahrung in ÖPNV Verwaltung | Zufriedene Kunden und Angestellte |



## 2.2 Funktionale Anforderungen

![UseCases Rettungsdienst](./img/UseCase.png)



## 2.3 Nicht-funktionale Anforderungen 

### 2.3.1 Rahmenbedingungen

```java
// TODO: Normen, Standards, Protokolle, Hardware, externe Vorgaben
```

### 2.3.2 Betriebsbedingungen
```java
// TODO: Vorgaben des Kunden (z.B. Web Browser / Betriebssystem Versionen, Programmiersprache)
```

### 2.3.3 Qualitätsmerkmale

Qualitätsmerkmal | sehr gut | gut | normal | nicht relevant
---|---|---|---|---
**Zuverlässigkeit** | | | | 
Fehlertoleranz |X|-|-|-
Wiederherstellbarkeit |-|X|-|-
Ordnungsmäßigkeit |X|-|-|-
Richtigkeit |X|-|-|-
Konformität |-|X|-|-
**Benutzerfreundlichkeit** | | | | 
Installierbarkeit |-|-|-|X
Verständlichkeit |X|-|-|-
Erlernbarkeit |-|X|-|-
Bedienbarkeit |X|-|-|-
**Performance** | | | | 
Zeitverhalten |-|X|-|-
Effizienz|-|-|X|-
**Sicherheit** | | | | 
Analysierbarkeit |-|-|X|-
Modifizierbarkeit |-|-|X|-
Stabilität |-|X|-|-
Prüfbarkeit |-|X|-|-

## 2.4 Graphische Benutzerschnittstelle

![startpage](img/mockups/startpage.png)

## 2.5 Anforderungen im Detail

| **Als** | **möchte ich** | **so dass** | **Akzeptanz** |
| :------ | :----- | :------ | :-------- |
| Bürger | die Taxiunternehmen der Stadt einsehen | ich mir ein Taxi rufen kann | Muss |
| Bürger | mir die aktuellen freien Parkplätze ansehen können | so das ich schnell einen Parkplatz finde | Muss |
| Bürger | mir die aktuellen Verkehrsinformationen anzeigen lassen | ich mich auf Verzögerungen einstellen kann | Kann |
| Bürger | mir die Fahrpläne von Bus und Bahn anzeigen lassen | ich weiß wann meine Linie abfährt und wo sie hält | Muss |
| Bürger | mir die verfügbaren City Roller der Stadt auf eine Karte anzeigen lassen | ich erkennen kann ob ein freier City Roller in meiner Nähe zu Verfügung steht | Kann |
| Bürger | mir die Carsharing Angebote anderer Bürger anschauen | ich mir eine Mitfahrgelegenheit suchen kann | Kann |
| Unternehmen | Werbeflächen (Bus/Bahn) mieten können | Werbung für mein Unternehmen in der Stadt veröffentlichen kann | Muss |
| Unternehmen | gemietete Werbeflächen (Bus/Bahn) wieder Freigeben können | ich diese nicht mehr bezahlen muss | Muss |
| Bürger | freie City Roller mieten und freigeben können | ich diese für einen bestimmten Zeitraum nutzen kann | Kann |
| Bürger | Fahrkarten für Bus und Bahn erwerben können | ich die öffentlichen Verkehrsmittel nutzen kann | Muss |
| Bürger | eine Monatskarte erwerben können | ich bei häufiger Nutzung des ÖPNV eine Vergünstigung erhalte | Muss |
| Bürger | Carsharing Angebote veröffentlichen, löschen und deaktivieren können | ich meine Carsharing angebote einfach verwalten kann | Kann |
| Bürger | mich mit meinem Account Einloggen und Ausloggen können | ich meine Daten einsehen kann und die ÖPNV Plattform nutzen kann | Muss |


# 3 Technische Beschreibung

## 3.1 Systemübersicht

![SysArch](/Users/alex/Git/sgse/Spezifikation/docs/alexander_bergmann/img/SysArch.png)

## 3.2 Softwarearchitektur

```java
// TODO: Darstellung von Softwarebausteinen (Module, Schichten, Komponenten)
```

## 3.3 Schnittstellen

Beispiel: Erstellen eines Carsharing Angebots mit GeoJSON

````json
"sgse.model.opnv.create_carsharing_offer": {
    "description": "Request to create a carsharing offer ",
    "fields": [
      {"name": "user_id", "type": "number", "required": true},
      {"name": "date", "type": "date", "required": true},
      {"name": "time", "type": "datetime", "required": true},
      {"name": "passengers", "type": "number", "required": true},
      {"name": "route", 
      	"type": {
      	"type": "FeatureCollection",
          "features": [
          {
            "type": "Feature",
            "properties": {
              "name": "Arbeitesstelle",
              "address": "Hochstr. 11",
              "marker-color": "#008800",
              "marker-symbol": "commercial"
            },
            "geometry": {
              "type": "Line",
              "coordinates": [7.0069, 51.1623],[16.0000, 32.1623]
            }
          }
        ]
      	}, 
      	"required": true}
    ]
}
````
Beispiel: Bearbeiten eines Carsharing Angebots

````json
"sgse.model.opnv.change_carsharing_offer": {
    "description": "Request to change a existing carsharing offer ",
    "fields": [
      {"name": "offer_id", "type": "number", "required": true},
      {"name": "date", "type": "date", "required": false},
      {"name": "time", "type": "datetime", "required": false},
      {"name": "passengers", "type": "number", "required": false},
      {"name": "route", 
      	"type": {
      	"type": "FeatureCollection",
          "features": [
          {
            "type": "Feature",
            "properties": {
              "name": "Arbeitesstelle",
              "address": "Hochstr. 11",
              "marker-color": "#008800",
              "marker-symbol": "commercial"
            },
            "geometry": {
              "type": "Line",
              "coordinates": [7.0069, 51.1623],[16.0000, 32.1623]
            }
          }
        ]
      	}, 
      	"required": true}
    ]
}
````


...



## 3.3.1 Ereignisse

```java
// TODO: In Event-gesteuerten Systemen: Definition der Ereignisse und deren Attribute
```

## 3.4 Datenmodell 

```java
// TODO: 

// Konzeptionelles Analyseklassendiagramm (logische Darstellung der Konzepte der Anwendungsdomäne)

// Modellierung des physikalischen Datenmodells ER-Diagramm oder JSON-Schema
```

## 3.5 Abläufe

```java
// TODO: 

// Aktivitätsdiagramme für relevante Use Cases

// Aktivitätsdiagramm für den Ablauf sämtlicher Use Cases
```

## 3.6 Entwurf

```java
// TODO: Detaillierte UML-Diagramme für relevante Softwarebausteine
```

## 3.7 Fehlerbehandlung 

```java
// TODO: Mögliche Fehler / Exceptions auflisten
```

## 3.8 Validierung

```java
// TODO: Relevante (Integrations)-Testfälle, die aus den Use Cases abgeleitet werden können
```

# 4 Projektorganisation

## 4.1 Annahmen

```java
// TODO: 

// Nicht durch den Kunden definierte spezifische Annahmen, Anforderungen und Abhängigkeiten

// Verwendete Technologien (Programmiersprache, Frameworks, etc.)

// Aufteilung in Repositories gemäß Software- und Systemarchitektur und Softwarebbausteinen

// Einschränkungen, Betriebsbedingungen und Faktoren, die die Entwicklung beeinflussen (Betriebssysteme, Entwicklungsumgebung)

// Interne Qualitätsanforderungen (z.B. Softwarequalitätsmerkmale wie z.B. Erweiterbarkeit)
```

## 4.2 Verantwortlichkeiten

Für alle Softwarebausteine und Komponenten des Microservice ist Alexander Bergmann zuständig.

### Rollen

#### Softwarearchitekt
Entwirft den Aufbau von Softwaresystemen und trifft Entscheidungen über das Zusammenspiel der Softwarebausteine.

#### Frontend-Entwickler
Entwickelt graphische oder andere Benutzerschnittstellen, insbesondere das Layout einer Anwendung.

#### Backend-Entwickler
Implementiert die funktionale Logik der Anwendung. Hierbei werden zudem diverse Datenquellen und externe Dienste integriert und für die Anwendung bereitgestellt.

### Rollenzuordnung

| Name     | Rolle     |
|----------|-----------|
| Alexander Bergmann | Softwarearchitekt |
| Alexander Bergmann | Backend-Entwickler |
| Alexander Bergmann | Frontend-Entwickler |

## 4.3 Grober Projektplan

### Meilensteine

- KW 43 (11.05)
  - Abgabe Pflichtenheft
- KW 45 (08.06) 
  - Implementierung
- KW 48 (03.07)
  - manuelle Abnahmetestss
  - Präsentation / Software-Demo


# 5 Anhänge




# Anforderungs- und Entwurfsspezifikation ("Pflichtenheft")

* Fitnesscenter, Malte Riechmann, Inhaltsverzeichnis
* Link zum Source Code Repository

# 1 Einführung

## 1.1 Beschreibung

* Projektname
* Darstellung der Produktvision in Prosa (5-10 Sätze)
* Ziele
* Für wen ist das Produkt/der Service?
* Was ist das Bedürfnis? 
* Was ist das Produkt/der Service?
* Warum sollte der Kunde dieses Produkt/den Service „kaufen“ oder nutzen?
* Im Gegensatz zu welchen anderen Produkten/Services steht dies?
* Was macht dieses Produkt/der Service anders?
* Warum ist das Projekt sinnvoll?
* Welche Stakeholder sind betroffen und wie stehen Sie zu der Projektidee?
* Welche alternativen Lösungsideen existieren für den identifizierten Bedarf?
* Wie hoch sind Aufwand und erwarteter Nutzen und stehen sie in einem sinnvollen Verhältnis? (Lohnt sich das Projekt?)
* Verfügen wir über die notwendigen Kompetenzen? (Umsetzbarkeit)
* Welche Risiken und negativen Nebeneffekte sind zu erwarten?

## 1.2 Ziele

- Anwendungsbereiche, Motivation, Umfang, Alleinstellungsmerkmale, Marktanforderungen
- Informationen zu Zielbenutzergruppen und deren Merkmale (Bildung, Erfahrung, Sachkenntnis)
- Abgrenzung (Was ist das Softwaresystem _nicht_)
- ggfs. SWOT-Analyse

# 2 Anforderungen

## 2.1 Stakeholder

| Funktion / Relevanz | Name | Kontakt / Verfügbarkeit | Wissen  | Interessen / Ziele  |
|---|---|---|---|---|
|  |   |   |    |   |


### Beispiel

| Funktion / Relevanz | Name | Kontakt / Verfügbarkeit | Wissen  | Interessen / Ziele  |
|---|---|---|---|---|
| Leiter der Bibliothek, Fachlicher Entscheider  |  Herr Bauer | Tel. 409000, Von 9-19 Uhr telefonisch erreichbar, Mitarbeit zu 30% möglich, Nürnberg  | Kennt das Altsystem aus der Anwendersicht, soll mit dem System arbeiten  | Vereinfachung der Ausleihprozesse  |
| Administrator, Informationslieferant bzgl. Wartungsanforderungen  | Herr Heiner  | Heiner@gmx.net, Per E-Mail, immer erreichbar, Verfügbarkeit 50%, Nürnberg  | Vertraut mit vergleichbarer Verwaltungssoftware   |  Stabiles System, geringer Wartungsaufwand |
| Product-Owner, Entscheider - als Koordinator der Stakeholderanforderungen   | Paul Ottmer  |  po@ottmer.de, Per E-Mail und tel. tagsüber, Verfügbarkeit 100%, Nürnberg  | Koordinator für die Inputs der Stakeholder  | ROI des Systems sicherstellen  |

## 2.2 Funktionale Anforderungen

**Kundenportal**

![UseCaseKunde](./img/kundenportal.png)

**Allgemeine Verwaltung**

![UseCaseVerwaltung](./img/verwaltung.png)

**Mitgliederverwaltung**

![UseCaseMitglieder](./img/mitgliederverwaltung.png)

**Trainer und Therapeuten Funktionen**

![UseCaseTrainerTherapeut](./img/trainer_therapeut.png)



## 2.3 Nicht-funktionale Anforderungen 

### 2.3.1 Rahmenbedingungen

- Normen, Standards, Protokolle, Hardware, externe Vorgaben

### 2.3.2 Betriebsbedingungen

- Vorgaben des Kunden (z.B. Web Browser / Betriebssystem Versionen, Programmiersprache)

### 2.3.3 Qualitätsmerkmale

- Externe Qualitätsanforderungen (z.B. Performance, Sicherheit, Zuverlässigkeit, Benutzerfreundlichkeit)

Qualitätsmerkmal | sehr gut | gut | normal | nicht relevant
---|---|---|---|---
**Zuverlässigkeit** | | | | |
Fehlertoleranz |X|-|-|-|
Wiederherstellbarkeit |X|-|-|-|
Ordnungsmäßigkeit |X|-|-|-|
Richtigkeit |X|-|-|-|
Konformität |-|X|-|-|
**Benutzerfreundlichkeit** | | | | |
Installierbarkeit |-|-|X|-|
Verständlichkeit |X|-|-|-|
Erlernbarkeit |-|X|-|-|
Bedienbarkeit |-|X|-|-|
**Performance** | | | | |
Zeitverhalten |-|-|X|-|
Effizienz|-|-|-|X|
**Sicherheit** | | | | |
Analysierbarkeit |X|-|-|-|
Modifizierbarkeit |-|-|-|X|
Stabilität |X|-|-|-|
Prüfbarkeit |X|-|-|-|

## 2.4 Graphische Benutzerschnittstelle

- GUI-Mockups passend zu User Stories
- Screens mit Überschrift kennzeichnen, die im Inhaltsverzeichnis zu sehen ist
- Unter den Screens darstellen (bzw. verlinken), welche User Stories mit dem Screen abgehandelt werden
- Modellierung der Navigation zwischen den Screens der GUI-Mockups als Zustandsdiagramm

## 2.5 Anforderungen im Detail

**Kundenportal**

| **In meiner Rolle als** | **möchte ich** | , **so dass** | **Erfüllt, wenn** | **Priorität** |
| :------ | :----- | :------ | :-------- | ------- |
| Kunde | die verschiedenen Geräte ansehen können | mein Trainingsmöglichkeiten besser einschätzen kann. | Geräte mit kurz Beschreibung angezeigt werden | hoch |
| Kunde | eine Liste der verschiedenen Kurse angezeigt bekommen | mehr Informationen über den jeweiligen Kurs erhalte. | Liste der Kurse mit Beschreibung angezeigt wird | hoch |
| Kunde | die Standorte anschauen können | die mehr über die verschiedenen Möglichkeiten erfahre. | Die verschiedenen Standorte angezeigt (und ausgewählt werden können) | mittel |
| Kunde | die verschiedenen Abonnement-Möglichkeiten ansehen können | für mich am besten passende Angebot auswählen kann. | Abonnements angezeigt werden | hoch |
| Kunde | einen Termin beim Physiotherapeuten beantragen können | behandelte werden kann. | Anmeldungsformular für Physiotherapeuten vorhanden | hoch |
| Kunde | einen neuen Trainingsplan beantragen können | ich mein Training an meine aktuelle Verfassung anpassen kann. | Antragsformular für Trainingsplan vorhanden | hoch |
| Kunde | meine Trainingspläne  einsehen können | ich meine Fortschritte sehen kann. | Persönlicher Trainingsplan angezeigt wird | hoch |

**Allgemeine Verwaltung**

| **In meiner Rolle als** | **möchte ich** | , **so dass** | **Erfüllt, wenn** | **Priorität** |
| :------ | :----- | :------ | :-------- | ------- |
| Trainer/ Chef/ Physiotherapeut | neue Geräte hinzufügen können | Kunden diese ansehen und sich informieren können | Gerät hinzugefügt | mittel |
| Trainer/ Chef/ Physiotherapeut | bestehende Geräte ändern können | Fehler oder neue Erkenntnisse eingefügt werden | Gerät geändert | mittel |
| Trainer/ Chef/ Physiotherapeut | alte Geräte entfernen können | Kunden keine Geräte angezeigt bekommen, die nicht vorhanden sind | Gerät entfernt | mittel |
| Trainer/ Chef/ Physiotherapeut | neue Kurse hinzufügen können | Kunde neue Angebote angezeigt bekommen | Kurs hinzugefügt | mittel |
| Trainer/ Chef/ Physiotherapeut | bestehende Kurse ändern können | Neuerungen im Programm für Kunden einsehbar sind | Kurs geändert | mittel |
| Trainer/ Chef/ Physiotherapeut | alte Kurse entfernen können | Kunden keine Kurse angezeigt bekommen, die nicht vorhanden sind | Kurs entfernt | mittel |
| Trainer/ Chef/ Physiotherapeut | neue Abonnement hinzufügen können | Kunden unser Angebote einsehen können. | Abonnement hinzugefügt | mittel |
| Trainer/ Chef/ Physiotherapeut | bestehende Abonnement ändern können | Änderungen bezüglich der Abonnements eingestellt werden können | Abonnement geändert | mittel |
| Trainer/ Chef/ Physiotherapeut | alte Abonnement entfernen können | Kunden keine Abonnements angezeigt bekommen, die nicht vorhanden sind | Abonnement entfernt | mittel |

**Mitgliederverwaltung**

| **In meiner Rolle als** | **möchte ich** | , **so dass** | **Erfüllt, wenn** | **Priorität** |
| :------ | :----- | :------ | :-------- | ------- |
| Trainer/ Chef/ Physiotherapeut | neue Mitglieder einfügen können | neue Kunden verzeichnet werden und sie die verschiedenen Angebote annehmen können | Mitglied eingefügt werden | hoch |
| Trainer/ Chef/ Physiotherapeut | Mitglieder ansehen können | ich die jeweiligen Mitglieder optimal beraten kann | Mitglieder angezeigt werden | hoch |
| Trainer/ Chef/ Physiotherapeut | Mitglieder bearbeiten können | ich neue Information einfügen und veraltete entfernen kann | Mitglieder werden bearbeitet | hoch |
| Trainer/ Chef/ Physiotherapeut | Mitglieder entfernen können | Persönlich Daten nicht gespeichert werden müssen, wenn es nicht nötig ist | Mitglieder werden gelöscht | hoch |
| Chef | Trainerrollen vergeben können | neue Trainer alle wichtige Funktionen nutzen können | Trainerrolle hinzufügen | mittel |
| Chef | Trainerrollen entfernen können | ehemalige Trainer keinen Zugriff auf persönliche Daten haben | Trainerrolle entfernen | mittel |
| Chef | Physiotherapeuten-rolle vergeben können | neue Physiotherapeuten alle wichtige Funktionen nutzen können | Physiotherapeuten hinzufügen | mittel |
| Chef | Physiotherapeuten-rolle entfernen können | ehemalige Physiotherapeuten keinen Zugriff auf persönliche Daten haben | Physiotherapeuten entfernen | mittel |
| Chef | neue Chefs hinzufügen können | neue Führungspersonen auf alle Funktionen zugreifen können | Chef hinzufügen | niedrig |
| Chef | Chefs entfernen können | ehemalige Führungspersonen keinen Zugriff auf persönliche Daten haben | Chef entfernen | niedrig |

**Trainer und Therapeuten Funktionen**

| **In meiner Rolle als** | **möchte ich** | , **so dass** | **Erfüllt, wenn** | **Priorität** |
| :------ | :----- | :------ | :-------- | ------- |
| Trainer/ Physiotherapeut | Mitgliedern neue Trainingspläne hinzufügen können | diese und ihr neues Trainingsprogramm einsehen können | Trainings-plan eingefügt        | hoch |
| Trainer/ Physiotherapeut | Trainingsplänen von Mitgliedern ändern können | auf Rück- und Fortschritte eingegangen werden kann | Trainings-plan geändert | hoch |
| Trainer/ Physiotherapeut | die Anträge für neue Trainingspläne ansehen können | erste Ideen auf Grundlage der Anamnese vorbereitet werden können | Training-plan-anträge angezeigt | hoch |
| Physiotherapeut | die Kunden-Behandlungsakte einsehen können | ich die Behandlung basierten auf diesen Daten anpassen kann | Akte angezeigt | mittel |
| Physiotherapeut | die Kunden-Behandlungsakte bearbeiten können | ich neue Erkenntnisse für Folgebehandlungen speichern kann | Akte geändert | mittel |
| Physiotherapeut | die Anmeldungen zur Therapie ansehen können | ein Termin vereinbaren zu können und eine erste Behandlung auf Grundlage der Anamnese erstellen kann | Termin-anfrage angezeigt | mittel |

# 3 Technische Beschreibung

## 3.1 Systemübersicht

- Systemarchitekturdiagramm ("Box-And-Arrow" Diagramm)
- Kommunikationsprotokolle, Datenformate

## 3.2 Softwarearchitektur

- Darstellung von Softwarebausteinen (Module, Schichten, Komponenten)

## 3.3 Schnittstellen

- Schnittstellenbeschreibung (API)
- Auflistung der nach außen sichtbaren Schnittstelle der Softwarebausteine

## 3.3.1 Ereignisse

- In Event-gesteuerten Systemen: Definition der Ereignisse und deren Attribute

## 3.4 Datenmodell 

- Konzeptionelles Analyseklassendiagramm (logische Darstellung der Konzepte der Anwendungsdomäne)
- Modellierung des physikalischen Datenmodells 
  - RDBMS: ER-Diagramm bzw. Dokumentenorientiert: JSON-Schema

## 3.5 Abläufe

- Aktivitätsdiagramme für relevante Use Cases
- Aktivitätsdiagramm für den Ablauf sämtlicher Use Cases

## 3.6 Entwurf

- Detaillierte UML-Diagramme für relevante Softwarebausteine

## 3.7 Fehlerbehandlung 

* Mögliche Fehler / Exceptions auflisten

## 3.8 Validierung

* Relevante (Integrations)-Testfälle, die aus den Use Cases abgeleitet werden können

# 4 Projektorganisation

## 4.1 Annahmen

- Nicht durch den Kunden definierte spezifische Annahmen, Anforderungen und Abhängigkeiten
- Verwendete Technologien (Programmiersprache, Frameworks, etc.)
- Aufteilung in Repositories gemäß Software- und Systemarchitektur und Softwarebbausteinen 
- Einschränkungen, Betriebsbedingungen und Faktoren, die die Entwicklung beeinflussen (Betriebssysteme, Entwicklungsumgebung)
- Interne Qualitätsanforderungen (z.B. Softwarequalitätsmerkmale wie z.B. Erweiterbarkeit)

## 4.2 Verantwortlichkeiten

- Zuordnung von Personen zu Softwarebausteinen aus Kapitel 3.1 und 3.2
- Rollendefinition und Zuordnung

| Softwarebaustein | Person(en) |
|----------|-----------|
| Komponente A | Thomas Mustermann |

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
| Thomas Mustermann | Softwarearchitekt |


## 4.3 Grober Projektplan

- Meilensteine

### Meilensteine
* KW 43 (21.10)
  * Abgabe Pflichtenheft
* KW 44 (28.10) / Projekt aufsetzen
  * Repository Struktur
* KW 45 (4.11) / Implementierung
  * Implementierung #3 (Final)
* KW 48 (18.12) / Abnahmetests
  * manuelle Abnahmetestss
  * Präsentation / Software-Demo

# 5 Anhänge

## 5.1 Glossar 

- Definitionen, Abkürzungen, Begriffe

## 5.2 Referenzen

- Handbücher, Gesetze

## 5.3 Index




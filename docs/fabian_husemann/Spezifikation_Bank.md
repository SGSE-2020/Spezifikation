# Anforderungs- und Entwurfsspezifikation - SmartCity - Bank

* Titel: SmartCity - Bank

* Autor: Fabian Husemann

* Repository: [Repo](https://github.com/SGSE-2020/MS_Bank.git)

   

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
| Kundenberatung | Fabian Husemann | Tel.: 0400805 4646 <br />Email: fabian@husemann-web.de<br />von 8 - 20 Uhr erreichbar | Kennt sich mit dem Bankportal gut aus | Gute Kundenübersicht,  Einfacher Kontakt mit Kunden |

## 2.2 Funktionale Anforderungen

## ![uc diagram](./img/Benutzer_Story.jpg)

![uc diagram](./img/Admin_Story.jpg)



## 2.3 Nicht-funktionale Anforderungen 

### 2.3.1 Rahmenbedingungen

* Kommunikation
  * Synchron: gRPC
  * Asynchron: RabbitMQ
* WebAnwendung

### 2.3.2 Betriebsbedingungen

* Um auf den MicroService: Bank zu zugreifen, muss über einen Browser die URL aufgerufen werden.

* Als Client kann dabei ein Computer oder auch eine Handy Browser benutzt werden.

  

### 2.3.3 Qualitätsmerkmale

| Qualitätsmerkmal           | sehr gut | gut  | normal | nicht relevant |
| -------------------------- | -------- | ---- | ------ | -------------- |
| **Zuverlässigkeit**        |          |      |        |                |
| Fehlertoleranz             | X        | -    | -      | -              |
| Wiederherstellbarkeit      | -        | -    | X      | -              |
| Ordnungsmäßigkeit          | X        | -    | -      | -              |
| Richtigkeit                | X        | -    | -      | -              |
| Konformität                | -        | X    | -      | -              |
| **Benutzerfreundlichkeit** |          |      |        |                |
| Installierbarkeit          | -        | X    | -      | -              |
| Verständlichkeit           | X        | -    | -      | -              |
| Erlernbarkeit              | -        | -    | X      | -              |
| Bedienbarkeit              | -        | X    | -      | -              |
| **Performance**            |          |      |        |                |
| Zeitverhalten              | -        | X    | -      | -              |
| Effizienz                  | -        | X    | -      | -              |
| **Sicherheit**             |          |      |        |                |
| Analysierbarkeit           | -        | -    | X      | -              |
| Modifizierbarkeit          | -        | -    | X      | -              |
| Stabilität                 | X        | -    | -      | -              |
| Prüfbarkeit                | -        | X    | -      | -              |

## 2.4 Graphische Benutzerschnittstelle

#### Login

![Bank Login](./img/Login.png)

#### Überschicht ( Hauptseite )

![Kontoübersicht](./img/Übersicht.png)

#### Kontoübersicht

![](./img/Kontoübersicht.png)

#### Konteneinstellungen

![Kontoübersicht](./img/Kontoeinstellung.png)

#### Überweisungen

![Kontoübersicht](./img/Überweisungen.png)

#### Ein-/Auszahlungen

![Kontoübersicht](./img/Ein-_Auszahlung.png)

#### Kontakt

![Kontoübersicht](./img/Kontakt.png)



## 2.5 Anforderungen im Detail

#### Benutzer

| **Als**  | **möchte ich**                        | **so dass**                                      | **Akzeptanz**                  | Priorität |
| :------- | :------------------------------------ | :----------------------------------------------- | :----------------------------- | --------- |
| Benutzer | mein Konto gründen                    | ich Geld sparen kann                             | Online Website                 | hoch      |
| Benutzer | mein Kontostand abrufen               | ich weiß wieviel Geld auf meinem Konto ist       | Online Website                 | hoch      |
| Benutzer | mein Geld einzahlen                   | ich Geld auf meinem Konto habe                   | Online Website                 | hoch      |
| Benutzer | mein Geld auszahlen                   | ich Bargeld in meiner Tasche habe                | Online Website                 | hoch      |
| Benutzer | Geld zu anderen Benutzern schicken    | ich jemand anderen Geld geben kann               | Online Website/ Überweisungen  | hoch      |
| Benutzer | Berater Kontaktieren                  | mein Konto Bearbeiten kann                       | Online Website/ Kunden Service | mittel    |
| Benutzer | mich sicher Einloggen                 | kein anderer auf mein Konto zugreifen kann       | Online Website                 | hoch      |
| Benutzer | mein Konto auch Rückblickend einsehen | ich weiß wo mein Geld diesen Monat geblieben ist | Online Website                 | mittel    |
| Benutzer | mir Geld leihen                       | ich an Geld komme wenn ich es brauche            | Online Website                 | mittel    |

#### Administrator


| **Als**       | **möchte ich**                                               | **so dass**                                                  | **Akzeptanz** | Priorität |
| ------------- | :----------------------------------------------------------- | :----------------------------------------------------------- | :------------ | --------- |
| Administrator | mir eine Kundenliste anzeigen                                | alle Kunden auf einem Überblick sehe                         | Admin Zugriff | hoch      |
| Administrator | von Kunden kontaktiert werden                                | ich alle Kunden zufrieden stellen kann                       | Admin Zugriff | mittel    |
| Administrator | mir eine Liste von Kunden anzeigen die sich Geld leihen wollen | ich ihre Konten einsehen kann und ihn ein Darlehen gewähren kann. | Admin Zugriff | mittel    |
| Administrator | Kunden Konten einsehen                                       | einen Überblick über die Kunden Konten habe                  | Admin Zugriff | hoch      |
| Administrator | Kunden Konten bearbeiten                                     | der Kunde sein Konto einstellen kann                         | Admin Zugriff | hoch      |

# 3 Technische Beschreibung

## 3.1 Systemübersicht

![Systemübersicht](./img/Systemübersicht.png)

## 3.2 Softwarearchitektur

![Softwarearchitektur](./img/Systemarchitektur.png)

## 3.3 Schnittstellen

### Überweisung tätigen

```json
"bank.ueberweisung":{
    "iban": "DE46 4585 4585 2000 5145 20",
    "purpose": "Einkauf",  
    
    "dest_name": "Supermarkt",
    "dest_iban": "DE46 7845 2998 2554 8461 20",
    "amount": "20.00",
}
```

### Terminale Überweisung tätigen

```json
"bank.ueberweisung":{
    "iban": "DE46 4585 4585 2000 5145 20",
    "purpose": "Einkauf",  
    
    "name": "Supermarkt",
    "dest_iban": "DE46 7845 2998 2554 8461 20",
    "amount": "20.00",
    "start_date": "07.05.2020",
    "repeat": "monthly | daily | yearly"
}
```



* Zugriff auf jedes Microservice mit Geldanbindung

## 3.4 Datenmodell

## 3.5 Abläufe

## 3.6 Entwurf

## 3.7 Fehlerbehandlung 

## 3.8 Validierung

# 4 Projektorganisation

## 4.1 Annahmen

## 4.2 Verantwortlichkeiten

### Rollen

#### Softwarearchitekt

#### Frontend-Entwickler

#### Backend-Entwickler

### Rollenzuordnung

## 4.3 Grober Projektplan

### Meilensteine

# 5 Anhänge

## 5.1 Glossar

- Definitionen, Abkürzungen, Begriffe

## 5.2 Referenzen

- Handbücher, Gesetze

## 5.3 Index

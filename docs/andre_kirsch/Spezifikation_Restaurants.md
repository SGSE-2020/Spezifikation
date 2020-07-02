# Restaurants - Anforderungs- und Entwurfsspezifikation

* Titel: SmartCity - Restaurants
* Autor: André Kirsch
* https://github.com/SGSE-2020/MS_Restaurants

# 1 Einführung

## 1.1 Beschreibung

Restaurants sind zentrale Punkte des öffentlichen Lebens in einer Stadt. Mit dem SmartCity Service **Restaurants** können Restaurants sich online vorstellen und ihre Produkte anbieten. Besucher der Webseite können sich über einzelne Restaurants informieren und Bestellungen tätigen sowie Tische reservieren. Restaurantbesitzer können ihre Restaurants online einstellen und präsentieren. Die Webseite bietet Restaurantbesitzern einen neuen Weg der Vermarktung.

## 1.2 Ziele

Der SmartCity Service Restaurant soll Restaurantbesitzer ermöglichen, eine Online Plattform für ihr Restaurant aufzubauen. Dabei soll es grundlegende Einstellungsmöglichkeiten für Restaurantbesitzer geben. Andere Besucher der Online Plattform sollen Informationen zu eingetragenen Restaurants finden und Bestellungen aufgeben können. Im Unterschied zu einzelnen Webseiten von Restaurants befindet sich auf dieser Webseite eine Auswahl mehrerer Restaurants einer bestimmten Smart City.

# 2 Anforderungen

## 2.1 Stakeholder

| Funktion / Relevanz | Name | Wissen  | Interessen / Ziele  |
|---|---|---|---|
| Restaurantkunde, der Bestellungen tätigen und Tische reservieren möchte | Kunde | Hat Grundwissen beim Bestell- und Reservierungsprozess | Möchte sich über ein Restaurant informieren, Bestellungen aufgeben oder Tische reservieren |
| Restaurantbesitzer, der sein Restaurant im Internet vorstellen möchte | Restaurantbesitzer | Weiß vllt schon, wie er mit der Webseite umgehen muss. Ist aber vorsichtig, weil er nichts falsch machen möchte | Möchte sein Restaurant im Internet vorstellen und über das Internet mit dem Restaurant Geld verdienen |

## 2.2 Funktionale Anforderungen

##### Kundenportal

![UseCases_User](img\UseCases_User.png)

##### Restaurantverwaltung

![UseCases_Besitzer](img\UseCases_Besitzer.png)

## 2.3 Nicht-funktionale Anforderungen 

### 2.3.1 Rahmenbedingungen

Im Frontend wird Vue.js als Framework verwendet. Das Backend ist zum einen ein Server, der die Webseite zur Verfügung stellt und eine NodeJS Applikation, welche eine REST Schnittstelle und eine gRPC Schnittstelle bereitstellt. Sollten Nachrichten asynchron verschickt und abgerufen werden, wird RabbitMQ verwendet. Abschließend ist eine MongoDB Datenbank an das Backend angebunden.

### 2.3.2 Betriebsbedingungen

Der Benutzer soll mithilfe eines Browser auf die Anwendung als Webseite zugreifen können. Der Zugriff über den Browser soll dabei über PC, Tablet und Smartphone erfolgen können. Die Bedingung für den vollfunktionsfähigen Zugriff auf die Webseite ist die Verwendung einer aktuellen Browserversion.

### 2.3.3 Qualitätsmerkmale

Qualitätsmerkmal | sehr gut | gut | normal | nicht relevant
---|---|---|---|---
**Zuverlässigkeit** | | | | 
Fehlertoleranz | X        |-| -      |-
Wiederherstellbarkeit | X        |-| -      |-
Ordnungsmäßigkeit | X        |-|-|-
Richtigkeit | X        |-| -      |-
Konformität |-|X|-|-
**Benutzerfreundlichkeit** | | | | 
Installierbarkeit |-|-|-| X              
Verständlichkeit |X|-|-|-
Erlernbarkeit |X|-|-|-
Bedienbarkeit |X|-|-|-
**Performance** | | | | 
Zeitverhalten |-|X|-|-
Effizienz|-| X   | - |-
**Sicherheit** | | | | 
Analysierbarkeit |-|-|X|-
Modifizierbarkeit |-|-|-|X
Stabilität |-|X|-|-
Prüfbarkeit |-|-|X|-

## 2.4 Graphische Benutzerschnittstelle

### Home

![home](img\mockups\home.png)

(Restaurantliste einsehen)

### Restaurant erstellen

![restauranterstellen](img\mockups\restauranterstellen.png)

(Restaurant eintragen)

### Restaurantübersicht

![restaurant](img\mockups\restaurant.png)

(Speisekarte einsehen, Öffnungszeiten einsehen, Bewertungen einsehen, Restaurant bewerten, Restaurantauslastung einsehen, Parkplatzauslastung einsehen)

### Tisch reservieren

![tisch_reservieren](img\mockups\tisch_reservieren.png)

(Tisch reservieren, Parkplatz reservieren, Terminkollision überprüfen)

### Bestellung aufgeben

![bestellung](img\mockups\bestellung.png)

(Nach Hause bestellen)

### Bestellbestätigung

![bestellbestaetigung](img\mockups\bestellbestaetigung.png)

(Nach Hause bestellen)

### Restaurantübersicht als Restaurantbesitzer

![restaurantbesitzer](img\mockups\restaurantbesitzer.png)

### Speise bearbeiten/hinzufügen

![speisebearbeitenhinzufgen](img\mockups\speisebearbeitenhinzufgen.png)

(Speisekarte eintragen)

### Restaurantinfos bearbeiten

![restaurantinfosbearbeiten](img\mockups\restaurantinfosbearbeiten.png)

(Öffnungszeiten eintragen, Tischdaten eintragen, Restaurantlogo einfügen, Bestellungen erlauben, Reservierungen erlauben)

### Bestellliste

![bestellliste](img\mockups\bestellliste.png)

(Bestellungen einsehen, Bestellungen annehmen, Bestellungen abschließen)

### Restaurantangebot veröffentlichen

![restaurantangebote](img\mockups\restaurantangebote.png)

(Restaurantangebote im Bürgerbüro teilen)

### Lebensmittelbestellung

![lebensmittelbestellung](img\mockups\lebensmittelbestellung.png)

(Lebensmittel bestellen)

## 2.5 Anforderungen im Detail

#### Benutzer

| **Name**                      | **In meiner Rolle als**... | ...**möchte ich**...                                         | ..., **so dass**...                                          | **Erfüllt, wenn**...                                         | **Priorität** |
| :---------------------------- | :------------------------: | :----------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- | :------------ |
| Restaurantliste einsehen      |          Benutzer          | eine Liste mit allen Restaurants in meiner Stadt und zusätzlichen Informationen zu diesen Restaurants einsehen | ich weiß, welche Restaurants in der Stadt existieren und welche sich aktuell lohnen zu besuchen. | die Restaurantliste einsehbar ist.                           | Muss          |
| Speisekarte einsehen          |          Benutzer          | die Speisekarte zu einem von mir ausgewählten Restaurant angezeigt bekommen | ich sehen kann, welche Gerichte in diesem Restaurant bestellt werden können. | die Speisekarte zu jedem Restaurant einsehbar ist.           | Muss          |
| Öffnungszeiten einsehen       |          Benutzer          | die Öffnungszeiten zu einem von mir ausgewählten Restaurant angezeigt bekommen | ich sehen kann, wann das Restaurant geöffnet hat.            | die Öffnungszeiten zu jedem Restaurant einsehbar sind.       | Muss          |
| Bewertungen einsehen          |          Benutzer          | die Bewertungen eines Restaurants von anderen Nutzern angezeigt bekommen | ich sehen kann, wie gut das Restaurant bewertet wurde        | die Bewertungen zu jedem Restaurant einsehbar sind.          | Muss          |
| Tisch reservieren             |          Benutzer          | bei einem ausgewählten Restaurant einen Tisch für eine von mir ausgewählte Anzahl an Personen für einen bestimmten Zeitpunkt reservieren | dieser Tisch verfügbar ist, wenn ich mit meiner Gruppen zu dem gegebenen Zeitpunkt in dem Restaurant essen möchte | Tische über die Webseite reserviert werden können.           | Muss          |
| Restaurantauslastung einsehen |          Benutzer          | einsehen können, wie stark aktuell die Restaurantauslastung in einem Restaurant ist und wie viele Plätze in dem Restaurant noch frei sind | ich besser einschätzen kann, ob sich aktuell ein Besuch bei dem Restaurant lohnt. | die Restaurantauslastungen und die Anzahl freier Tische einsehbar ist | Kann          |
| Terminkollision überprüfen    |          Benutzer          | , dass ich bei der Reservierung eines Tisches in einem Restaurant gewarnt werde, wenn in meinem Kalender eine Kollision mit einem anderen Termin existiert | ich zu dem gegebenen Zeitpunkt zusätzlich bestätigen muss, dass ich einen Tisch reservieren möchte. | bei Terminkollision eine zusätzliche Abfrage existiert.      | Muss          |
| Nach Hause bestellen          |          Benutzer          | eine Bestellung in einem Restaurant, welches Lieferungen unterstützt, aufgeben und online bezahlen | mir diese Bestellung nach Hause geliefert wird.              | Gerichte bestellt und bezahlt werden können.                 | Muss          |
| Parkplätze reservieren        |          Benutzer          | angeben können, ob und wie viele Parkplätze bei einer Tischreservierung in der Nähe des Restaurants mit reserviert werden können | ich bei der Ankunft am Restaurant keinen Parkplatz suchen muss. | Parkplatzreservierung mit Anzahl angegeben werden kann.      | Muss          |
| Parkplatzauslastung einsehen  |          Benutzer          | die Parkplatzauslastung am Restaurant einsehen können        | ich weiß, ob ich in der Nähe noch einen Parkplatz finden kann. | die Parkplatzauslastung einsehbar ist.                       | Kann          |
| Restaurants bewerten          |          Benutzer          | Restaurants bewerten können                                  | andere einsehen können, welche Restaurants gut sind.         | die Restaurantbewertungen einsehbar sind.                    | Muss          |

#### Administrator


| **Name**                                | **In meiner Rolle als**... | ...**möchte ich**...                                         | ..., **so dass**...                                          | **Erfüllt, wenn**...                                         | **Priorität** |
| :-------------------------------------- | :------------------------: | :----------------------------------------------------------- | :----------------------------------------------------------- | :----------------------------------------------------------- | :------------ |
| Restaurant eintragen                    |     Restaurantbesiter      | mein Restaurant eintragen können                             | andere Personen sehen können, dass es mein Restaurant in der Stadt gibt. | neue Restaurants eingetragen werden können.                  | Muss          |
| Speisekarte eintragen                   |     Restaurantbesitzer     | die Speisekarte meines Restaurants eintragen und ändern können | andere Personen sehen können, welche Gerichte in meinem Restaurant angeboten werden. | Gerichte eingefügt, geändert und gelöscht werden können.     | Muss          |
| Öffnungszeiten eintragen                |     Restaurantbesitzer     | die Öffnungszeiten meines Restaurants eintragen können       | andere Personen wissen, wann mein Restaurant geöffnet ist.   | Öffnungszeiten eintragbar und von anderen Personen einsehbar sind. | Muss          |
| Tischdaten eintragen                    |     Restaurantbesitzer     | Tischanzahl und -größe eintragen können                      | Benutzer Tische reservieren kann.                            | Tische reserviert werden können.                             | Muss          |
| Parkplätze verlinken                    |     Restaurantbesitzer     | Parkplätze verlinken können                                  | Benutzer Parkplatzreservierungen bei Tischreservierungen vornehmen können. | Parkplätze reserviert werden können.                         | Muss          |
| Restaurantlogo einfügen                 |     Restaurantbesitzer     | das Restaurantlogo hochladen können                          | Besucher der Webseite das Restaurant anhand des Logos erkennen können. | Logo hochgeladen werden kann.                                | Kann          |
| Bestellungen erlauben                   |     Restaurantbesitzer     | Online-Bestellungen erlauben können                          | andere Personen in meinem Restaurant online Gerichte bestellen und bezahlen können. | Gerichte online bestellt und bezahl werden können und der Restaurantbesitzer diese Funktion aktivieren/deaktivieren kann. | Muss          |
| Reservierungen erlauben                 |     Restaurantbesitzer     | Reservierungen erlauben könne                                | andere Personen Tische in meinem Restaurant reservieren können | Tisch reserviert werden können und der Restaurantbesitzer diese Funktion aktivieren/deaktivieren kann. | Muss          |
| Bestellungen einsehen                   |     Restaurantbesitzer     | Online-Bestellungen einsehen können                          | ich weiß, wann ein Besucher der Webseite eine Bestellung aufgegeben hat. | Bestellungen auf der Webseite eingesehen werden können.      | Muss          |
| Bestellungen annehmen                   |     Restaurantbesitzer     | Online-Bestellungen annehmen können                          | die Bestellung geliefert werden kann.                        | Bestellungen auf der Webseite angenommen werden können       | Muss          |
| Bestellungen abschließen                |     Restaurantbesitzer     | Online-Bestellungen abschließen können                       | die Bestellung erfüllt werden kann.                          | Bestellungen auf der Webseite abgeschlossen werden können    | Muss          |
| Restaurantangebote im Bürgerbüro teilen |     Restaurantbesitzer     | spezielle Angebote in einem Restaurant an das Bürgerbüro senden | andere Personen dort diese Angebote sehen können.            | Angebote können an das Bürgerbüro gesendet werden.           | Kann          |
| Lebensmittel bestellen                  |     Restaurantbesitzer     | Lebensmittel im Supermarkt bestellen                         | man nicht selber zum Supermarkt laufen muss                  | Bestellungen gemacht werden können                           | Muss          |

# 3 Technische Beschreibung

## 3.1 Systemübersicht

![Systemarchitektur](img\Systemarchitektur.png)

## 3.2 Softwarearchitektur

![softwarearchitekturdiagramm](img\softwarearchitekturdiagramm.png)

## 3.3 Schnittstellen

##### Terminkollision überprüfen

Mit dieser Schnittstelle soll ein anderer Microservice überprüfen können, ob ein Benutzer zu einem bestimmten Zeitpunkt einen Tisch in einem Restaurant reserviert hat. Damit hat der Microservice die Möglichkeit eine Warnung auszugeben, wenn bei diesem ein Termin für den Benutzer erstellt werden soll, dieser aber zu dem Zeitpunkt keine Zeit hat. (*timespan soll in Minuten angegeben werden)

```json
"sgse.model.restaurants.appointment": {
	"description": "Check whether a user has made a reservation at a given time.",
	"fields": {
	    {"name": "uuid", "type": "string", "required": true},
    	{"name": "time", "type": "datetime", "required": true},
	    {"name": "timespan", "type": "int", "required": false, "default": 120}
	}
}
```

### 3.3.1 Ereignisse

##### Neues Restaurant erstellt

Dieses Ereignis wird versendet, wenn ein Besucher auf der Restaurant Webseite ein neues Restaurant erstellt.

```json
"sgse.model.restaurants.new_restaurant": {
    "description": "A new restaurant has been created",
    "fields": {
        {"name": "restaurant_name", "type": "string"},
        {"name": "owner", "type": "string"},
        {"name": "creation_date", "type": "datetime"}
    }
}
```



## 3.4 Datenmodell

![erm](img\erm.png)

## 3.5 Abläufe

##### Gerichte bestellen

![activity_diagram_1](img\activity_diagram_1.png)

##### Tisch reservieren

![activity_diagram_2](img\activity_diagram_2.png)

##### Restaurant erstellen

![activity_diagram_3](img\activity_diagram_3.png)

## 3.6 Entwurf

## 3.7 Fehlerbehandlung 

## 3.8 Validierung

# 4 Projektorganisation

## 4.1 Annahmen

- Das Projekt wird als Microservice implementiert
- Der Microservice unterteilt sich in die drei Container Frontend, Backend, Datenbank

##### Frontend

- Vue.js

##### Backend

- NodeJS
- Express

##### Datenbank

- MongoDB

## 4.2 Grober Projektplan

### Meilensteine

- Erstellung Repositories
  - Di, 21.04.2020
- Abgabe Software-Spezifikation
  - Mo, 11.05.2020
- Abgabe Softwareprodukt (Version 0)
  - Erste lauffähige Version
  - Mo, 08.06.2020
- Abgabe Softwareprodukt
  - Voll funktionsfähig
  - Mit Präsentation/Demo
  - Do, 03.07.2020

# 5 Anhänge

## 5.1 Glossar

- Definitionen, Abkürzungen, Begriffe

## 5.2 Referenzen

- Handbücher, Gesetze

## 5.3 Index

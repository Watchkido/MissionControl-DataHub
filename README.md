# Multisensor-System für Wetterstation und Raumschiff-Simulation

## Projektbeschreibung

Dieses Projekt verbindet mehrere Mikrocontroller (Arduino YUN, Arduino Mega, Arduino Uno, ESP32-CAM) sowie einen Raspberry Pi 3B zu einem zentralisierten System zur **Erfassung, Speicherung und Visualisierung von Sensordaten**.

**Anwendungsgebiete:**

- Wetterdaten-Erfassung auf einem Balkon
- Raumschiff-Simulation für ein Spiel basierend auf realen Sensorwerten

**Datenbanken:**

- **SQLite** (lokal auf dem Raspberry Pi)
- **PostgreSQL/MySQL** (lokal auf dem Raspberry Pi)

Anschließend erfolgt die **Abrufbarkeit und Visualisierung** über eine Weboberfläche.

---

## Zielsetzung

- Robuste Erfassung von Umweltdaten (Temperatur, Feuchtigkeit, Radioaktivität etc.)
- Zentrale Speicherung der Daten in zwei unterschiedlichen Datenbanksystemen
- Live-Visualisierung der Daten auf einer Weboberfläche
- Simulationslogik für ein "Raumschiff-Spiel" basierend auf realen Sensorwerten
- Offene und modulare Architektur für zukünftige Erweiterungen

---

## Systemarchitektur

```
[Sensoren] → [Arduinos/ESP32] → [Raspberry Pi] → [SQLite + PostgreSQL/MySQL] → [Webserver + Frontend]
```

- **Kommunikation:** Seriell (USB) zwischen Arduinos und Raspberry Pi
- **Datenübertragung:** JSON-Format über Serial-Port
- **Server:** Raspberry Pi mit Python-Skripten, Apache2 oder Nginx
- **Frontend:** HTML/JavaScript (AJAX oder WebSockets)

---

## Hardware-Komponenten
- 1x Optional Sensordaten aus Smartphone
- 1× Arduino YUN
- 1× Arduino Mega
- 1× Arduino Uno
- 1× ESP32-CAM
- 2× WLAN-Module
- 1× NanoVNA (geplant)
- 1× Sensor für Radioaktivität
- 1× Raspberry Pi 3B
- 1× Lafivin 4-Zoll TFT-Display
- 1× Sensor Kit V2.0 (37 Sensoren, Elegoo)
- 1× Expansion Board für Raspberry Pi

---

## Software-Komponenten

- **Betriebssystem:** Raspberry Pi OS (Debian-basiert)
- **Programmiersprachen:** Python 3, HTML, JavaScript
- **Datenbanken:** SQLite, PostgreSQL/MySQL
- **Webserver:** Apache2 oder Nginx
- **Zusatztools:** Node-RED (optional), MQTT (optional)

---

## Funktionsübersicht

| Funktion                  | Beschreibung |
|----------------------------|--------------|
| Sensordaten-Erfassung      | Kontinuierliches Sammeln aller Sensorwerte |
| Lokale Speicherung         | Rohdaten-Speicherung in SQLite |
| Langfristige Speicherung   | Redundante Speicherung in PostgreSQL/MySQL |
| Live-Visualisierung        | Webseite zeigt aktuelle Sensordaten in Echtzeit |
| Alarm- und Eventsystem     | Simulation von Notfallsituationen im Spiel |
| Bedienoberfläche           | Steuerung über Touch-Display geplant (TFT) |

---

Projektphasen
Phase 1: Aufbau der Hardware
Zusammenbau aller Arduinos und Sensoren.

USB-Verbindung aller Geräte mit dem Raspberry Pi.

Funktionstest aller Sensoren einzeln.

Phase 2: Datenkommunikation
Python-Skripte zum Auslesen der seriellen Schnittstellen.

Standardisiertes JSON-Datenformat definieren.

Fehlerbehandlung für nicht antwortende Geräte.

Phase 3: Datenpersistenz
Anlegen einer SQLite-Datenbankstruktur.

Anlegen einer PostgreSQL/MySQL-Datenbankstruktur.

Entwicklung von Python-Logik zur parallelen Speicherung.

Phase 4: Webserver und Visualisierung
Aufsetzen eines lokalen Webservers auf dem Raspberry Pi.

Entwicklung eines HTML/JavaScript-Frontends zur Live-Visualisierung.

Integration von Charts zur grafischen Darstellung.

Phase 5: Raumschiff-Simulation
Definition von Events (z.B. Sauerstoffmangel, Strahlungsalarm).

Aufbau der Spielmechanik basierend auf Sensordaten.

Implementierung einer Benutzeroberfläche für das Spiel.

Zeitplan (realistisch)

Phase	Dauer	Start
Hardware-Aufbau	1 Woche	Mai 2025
Datenkommunikation	1 Woche	Mai 2025
Datenpersistenz	1 Woche	Mai 2025
Webserver & Visualisierung	2 Wochen	Mai 2025
Simulation & Spiellogik	2–4 Wochen	Juni 2025
Gesamtdauer: ca. 6–8 Wochen (parallel möglich!)

---

## Lizenz

Dieses Projekt steht unter der **MIT-Lizenz** (Open Source).

---

## Mitwirkende

- **Projektleiter & Entwickler:** Watchkido

---

# 🛠️ Hinweis:
Das Ganze wird vermutlich länger dauern als gedacht, kostet ein paar Nerven, ein bisschen Schlaf – aber hey, am Ende kannst du sagen, du hast ein eigenes "Mini-ISS" im Wohnzimmer stehen. 😎🚀


Mitwirkende
Projektleiter & Entwickler: Watchkido

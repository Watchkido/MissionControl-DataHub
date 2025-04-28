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

# 🚀 Projekt-Roadmap: MissionControl-DataHub

## 1. Aufbau der Hardware
- Zusammenbau der Sensor-Module und Mikrocontroller (Arduino, ESP32-CAM)
- Verbindung aller Arduinos und Sensoren mit dem Raspberry Pi via USB/seriell

## 2. Datenkommunikation
- Definition des JSON-Datenformats für alle Sensordaten
- Python-Skript auf dem Raspberry Pi zur Erfassung und Aufbereitung der eingehenden Sensordaten

## 3. Speicherung der Daten
- Aufbau einer lokalen SQLite-Datenbank
- Aufbau einer PostgreSQL- oder MySQL-Datenbank
- Paralleles Schreiben der Sensorwerte in beide Systeme

## 4. Webserver und Frontend
- Einrichtung eines lokalen Webservers (Apache2 oder Nginx) auf dem Raspberry Pi
- Entwicklung eines Web-Frontends zur Anzeige der aktuellen Sensorwerte in Echtzeit (HTML/JavaScript)
- Implementierung von Diagrammen und Statistiken

## 5. Simulation der Raumschiff-Umgebung
- Definition von "Raumschiff-Events" (z.B. Sauerstoffmangel, Strahlungsalarm)
- Implementierung eines einfachen Spiels auf Basis der Live-Daten
- Anzeigen von Alarmen und Missionsstatus im Web-Interface

## 6. Erweiterungen (Future Work)
- Integration von Node-RED oder MQTT für IoT-Erweiterungen
- Mobile App zur Steuerung und Überwachung
- Automatische Kalibrierung und Fehlererkennung der Sensoren

---

# 📅 Zeitplan
- Mai 2025: Hardwareaufbau und Datenkommunikation
- Mai 2025: Datenbank-Integration
- Juni 2025: Webserver-Entwicklung und Visualisierung
- Juni/Juli 2025: Simulation und Spiel-Logik
- Juli 2025: Veröffentlichung als Stable Release (v1.0)

---

# 🛠️ ToDo-Liste
- [ ] Hardware vollständig verkabeln
- [ ] Python-Serielles Interface testen
- [ ] SQLite-Datenbankmodell erstellen
- [ ] PostgreSQL-/MySQL-Datenbank aufsetzen
- [ ] Web-Frontend Grundstruktur bauen
- [ ] Erste Sensorwerte live anzeigen
- [ ] Spiellogik entwickeln
- [ ] Erste Beta-Version veröffentlichen

---

# 🌟 Projektziel
Ein modulares, robustes und cooles System schaffen, das sowohl reale Sensordaten verarbeitet als auch eine spannende Simulationswelt erschafft!


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

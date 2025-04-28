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


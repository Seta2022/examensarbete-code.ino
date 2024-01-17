# examensarbete-code.ino
## Automatiserad Bevattning av Växter i en Lykta

### Projektöversikt
Detta projekt syftar till att skapa ett automatiserat bevattningssystem för växter inuti en lykta, använder IoT-teknologi för att optimera vattenanvändning och underlätta växtvård.

<img src="./images/bild.png" alt="Min bild">


### Hårdvara
- M5Core2
- ULTRASONIC I2C
- PaHUB2
- M5GO Bottom2
- ENV III
- Watering Unit
- NCIR
- DLight Unit
- RGB LED Strip

### Mjukvarukrav
- MQTT
- NodeRed
- InfluxDB
- Grafana
- Zerotier

### Installation
#### Montering av Hårdvara:
1. Börja med att montera M5Core2 och fäst den till M5GO Bottom2.
2. Anslut ULTRASONIC I2C, ENV III, Watering Unit och NCIR till M5Core2 via PaHUB2.
3. Installera RGB LED Strip och DLight Unit inuti lyktan och koppla dem till M5Core2.

#### Installation av Mjukvara:
1. Ladda ner och installera senaste versionen av NodeRed, InfluxDB, Grafana och Zerotier på en central dator eller server.
2. Installera MQTT-broker (t.ex. Mosquitto) för att hantera meddelandeförmedling mellan enheterna.

### Konfiguration
#### Konfigurera M5Core2:
- Programmera M5Core2 för att samla in data från sensorerna och styra bevattningen. Använd Arduino IDE eller liknande för att skriva och överföra koden.

#### Sätta upp NodeRed:
- Konfigurera NodeRed-flöden för att bearbeta och visa data från M5Core2.
- Skapa dashboards i NodeRed för övervakning och styrning av systemet.

#### InfluxDB och Grafana:
- Konfigurera InfluxDB för att lagra sensordata från M5Core2.
- Använd Grafana för att skapa visuella representationer av insamlade data.

#### Nätverkskonfiguration:
- Ställ in Zerotier för fjärråtkomst till systemet.
- Konfigurera MQTT-broker för att säkerställa korrekt kommunikation mellan enheterna och NodeRed.

### IoT-Komponenter och Integration
#### Sensorkonfiguration:
- Ställ in varje sensor (ULTRASONIC I2C, ENV III, etc.) för att skicka data till M5Core2. Använd rätt I2C-adresser och protokoll.

#### M5Core2:
- Programmera M5Core2 för att samla och skicka data via MQTT. Säkerställ att varje enhet är korrekt identifierad och att data skickas i rätt format.

#### Nätverksintegration:
- Konfigurera M5Core2 och NodeRed för att ansluta till samma nätverk. Säkerställ att MQTT-meddelanden flödar korrekt mellan enheterna och NodeRed.

### Användning
#### Övervakning och Justering via NodeRed Dashboard
- **Övervaka Data**: Använd NodeRed-dashboarden för att se realtidsdata från sensorerna.
- **Systemkontroller**: Implementera widgetar för att kontrollera bevattning, belysning och andra funktioner i systemet.
- **Anpassning**: Justera tröskelvärden och scheman för bevattning och belysning baserat på växtens behov och omgivningsförhållanden.

### Kontakt
Seare.taklab@yh.nackademin.se, rene.Ahmuda@yh.nackademin.se.

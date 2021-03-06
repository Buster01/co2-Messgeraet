# CO2-Messgerät
CO2 Messgerät mit CCS811 und ESP32

![CO2 Messgerät von oben](https://github.com/Buster01/co2-Messgeraet/blob/master/Bilder/CO2%20Messger%C3%A4t%20oben.jpg)

### Materialliste

* ESP32
* [Waveshare 2.9" Display (rot/schwarz/weiß)](https://www.waveshare.com/wiki/2.9inch_e-Paper_Module_(B))
* Sensormodul mit CCS811 (CO2-Sensor)
* Dallas DS18B20 (Temperatursensor)
* 1x 4,7 kOhm Widerstand
* 1x 1000 uF Elektrolytkondensator
* DC-DC Step Down Modul (Ausgangspannung 5V)
* Batterie-Halter mit An-/Aus-Schalter für 9V Blockbatterie
* Schrauben, Kabel, Schrumpfschlauch

### Verkabelung:

ESP32 Modul | Waveshare 2.9" Display | CCS811 | DS18B20
------------|------------------------|--------|---------
3.3V | Vcc (grau)|
GND  | GND (braun) | GND + WAKE | GND
GPIO 23  | DIN (blau)|
GPIO 18  | CLK (gelb)|
GPIO 5   | CS  (orange)|
GPIO 16  | DC  (grün)|
GPIO 17  | RST (weiß)|
GPIO 4   | BUSY (violet)|
5V | | Vcc | Vcc
GPIO 22 | | SCL |
GPIO 21 | | SDA | 
GPIO 15 | | | DATA ( 4,7kOhm Widerstand zwischen Data und Vcc)

### Stromverbrauch

Status | Stromverbrauch
-------|---------------
Light Sleep | ca. 22 mA
CO2 / Temperatur messen (CPU aktiv) | ca. 43 mA
Display aktualisieren (CPU aktiv) | ca. 60mA

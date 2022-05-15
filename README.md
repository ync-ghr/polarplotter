# Polar Plotter
Ein Projekt der Hochschule Pforzheim.

- Bauteile und deren Funktion/Herstellung
- Handhabung des Plotters


## Benötigte Komponenten

### Zukaufteile

- Arduino Uno: http://store.arduino.cc/products/arduino-uno-rev3

- Adafruit Motor Shiled v2: https://www.adafruit.com/product/1438

- Servomotor: https://www.amazon.de/dp/B07CYZK379?ref_=cm_sw_r_cp_ud_dp_AW2FQ5ZJ4909N2ZZ1QXP

- Schrittmotoren: https://www.adafruit.com/product/324#technical-details
  - 200 steps per revolution
  - 1.8 degrees
  - 12 V
  - 350 mA

- Zahnriemen und Zahnräder: https://www.amazon.de/dp/B07QH94G71?ref_=cm_sw_r_cp_ud_dp_NBP2886NY2H1YNJAXYJZ

- Gewichte: https://www.amazon.de/dp/B08F2H4TB8?ref_=cm_sw_r_cp_ud_dp_EE6H5DKYBR2R5X1NX4WT 
  - 100 g + 2 x 60 g

- 12 V Netzteil

- Schrauben und Muttern:
  - 

### 3D-Druck Teile

#### Funktion

- Gehäuse mit Deckel

      sss

- Gondel und Gewichthalterung

- Halterung für Gegengewichte

- Motorhalterung

- Klemme

- Schraubeinsatz

- Schraube

#### Herstellung

Dateien aus /stl auf dem 3D Drucker herstellen. Anordnung der einzelnen Komponenten wie im Bild um bestmögliche Ergebnisse zu erhalten.

![image](https://user-images.githubusercontent.com/58829180/168470991-aa8e7993-4bd5-4211-93ab-83f221624614.png)

## Polargraph Software

### Installation

- Herunterladen und installieren von Arduino IDE v1.8.5: https://www.arduino.cc/en/software/OldSoftwareReleases#previous

- Herunterladen des Polargraphcontollers: https://github.com/euphy/polargraphcontroller/releases/tag/2017-11-01-20-30

- Dieses Verzeichnis (polargraph.2017-11-01.zip)entpacken und öffnen. Darin ist ein Ordner \arduino-source\polargraph-server-a1 enhalten. Diesen in den Arduino Ordner verschieben (`C:\Users\"PCNAME"\Documents\Arduino`). [1]

- Den Inhalt des Ordners \arduino-source\libraries in den Ordner C:\Users\"PCNAME"\Documents\Arduino\libraries verschieben. [2]

- Anschließend Arduino IDE starten.

- File -> Sketchbook -> polargraph_server_a1 auswählen und im Tab polargraph_server_a1 unter 1. den Controller auf MC_UNO einstellen. Unter 3. die verwendeten Motortreiber auswählen. [3] 

      // 1. 
      //Uncomment the line for the kind of board you have.
      #ifndef MICROCONTROLLER
      #define MICROCONTROLLER MC_UNO
      //#define MICROCONTROLLER MC_MEGA
      #endif

      // 3. 
      //Specify what kind of motor driver you are using
      #define ADAFRUIT_MOTORSHIELD_V2
      #include <Wire.h>
      #include <Adafruit_MotorShield.h>
      #include "utility/Adafruit_PWMServoDriver.h"

- Auf den Pfeil klicken, um den Code auf den Arduino zu laden. Warten bis Hochladen abgeschlossen ist.

- Herunterladen und installieren von Processing v2.2.1: https://processing.org/download?processing

- Processing starten und wieder schließen.

- Im schon heruntergeladenen Verzeichnis (polargraph.2017-11-01) den Inhalt des Ordners `Polargraph.2017-11-01\processing-source\Processing libraries` nach `C:\Users\"PCNAME"\Documents\Processing\libraries` kopieren.

- Anschließend den gesamten Ordner `Polargraph 2017-11-01\processing-source\polargraphcontroller` in den Processing Sketchbook Ordner (`C:\Users\"PCNAME"\Documents\Processing`) kopieren.

- Processing erneut starten und File -> Sketchbook -> polargraphcontroller öffnen. [5]

- Run drücken um den Controller zu starten.




### Einstellungen in der Software

### Verwendung



 



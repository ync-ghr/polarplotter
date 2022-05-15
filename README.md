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

Dateien aus /stl auf dem 3D Drucker herstellen.

![image](https://user-images.githubusercontent.com/58829180/168470991-aa8e7993-4bd5-4211-93ab-83f221624614.png)

## Polargraph Software

### Installation

- Herunterladen und installieren von Arduino IDE v1.8.5: https://www.arduino.cc/en/software/OldSoftwareReleases#previous

- Herunterladen des Polargraphcontollers: https://github.com/euphy/polargraphcontroller/releases/tag/2017-11-01-20-30

- Dieses Verzeichnis (polargraph.2017-11-01.zip)entpacken und öffnen. Darin ist ein Ordner \arduino-source\polargraph-server-a1 enhalten. Diesen in den Arduino Ordner verschieben (`C:\Users\"PCNAME"\Documents\Arduino`). ![image](https://user-images.githubusercontent.com/58829180/168472281-1d77a318-3a13-466e-a567-8d2137aa97d8.png)

- Den Inhalt des Ordners \arduino-source\libraries in den Ordner C:\Users\"PCNAME"\Documents\Arduino\libraries verschieben. ![image](https://user-images.githubusercontent.com/58829180/168472653-08670873-b451-4253-8424-7977ee3ee37a.png)

- Anschließend Arduino IDE starten.

- File -> Sketchbook -> polargraph_server_a1 auswählen und im Tab polargraph_server_a1 unter 1. den Controller auf MC_UNO einstellen. Unter 3. die verwendeten Motortreiber auswählen. ![image](https://user-images.githubusercontent.com/58829180/168472719-464ff1c7-55a8-4c44-84b5-1600686a130c.png) 

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

- Im schon heruntergeladenen Verzeichnis (polargraph.2017-11-01) den Inhalt des Ordners `Polargraph.2017-11-01\processing-source\Processing libraries` nach `C:\Users\"PCNAME"\Documents\Processing\libraries` kopieren. ![image](https://user-images.githubusercontent.com/58829180/168473290-ab935f19-e45b-4012-8ca4-7e088a439ae2.png)

- Anschließend den gesamten Ordner `Polargraph 2017-11-01\processing-source\polargraphcontroller` in den Processing Sketchbook Ordner (`C:\Users\"PCNAME"\Documents\Processing`) kopieren.

- Processing erneut starten und File -> Sketchbook -> polargraphcontroller öffnen. ![image](https://user-images.githubusercontent.com/58829180/168473686-794536f1-a014-4cf2-ae10-0fb310a638d6.png)

- Run drücken um den Controller zu starten.

### Aufsetzen der Software

### Einstellungen in der Software

### Verwendung

 



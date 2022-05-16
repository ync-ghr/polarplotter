# Polar Plotter
Ein Projekt der Hochschule Pforzheim.

- Bauteile und deren Funktion/Herstellung
- Handhabung des Plotters


## Benötigte Komponenten

![image](https://user-images.githubusercontent.com/58829180/168477973-95d0accc-3933-4d4f-9964-99fa80b72a3a.jpg)

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



## Installation Polargraph Software

- Herunterladen und installieren von Arduino IDE v1.8.5: https://www.arduino.cc/en/software/OldSoftwareReleases#previous

- Herunterladen des Polargraphcontollers: https://github.com/euphy/polargraphcontroller/releases/tag/2017-11-01-20-30

- Dieses Verzeichnis (polargraph.2017-11-01.zip)entpacken und öffnen. Darin ist ein Ordner `\arduino-source\polargraph-server-a1` enhalten. Diesen in den Arduino Ordner verschieben (`C:\Users\"PCNAME"\Documents\Arduino`). ![image](https://user-images.githubusercontent.com/58829180/168472281-1d77a318-3a13-466e-a567-8d2137aa97d8.png)

- Den Inhalt des Ordners `\arduino-source\libraries` in den Ordner `C:\Users\"PCNAME"\Documents\Arduino\libraries` verschieben. <img src="https://user-images.githubusercontent.com/58829180/168472653-08670873-b451-4253-8424-7977ee3ee37a.png" height="200"/>

- Anschließend Arduino IDE starten.

- `File -> Sketchbook -> polargraph_server_a1` auswählen und im Tab polargraph_server_a1 unter 1. den Controller auf MC_UNO einstellen. Unter 3. die verwendeten Motortreiber auswählen. ![image](https://user-images.githubusercontent.com/58829180/168472719-464ff1c7-55a8-4c44-84b5-1600686a130c.png) 

  ```
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
  ```

- Auswahl des Boards: `Tools -> Board -> Arduino Uno`

- Setzen des angeschlossenen Ports: `Tools -> Port -> COMx`

- Auf den Pfeil klicken, um den Code auf den Arduino zu laden. Warten bis Hochladen abgeschlossen ist.

- Herunterladen und installieren von Processing v2.2.1: https://processing.org/download?processing

- Processing starten und wieder schließen.

- Im schon heruntergeladenen Verzeichnis (polargraph.2017-11-01) den Inhalt des Ordners `Polargraph.2017-11-01\processing-source\Processing libraries` nach `C:\Users\"PCNAME"\Documents\Processing\libraries` kopieren. ![image](https://user-images.githubusercontent.com/58829180/168473290-ab935f19-e45b-4012-8ca4-7e088a439ae2.png)

- Anschließend den gesamten Ordner `Polargraph 2017-11-01\processing-source\polargraphcontroller` in den Processing Sketchbook Ordner (`C:\Users\"PCNAME"\Documents\Processing`) kopieren.

- Processing erneut starten und `File -> Sketchbook -> polargraphcontroller` öffnen. ![image](https://user-images.githubusercontent.com/58829180/168473686-794536f1-a014-4cf2-ae10-0fb310a638d6.png)

- Run drücken um den Controller zu starten.

## Aufbau des Plotters

- Zusammenbau der beiden Motorhalterungen aus den 3D-Druckteilen, jeweils 3 Schrauben(2st M3x15, 1st M3x18) und 3 Muttern.
![image](https://user-images.githubusercontent.com/58829180/168479281-f0360503-3d68-4132-b768-b2df2f2ae6e7.png)
 
- Festschrauben der Motoren an der Halterung und Befestigung am Zeichenbrett und Anbringung der Zahnräder.
![20220516_110719](https://user-images.githubusercontent.com/58829180/168559960-e3f53283-147d-4a8c-b2c6-c62ea221a4bd.jpg)

- Anbringung des Motorshields auf dem Arduino und Vorbereiten der 12 V Stromversorgung.
![20220516_111948](https://user-images.githubusercontent.com/58829180/168561048-7b88ac8f-c3d1-4d6f-aeaf-cb69f87a328b.jpg)

- Einlegen der Gewichte in die Gewichthalterungen und Befestigung des Gummiriemens durch verkanten der Zähne. Riemen soll einmal gespielgelt angebracht werden (siehe Bild).
![image](https://user-images.githubusercontent.com/58829180/168568506-5a603d1d-076f-4bfc-96d7-2ebf2eedf45e.png)

- Anbringen des Servomotors und der Gewichthalterung an der Gondel. Befestigung des Gummiriemens durch verkanten. Verlängerungskabel für den Servomotor verbinden. Einschmelzen des Gewindes in die Bohrung.
![20220516_121023](https://user-images.githubusercontent.com/58829180/168570563-8d301d7e-7dcd-4682-bf0e-0740712784b9.jpg) ![20220516_131647](https://user-images.githubusercontent.com/58829180/168581409-2ad9771a-cbc7-4bed-8488-3364a2c2bc27.jpg)



- Aufsetzen der Konstruktion über die Zahnräder und Kabel auf der Rückseite führen.
![20220516_122937](https://user-images.githubusercontent.com/58829180/168573883-09961e05-999e-4f74-878e-248b0c09f473.jpg)


- Verkabelung der beiden Schrittmotoren an die Klemmen (Blau/Grün ein Coil, Gelb/Rot ein Coil) und aufstecken des Servosteckers an die Servo 2 Pins. Herstellen der 12 V Stromversorgung und der USB-Verbindung mit einem Windows-PC.
![image](https://user-images.githubusercontent.com/58829180/168578243-2e42a344-23a8-4350-8ab4-d5836b6ee91a.png)



## Einstellungen in der Software

### SETUP

Einstellungen für die Abmessungen des Zeichenbretts und des Zeichenblatts sowie weitere grundsätzliche Einstellungen.

| Feldname | Wert | Bedeutung |
|---|----:|----------------|
| MM PER REV        | 64 | Drehung des Riemens pro Schritt |
| STEPS PER REV     | 400 | Schritte pro Umdrehung |
| STEP MULTIPLIER   | 16 | Skalierung der Schritte |
| MASCHINE WIDTH    | - | Breite des Zeichenbretts (Distanz zwischen beiden Motoren)               |
| MASCHINE HIGHT    | - | Höhe des Zeichenbretts |
| PAGE WIDTH        | - | Breite des Zeichenblatts |
| PAGE HIGHT        | - | Höhe des Zeichenblatts |
| PAGE POS X        | - | X-Position des Blatts |
| PAGE POS Y        | - | Y-Position des Blatts |
| HOME POS X        | - | X-Position des Homepunkts |
| HOME POS Y        | - | Y-Postition des Homepunkts |
| PEN UP POSTION    | - | Winkel des Servos für angehobeben Stift |
| PEN DOWN POSITION | - | Winkel des Servos für abgesetzten Stift |
| MOTOR MAX SPEED | 600 | Maximalgeschwindigkeit des Motors |
| MOTOR MAX ACCELERATION | 400 | Maximalbeschleunigung des Motors |

- Außerdem muss der SERIAL PORT... eingesetellt werden.

![image](https://user-images.githubusercontent.com/58829180/168475457-5be9ecf9-80a4-4091-a58f-1444e811f564.png)


### INPUT

Einstellungen die das Zeichenobjekt betreffen.

![image](https://user-images.githubusercontent.com/58829180/168476232-b45c74d7-8c10-472a-9b71-563c5e8b700b.png)







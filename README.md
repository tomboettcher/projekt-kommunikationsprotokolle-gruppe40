# projekt-kommunikationsprotokolle-gruppe40
Benötigte Bauteile:
Zum Aufbau der Schaltung werden 3 STM 32 benötigt (1 mal Master, 2 mal Slave), 6 Taster (4 zum Schalten der Lampen und 2 für den Send request) , 4 Lampen (Rot, Grün, Blau und Gelb), 6 Pullup Wiederstände (10 KΩ), 4 Vorwiederstände für die Lampen (320Ω), 

Aufbau:
Zum Aufbau der Schaltung müssen die I2C Schnittstelle (SDA und SCL) des Masters mit den I2C Schnittstellen der beiden Slaves  verbunden werden. Diese beiden Verbindungen müssen noch über einen 10 kΩ mit 5V verbunden werden. Die Schalter werden an den Master angeschlossen wobei die Anschlüsse dem Schaltplan zu entnehmen sind. Die Lampen werden mit den Vorwiederständen an den Slaves angeschlossen wobei die Anschlüsse wieder dem Schaltplan zu entnehmen sind. 

I2C Protokoll:
Bei dem Byte 0000 0000 sind beide Lampen die über den Slave 1 oder 2 angesteuert werden aus.
Bei dem Byte 0000 0001 ist beim Slave 1 die Lampe Rot an und beim Slave 2 die Gelbe Lampe an. 
Bei dem Byte 0000 0010 ist beim Slave 1 die Lampe Grün an und beim Slave 2 die Blaue Lampe an.   
Bei dem Byte 0000 0011 sind beide Lampen die über den Slave 1 oder 2 angesteuert werden an.

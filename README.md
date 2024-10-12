# Station météo

Ce montage permet de mesurer la vitesse du vent :
* 1 Kit de développement miniature M5 Atom RS485 basé sur un microcontrôleur miniature Atom Lite avec interfaces WiFi et Bluetooth. Ce module est associé à une extension prévue pour convertir un signal RS485 12 Vcc vers un signal TTL 5 Vcc.
* Le module ATOM et le capteur sont alimentés en 12V

![wind](https://github.com/user-attachments/assets/c80dc17a-f738-4c5b-837e-087735042ec4)

## Matériel

* [Capteur anémomètre extérieur RS485](https://www.aliexpress.com/item/1005005698076731.html)
  * Documentation technique: [RS-FSJT-N01Wind speedtransmitteruser's Guide](https://instrucenter.com/wp-content/uploads/2022/03/RS-FSJT-No1.pdf)
* [Kit de développement miniature M5 Atom RS485](https://www.gotronic.fr/art-kit-atom-rs485-k045-32911.htm)


## Câblage du capteur

Le câble qui sort de la partie inférieure de l'anémomètre a le brochage suivant :
* Marron : +12V
* Noir : Masse
* Vert : RS485-A
* Bleu : RS485-B

## Programmation

### ESPHome

Programmer l'ESP32 pour lire le registre ModBus de l'anémomètre: 
* Tutoriel configuration ESPHome: [Renke RS-FSJT-N01 Wind speed anemometer](https://devices.esphome.io/devices/Renke-RS-FSJT-N01-Wind-Speed)

**Page ESPHome**


![image](https://github.com/user-attachments/assets/d945c143-ac2f-4a8c-ac80-683947c04954)

**Journal ESPHome**

* La valeur indiquée par le capteur est en m/s * 10
* Il est possible de convertir en km/h avec un facteur 3,6

![image](https://github.com/user-attachments/assets/d50ee223-b9f6-4989-95f6-8c5c9a81cdbf)

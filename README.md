# Station météo

Ce montage permet de mesurer la vitesse du vent :
* 1 Kit de développement miniature M5 Atom RS485 basé sur un microcontrôleur miniature Atom Lite avec interfaces WiFi et Bluetooth. Ce module est associé à une extension prévue pour convertir un signal RS485 12 Vcc vers un signal TTL 5 Vcc.
* Le module ATOM et le capteur sont alimentés en 12V

![wind](https://github.com/user-attachments/assets/c80dc17a-f738-4c5b-837e-087735042ec4)

## Matériel

* [Capteur anémomètre extérieur RS485](https://www.aliexpress.com/item/1005005698076731.html)
* [Kit de développement miniature M5 Atom RS485](https://www.gotronic.fr/art-kit-atom-rs485-k045-32911.htm)

## Programmation

### ESPHome

Programmer l'ESP32 pour lire le registre ModBus de l'anémomètre: 
* Tutoriel configuration ESPHome: [Renke RS-FSJT-N01 Wind speed anemometer](https://devices.esphome.io/devices/Renke-RS-FSJT-N01-Wind-Speed)

## Cablage du capteur

Le câble qui sort de la partie inférieure de l'anémomètre a le brochage suivant :
* Marron : +12V
* Noir : Masse
* Vert : RS485-A
* Bleu : RS485-B

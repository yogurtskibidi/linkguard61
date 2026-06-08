# linkguard61
LinkGuard : Système de sécurité pour tous. Ce dispositif de communication sans fil détecte le retrait d'un objet et déclenche une alerte immédiate sonore et par mail. Une solution efficace utilisant la transmission de données à distance pour protéger vos objet contre le vol en temps réel.

Pour ce projet de CSF (Communication Sans Fil), nous avons eu comme projet de faire un antivol qui se déclanche lorsque l'objet présent est retiré.
L'idée étant de poser l'objet sur le support, qui ce dernier comporte un capteur ultrason, et que si cet objet n'est plus détecté (seuil défini dans le code dans Arduino IDE), cela ferait retentir un buzzer qui permettra justement de signaler le vol en direct et envoyer un email à l'utilisateur. Bien entendu, si l'objet est remis en place, alors le buzzer en question cessera de sonner.
Pour répondre aux exigences du cours "Communication sans fil", nous avons intégré la technologie LoRaWAN à notre projet. Ce protocole sans fil a été directement implémenté dans notre code via l'IDE Arduino.
Ainsi, la carte transmet le booléen gérant la présence de l'objetvia le protocole LoRaWAN au réseau TTN, qui est lui même relié à la platforme Tago.io qui à pour tâche de prendre la variable donnée et d'en faire une action, ainsi lorsqu'il recoit l'absence de l'objet, cela enverra un mail à l'utilisateur.




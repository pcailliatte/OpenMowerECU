# Câblage — Prise d’alimentation et prise de commande

Rétro-ingénierie du câblage d’alimentation de l’ECU MowerBoard sur le Staub 107 L 16 KH.

## Prise d’alimentation

<p align="center">
  <img src="./assets/img/power_plug_wiring.jpg" alt="Prise d’alimentation" width="50%">
</p>

| Broche | Fonction | Couleur du fil | Tension | Notes |
|---|---|---|---|---|
| 1 | Embrayage plateau de coupe | Bleu | GND pour activer | Bobine 2 relais K1 |
| 2 | Masse | Noir | GND | |
| 3 | Arrêt moteur (kill switch) | Bleu | GND = moteur OFF | Bobine 1 relais K1 — NC sur GND (sécurité) |
| 4 | Sortie carte (fusible 20A) | Rouge | +12V | |
| 5 | Entrée batterie | Rouge | +12V | |
| 6 | Sortie carte (fusible 10A) | Rouge | +12V | |

<p align="center">
  <img src="./assets/img/power_socket.png" alt="Prise d’alimentation (vue connecteur)" width="200px">
</p>

## Connecteur Molex 2x7 broches (14 broches)

<p align="center">
  <img src="./assets/img/command_plug_wiring_1-7.jpg" alt="Prise de commande (broches 1 à 7)" width="400px">
  <img src="./assets/img/command_plug_wiring_8-14.jpg" alt="Prise de commande (broches 8 à 14)" width="350px">
</p>

Numérotation :
- Rangée A : broches 1 à 7
- Rangée B : broches 8 à 14

| Broche | Signal / Fonction | Direction | Couleur | Tension | Notes |
|---:|---|---|---|---|---|
| 1 | Non connecté | NC | | | |
| 2 | Non connecté | NC | | | |
| 3 | Ordre de coupe / PTO | Entrée | Orange | Commutation de masse | |
| 4 | Bouton A/R sur tableau de bord | Entrée | Blanc | Commutation de masse | Historiquement, déverrouillage de la coupe en marche arrière |
| 5 | Masse de la solénoïde du démarreur | Sortie | Vert | GND = démarrage | Via relais K1, bobine 1 |
| 6 | AUX / Feux | Sortie | Jaune | +12V ou GND selon le relais | Peu utilisé, via relais K2, bobine 2 |
| 7 | Tension de contact (Neiman) | Entrée / Alimentation | Rouge | +12V | Historiquement alimentation de la carte |
| 8 | Demande de démarrage | Entrée | Jaune | +12V | Le +12V vient du contact Neiman |
| 9 | Frein | Entrée | Vert | Commutation de masse | Le frein peut être verrouillé fermé |
| 10 | Contact siège | Entrée | Orange | Commutation de masse | |
| 11 | Non connecté | NC | | | |
| 12 | Masse / GND | Alimentation | Noir | | |
| 13 | Marche arrière | Entrée | Bleu | Commutation de masse | |
| 14 | Marche avant | Entrée | Vert | Commutation de masse | |

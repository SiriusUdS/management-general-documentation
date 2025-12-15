
| Ordre des bits | 0-3       | 4-7            | 8-21  | 22      | 23-28    |
| -------------- | --------- | -------------- | ----- | ------- | -------- |
| Sujets         | Source ID | Destination ID | Sujet | Drapeau | Priorité |

| Nombre de posibilité | 16        | 15             | 16 384 | 2       | 64       |
| -------------------- | --------- | -------------- | ------ | ------- | -------- |
| Sujets               | Source ID | Destination ID | Sujet  | Drapeau | Priorité |

### Logique du ID :

Source ID : 0x0 : node 0 | 0x1 : node 1 ... etc.
Destination ID : 0x0 : node 0 | 0x1 : node 1 ... 0xF : BROADCAST

Si deux messages ont la même priorité, le module CAN va choisir la valeur numérique la plus basse en premier donc (ex : arrêt d'urgence : 0x0010 : Bon choix (très bas), 0xEEEE : Mauvais choix (très haut)) Le choix de l'ordre des sujets doit donc être choisi judicieusement.

### ⚠️ Si deux messages ont la même priorité, le module CAN va choisir la valeur numérique la plus basse en premier donc (ex : arrêt d'urgence : 0x0010 : Bon choix (très bas), 0xEEEE : Mauvais choix (très haut)) Le choix de l'ordre des sujets doit donc être choisi judicieusement. ⚠️

### Sujets de messages :

| 0x0000 - 0x00FF | Système & Sécurité |
| --------------- | ------------------ |
| 0x0100 - 0x0FFF | Contrôle Rapide    |
| 0x1000 - 0x1FFF | Capteurs Lents     |
| 0x3000...       | Logs & Debugs      |
### Flag Remote Request

Flag Remote Request (R/R) : 0 : I am sending information | 1 : I want this information

### Priorité : 
| Priorité | Priorité (HEX) | Nom                | Description                                                                                                                                           |
| -------- | -------------- | ------------------ | ----------------------------------------------------------------------------------------------------------------------------------------------------- |
| 0-3      | 0x00 - 0x03    | Critique           | Aucune latence. Priorité sur tout les messages. Uniquement pour les arrêts d'urgence, les battement (NMT) et pour signaler une erreur fatal du réseau |
| 4-15     | 0x04 - 0x0F    | Contrôle temp réel | Basse latence < 1ms. Pour le contrôle en temp réel critique.                                                                                          |
| 16-47    | 0x10 - 0x2F    | Status normal      | Latence normal > 10 ms. La plupart du trafic, pour les capteur/bouton non critique                                                                    |
| 48-63    | 0x30 - 0x3F    | Background         | Peut attendre indéfiniment (Logs & debug)                                                                                                             |
### Cas spéciaux :
Priorité 0x00 (Critique) + Sujet 0x0000 (+ important): 
⚠️Option nucléaire (shutdown total du système)⚠️
Priorité 0xFF (Background) + Sujet 0xFFFF (- important):
🗑️Message poubelle (Logs et autres )🗑️
# Fiche projet — Équipe 17

> Livrable L2 · Jalon J1 (samedi 29 août 2026) · validée par l'encadreur référent.
> Aucune fabrication n'est autorisée avant la validation de ce jalon.

## 1. Titre et accroche

**AlertGSM-ESP32 : Prototype d'alarme d'intrusion et d'incendie à alerte SMS distante**  
Un prototype pédagogique développé pour l'atelier du FabLab qui transforme une alerte locale en une notification SMS distante envoyée directement au responsable du FabLab.

## 2. Besoin et bénéficiaires

- **Difficulté d'apprentissage visée :** Prise en main du microcontrôleur ESP32-S3, apprentissage de la chaîne d'information (capteurs, traitement, communication GSM/SMS), et gestion logicielle de l'armement/désarmement.
- **Élèves concernés :** Participants aux ateliers du FabLab / Élèves de formation technique (25 groupes de 4 élèves).
- **Établissement d'accueil :** L'atelier du FabLab d'accueil (inoccupé la nuit et le week-end).

## 3. Objectifs d'apprentissage

Trois objectifs observables rattachés au programme officiel :

1. **Maîtrise de l'ESP32-S3 :** Programmer un microcontrôleur moderne pour lire des données de capteurs multiples et piloter des actionneurs/modules GSM.
2. **Programmation de la logique d'armement :** Concevoir une interface d'armement et de désarmement du système d'alarme automatique via code 
3. **Fabrication numérique multi-procédés :** Concevoir le circuit (PCB gravé au laser) et l'enveloppe du prototype pour l'atelier du FabLab.

## 4. Description du dispositif

- **Ce que l'objet fait :** Installé dans l'atelier du FabLab, le prototype surveille les accès et la présence de feu/fumée. Une fois armé, toute intrusion ou détection de flamme déclenche la sirène locale et envoie un SMS d'alerte ciblé. Un autotest quotidien vérifie l'état des capteurs.
- **Ce que l'élève fait avec :** L'élève câble les composants sur l'ESP32-S3, programme les séquences d'armement/désarmement et d'alerte, fabrique le boîtier et réalise les tests de déclenchement dans l'atelier.
- **Esquisse :

## 5. Architecture technique pressentie

- **Unité centrale :** Carte à microcontrôleur **ESP32-S3**.
- **Capteurs :** Capteur infrarouge passif (PIR), détecteur de fumée (MQ-135).
- **Système d'armement/désarmement :** Interface d'armement gérée par l'ESP32-S3.
- **Actionneurs :** Sirène d'alarme sonore, module GSM (envoi de SMS), LED indicatrices de statut.
- **Application :** Programme embarqué (C++ / Arduino IDE).
- **Procédés de fabrication envisagés (3 procédés) :**
  1. Gravure de la carte électronique (PCB) au laser fibre MOPA (**xTool F2 Ultra**).
  2. Découpe et gravure laser du boîtier de la centrale d'alarme du FabLab (**xTool**).
  3. Impression 3D des boîtiers et supports de capteurs (**Bambu Lab P2S**).

## 6. Rôle des élèves

- **Positionnement :** Démarche **PAR** les élèves.
- **Extension PAR :** Les élèves étudient l'agencement de l'atelier du FabLab, conçoivent le typon de la carte pour ESP32-S3, réalisent la gravure laser du PCB, assemblent le prototype et programment la logique d'autotest.

## 7. Ancrage réseau et implantation

- **Lab de rattachement :** FabLab d'accueil.
- **Lieu d'usage :** Local / Atelier du FabLab.
- **Conditions matérielles de la salle :** Postes informatiques configurés, réseau GSM fonctionnel, équipements de fabrication (xTool F2 Ultra, Bambu Lab P2S).

## 8. Périmètre

| | Contenu |
|---|---|
| **Dans la v1.0 (Socle)** | Prototype d'atelier basé sur ESP32-S3, 1 capteur PIR, 1 capteur de flamme, contacts magnétiques, sirène locale, module GSM avec SMS, système d'armement/désarmement et autotest quotidien. |
| **En option (Avancé / Expert)** | Interface Web locale hébergée sur l'ESP32-S3 (via Wi-Fi) pour armer/désarmer et consulter les logs. |
| **Explicitement exclu** | Utilisation de badges RFID, raccordement aux services de secours publics. |

## 9. Risques et parades

| Risque | Type | Parade |
|---|---|---|
| Réception GSM faible dans l'atelier | Technique | Déporter l'antenne du module GSM près d'une fenêtre du FabLab. |
| Complexité du brochage de l'ESP32-S3 | Technique | Valider le schéma de câblage sur breadboard avant la gravure finale du PCB. |
| Fausses alertes lors des tests | Pédagogique | Ajouter une temporisation d'entrée/sortie (délais d'armement) dans le code de l'ESP32-S3. |

## 10. Budget matière estimé

- Microcontrôleur ESP32-S3  : 15 000 FCFA
- Capteurs PIR : 2 000 FCFA,
- Capteurs de fumée MQ-135 : 2 000 FCFA, 
- Le MODULE SIM7600E : 20 000 FCFA,
- Un buzzer 5V : 2000 FCFA,
- Matériaux de fabrication (Plaques contreplaqué, filament PLA/PETG)
- Boutons et connectique : 8 000 FCFA
- led rouge et vert : 500 FCFA,
- afficheur  MODULE TM1637 (4 digits, 7 sègments) : 2500 FCFA,
- **Total estimé :** **35 000 FCFA**

## 11. Licences et diffusion

- **Licence choisie : 
- **Motivation :** Permettre la réutilisation et l'amélioration du prototype par d'autres FabLabs du réseau.
- **Accord :** L'équipe 17 valide la diffusion de ce prototype sur le réseau.

## Exemptions demandées

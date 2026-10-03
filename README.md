# Mbia DataFlow — prototype natif Android

Prototype de compteur global de données mobiles pour Android.

## Fonctions incluses
- Compteur global mobile RX + TX via `TrafficStats`.
- Affichage actualisé régulièrement.
- Surveillance séparée de la **Protection par limite**.
- Interrupteur général **Application active**.
- Limite configurable en GB.
- Alertes à 80 %, 90 % et 100 %.
- Historique global conservé et remise à zéro de la période sans effacer l'historique cumulé.
- Service au premier plan pour maintenir la surveillance en arrière-plan.
- Projet Android natif + workflow GitHub Actions.

## Important pour le prototype
Le mode normal alerte à la limite. Il ne prétend pas couper globalement les données mobiles, car une application Android ordinaire n'a pas ce contrôle système universel.

Les compteurs `TrafficStats` reflètent les statistiques réseau fournies par Android et doivent être validés sur le TECNO Spark 9T / Android 12 ciblé par le prototype.

## Compilation
Le projet contient le wrapper Gradle. Depuis Termux ou GitHub Actions :

```bash
./gradlew assembleDebug
```

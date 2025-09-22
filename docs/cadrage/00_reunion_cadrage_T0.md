# Compte-rendu — Réunion de cadrage T0

**Date :** Semaine 1  
**Participants :** Gérant du garage, Étudiant (chef de projet)  
**Lieu :** Garage Léon Olivier, Saint-Ouen

## Besoins exprimés

- Aucun outil de suivi de stock actuellement (suivi papier)
- Commandes via Rpartstore, factures envoyées au client final
- Équipe : 2-3 mécaniciens, peu à l'aise avec l'informatique
- Besoin max estimé : ~200 références actives (plafond 1 000)

## Contraintes identifiées

- Pas de serveur en atelier → solution 100% locale
- Budget : 0 € → open-source uniquement
- Délai : livraison avant fin du workshop (~13 semaines)
- RGPD : factures contiennent des données clients → OCR local obligatoire

## Décisions prises

- Solution HTML mono-fichier, ouverture directe navigateur
- Stockage CSV portable (compatible Excel)
- OCR intégré via Tesseract.js (sans envoi cloud)
- Interface minimaliste : boutons +/−, alertes colorées, sidebar

## Prochaine étape

Rédaction note de cadrage → validation client S2

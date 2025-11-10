# Recettage V1

**Date :** Semaine 8  
**Testeurs :** Gérant + 1 mécanicien  
**Navigateur :** Chrome, PC fixe atelier

| #   | Cas de test                        | Résultat | Note               |
|-----|------------------------------------|----------|--------------------|
| T01 | Ajout pièce via formulaire modal   | ✅ OK    |                    |
| T02 | Bouton + / − quantité              | ✅ OK    | Très intuitif      |
| T03 | Filtre catégorie                   | ✅ OK    |                    |
| T04 | Filtre état + texte simultanés     | ✅ OK    |                    |
| T05 | Alerte rupture + lien Rpartstore   | ✅ OK    | Lien fonctionnel   |
| T06 | Export CSV → ouverture Excel       | ✅ OK    |                    |
| T07 | Persistance après fermeture nav.   | ✅ OK    | localStorage stable|

## Retours client

- ✅ "C'est simple, on comprend tout de suite"
- 🔄 "On aimerait voir le prix pour prioriser les commandes" → V2
- 🔄 "Pouvoir scanner les factures directement" → V2 OCR

## Décision

V1 validée et livrable. Développement V2 (OCR + historique) lancé.

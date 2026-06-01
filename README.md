# Logiciel de gestion de stock — Garage Renault Léon Olivier

**Workshop Client M2 — MBA Big Data — MyDigitalSchool 2025–2026**

## Présentation

Application web autonome (1 fichier HTML) de gestion de stock de pièces détachées
pour le Garage Léon Olivier (Renault agréé, Saint-Ouen 93).

## Fonctionnalités

- Gestion CRUD du stock (jusqu'à 1 000 références)
- Import automatique de factures par OCR (Tesseract.js — 100% local)
- Import/Export CSV compatible Excel
- Historique des mouvements horodatés
- Alertes de seuil et lien direct Rpartstore

## Versions livrées

| Version | Description | Semaine |
|---------|-------------|---------|
| V1 | Interface stock + CRUD + localStorage | S8 ✅ |
| V2 | + OCR factures + Historique | S11 ✅ |
| V3 | + CSV persistant + Import CSV masse | S12 ✅ |

## Utilisation

Ouvrir `src/gestion_stock_renault_v3.html` dans Chrome ou Firefox.
Aucune installation requise.

## Liens

- Portail commandes Renault : https://rpartstore.renault.com/
- Dossier technique : `docs/dossier_technique_workshop_renault.docx`

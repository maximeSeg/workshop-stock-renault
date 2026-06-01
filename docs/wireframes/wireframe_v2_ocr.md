# Wireframes V2 — Module OCR

**Semaine :** 9 — Validés par le client

## Écran — Import facture OCR

```
┌──────────────────────────────────────────────────────────────────┐
│  Import facture Renault (OCR) — 100% local, aucun envoi réseau  │
├──────────────────────────────────────────────────────────────────┤
│                                                                  │
│  ┌ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─┐  │
│  │  📄  Glissez une photo de facture ici                      │  │
│  │      ou cliquez — JPG, PNG, BMP                           │  │
│  │  Entités ciblées : Désignation · Référence · Qté · Prix   │  │
│  └ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─┘  │
│                                                                  │
│  [▶ Analyser la facture]  [Annuler]                             │
│  ████████████████░░░░  80%  Reconnaissance en cours...          │
│                                                                  │
│  ✓ 1 pièce détectée — vérifiez avant import                    │
│  ┌──────────────┬──────────────────────────┬─────┬──────────┐   │
│  │ Référence    │ Désignation              │ Qté │ Catégorie│   │
│  │ [8200100   ] │ [Télécommande Megane IV] │ [1] │ [Autre▼] │   │
│  └──────────────┴──────────────────────────┴─────┴──────────┘   │
│  [✓ Importer dans le stock]   [▾ Voir texte brut OCR]          │
└──────────────────────────────────────────────────────────────────┘
```

## Stratégie parseur — Facture Rpartstore (analysée sur doc réel)

Problème : Tesseract extrait TOUT le texte de la page, y compris
les infos client (nom, adresse, immatriculation, KMS, n° agent).

Solution adoptée en 3 étapes :
  1. Détecter la ligne d'en-tête du tableau
     (contient "Désignation" ET "Référence")
  2. Ignorer toutes les lignes précédant cet en-tête (= infos client)
  3. Parser uniquement les lignes du corps du tableau :
     - Référence : suite de ≥6 chiffres consécutifs
     - Désignation : texte situé à gauche de la référence
     - Quantité : premier entier court après la référence
     - Prix HT : premier montant décimal (chiffres + virgule/point + 2 décimales)

Lignes ignorées après en-tête : Total, TVA, TTC, dates, n° facture

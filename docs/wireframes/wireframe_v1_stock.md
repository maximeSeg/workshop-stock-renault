# Wireframes V1 — Interface stock

**Semaine :** 5 — Présentés et validés par le client

## Écran principal — Tableau de stock

```
┌──────────────────────────────────────────────────────────────────┐
│  ◆ RENAULT  │  Stock pièces détachées  │ [+ Ajouter] [⬇ CSV]   │
├──────────────┬───────────────────────────────────────────────────┤
│              │  [6 réf.]  [OK:3]  [Faible:2]  [Rupture:1]       │
│  ▶ Stock     │  ⚠ 3 pièces à commander → Commander Rpartstore ↗ │
│              │                                                    │
│    OCR       │  [Recherche...  ] [Catégorie ▼] [État ▼] [Reset] │
│              │                                                    │
│    Import    │  Réf.         Désig.          Cat.   Qté   État   │
│    CSV       │  ─────────────────────────────────────────────    │
│              │  82 01 461    Plaquettes...   Frein  [−]6[+] ●OK  │
│    Historique│  16 40 600    Filtre huile    Filtr  [−]1[+] ⚠Fbl │
│              │  8200100      Télécommande    Autre  [−]0[+] ✕Rpt │
│    Paramètres│                                                    │
│              │  ── 6 référence(s) sur 6 ──────────────────────   │
└──────────────┴───────────────────────────────────────────────────┘
```

## Modal — Ajout / Modification de pièce

```
┌──────────────────────────────────────────┐
│  Ajouter une pièce                  [✕] │
│  ──────────────────────────────────────  │
│  Référence *      [                  ]   │
│  Catégorie        [Freinage         ▼]  │
│  Désignation *    [                  ]   │
│  Quantité  [0  ]  Seuil d'alerte [2  ]  │
│  Prix HT   [   ]  Emplacement    [   ]  │
│                                          │
│           [Annuler]  [✓ Enregistrer]    │
└──────────────────────────────────────────┘
```

## Retours client S5

- ✅ Interface claire pour les mécaniciens
- ✅ Boutons +/− très appréciés
- 🔄 Demande colonne Prix HT → intégré V2
- 🔄 Demande import facture automatique → OCR V2

# Bilan de projet

## KPIs atteints

| KPI                              | Cible      | Résultat         |
|----------------------------------|------------|------------------|
| Temps ajout pièce                | < 30s      | ~15s ✅          |
| Taux reconnaissance OCR          | > 80%      | 100% (nets) ✅   |
| Adoption équipe                  | 100%       | 100% ✅          |
| Ruptures non anticipées (J+30)   | 0          | 0 ✅             |

## Difficultés et solutions

1. **OCR capturait les infos client**
   → Détection de la ligne header du tableau pour isoler la zone produit

2. **localStorage limité (~5 Mo)**
   → Passage au fichier CSV portable en V3

3. **Encodage Excel France**
   → UTF-8 BOM ajouté au CSV pour compatibilité accents

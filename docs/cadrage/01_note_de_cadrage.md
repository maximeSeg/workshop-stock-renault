# Note de cadrage v1.0 — validée client

**Projet :** Logiciel de gestion de stock pièces détachées  
**Client :** Garage Léon Olivier — Renault, Saint-Ouen (93)  
**Chef de projet :** maximeSeg  
**Date :** Semaine 2 — validée par le client

---

## 1. Objet et finalité

Concevoir et livrer un logiciel web autonome permettant aux mécaniciens
du Garage Léon Olivier de gérer leur stock de pièces détachées Renault,
en remplacement du suivi papier actuel.

## 2. Périmètre

### Inclus (V1→V3)
- Catalogue pièces jusqu'à 1 000 références
- CRUD : ajout, modification, suppression, quantité +/−
- Filtres : catégorie, état du stock (OK / Faible / Rupture)
- Alertes de seuil + lien direct Rpartstore
- Import OCR des factures Rpartstore (Tesseract.js)
- Import/Export CSV
- Historique des mouvements

### Exclus (hors périmètre)
- Multi-utilisateurs / réseau (→ V4)
- Connexion API Rpartstore (→ V5)
- Application mobile native

## 3. Contraintes

| Type       | Description                        | Solution                  |
|------------|------------------------------------|---------------------------|
| Utilisateur | Mécaniciens non-techniciens       | UX simplifiée, 1 clic     |
| Technique  | Pas de serveur                     | HTML mono-fichier         |
| Budget     | 0 €                                | Open-source uniquement    |
| Délai      | 13 semaines                        | Itérations V1→V2→V3       |
| RGPD       | Données clients sur factures       | OCR 100% local            |

## 4. Planning macro

| Jalon | Semaine | Livrable                  |
|-------|---------|---------------------------|
| J1    | S1      | Réunion de cadrage (T0)   |
| J2    | S2      | Note de cadrage validée   |
| J3    | S5      | Wireframes V1             |
| J4    | S8      | Livraison V1              |
| J5    | S9      | Wireframes V2 (OCR)       |
| J6    | S11     | Réunion de clôture        |
| J7    | S13     | Soutenance                |

## 5. KPIs de succès

| Indicateur                      | Cible         |
|---------------------------------|---------------|
| Temps ajout pièce               | < 30 secondes |
| Taux reconnaissance OCR         | > 80%         |
| Adoption équipe mécaniciens     | 100%          |
| Ruptures non anticipées (J+30)  | 0             |

## Validation

☑ Note approuvée par le client — Semaine 2

# Architecture technique — Décision

## Solution retenue : application HTML mono-fichier

Après analyse des contraintes (pas de serveur, utilisateurs non-techniciens,
budget 0€), la solution retenue est une Single Page Application en
HTML/CSS/JavaScript pur, sans framework ni dépendance externe hors Tesseract.js.

## Stack technologique

| Couche    | Technologie        | Justification                           |
|-----------|--------------------|-----------------------------------------|
| UI        | HTML5 + CSS3       | Universel, aucune dépendance            |
| Logique   | JavaScript ES6+    | Natif navigateur, performances ok       |
| OCR       | Tesseract.js v5    | Open-source, 100% local                 |
| Cache     | localStorage       | Persistance entre sessions              |
| Stockage  | Fichier CSV        | Portable, compatible Excel              |

## Structure de l'application

```
gestion_stock_renault_v3.html
├── <style>           CSS complet (variables, layout, composants)
├── .sidebar          Navigation gauche (sombre)
├── .main-wrap
│   ├── #sec-stock    Tableau de stock + CRUD
│   ├── #sec-ocr      Import OCR facture Rpartstore
│   ├── #sec-import   Import CSV en masse
│   ├── #sec-history  Historique mouvements
│   └── #sec-settings Exports + paramètres
└── <script>
    ├── CSV Storage   stockToCSV(), csvToStock(), saveCSV()
    ├── Stock CRUD    renderTable(), chQty(), saveItem()
    ├── OCR Engine    parseRenaultInvoice(), runOCR()
    └── Import CSV    loadImportCSV(), confirmImportCSV()
```

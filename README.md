# JTIPilot v2

ERP de pilotage pour Responsable d'Agence d'intérim BTP — Île-de-France  
Stack : Vanilla HTML/CSS/JS · localStorage · Compatible GitHub Pages

## Usage local
Ouvrir `index.html` directement dans Chrome/Edge/Firefox.  
Toutes les données sont stockées localement (localStorage) — aucun serveur requis.

## Déploiement GitHub Pages
1. Pousser ce dossier sur un repo GitHub
2. Settings → Pages → Source: `main` branch, root `/`
3. L'URL sera : `https://[username].github.io/[repo]/`

## Modules
- **Aujourd'hui** — Dashboard opérationnel (démarrages, besoins, fins J-7, prospection)
- **CRM** — Prospects et clients (board Monday, fiche complète, météo, score, signaux)
- **Candidats** — Vivier intérimaires (CV, SMS, emails, marge, trajet, habilitations)
- **Missions** — Suivi missions actives (confirmation présence, clôture, carence)
- **TDB** — Tableau de bord (KPIs, prévisionnel, simulateur)
- **Marge** — Calculateur marge BTP + propale
- **P&L** — Simulateur compte de résultat
- **Radar** — Opportunités IA (analyse annonces, SIRET, arguments)
- **Référentiels** — Juridique, objections, ROME BTP
- **Paramètres** — Agence, objectifs, APIs

## LocalStorage
- `crm_btp_db` — Prospects et clients
- `cands_btp_v2` — Candidats intérimaires  
- `jtp_missions` — Missions actives
- `grilles_btp` — Grilles tarifaires
- `agence_btp` — Paramètres agence
- `tdb_cfg` — Configuration TDB

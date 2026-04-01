# JTIPilot v2 — Guide de déploiement

## Déploiement GitHub Pages

### 1. Structure des fichiers

Tous les fichiers doivent être dans le même dossier :

```
index.html              ← Page principale (Dashboard + CRM + Nav)
candidats_v2.html       ← Module Base Candidats
missions_v2.html        ← Module Missions
tdb_v2.html             ← Tableau de Bord RA
marge_v2.html           ← Fiche Marge + Calculateur
pl_v2.html              ← Simulateur P&L
radar_v2.html           ← Radar Opportunités + IA
refs_v2.html            ← Guide Juridique + Objections + ROME + Guide Marge
parametres_v2.html      ← Paramètres + Export/Import
marge_guide_v2.html     ← Redirect vers refs_v2.html
```

### 2. GitHub Pages

1. Créer un repo GitHub (ex: `JTIPilot`)
2. Uploader tous les fichiers .html à la racine
3. Settings → Pages → Source: `main` branch → `/root`
4. URL : `https://[username].github.io/JTIPilot/`

### 3. Premier lancement

1. Ouvrir `index.html`
2. Aller dans **Paramètres** → Renseigner les infos agence
3. Saisir les clés API si disponibles (Pappers, France Travail, Claude)
4. Cliquer **Enregistrer tout**

### 4. Migration depuis v4v (ancienne version)

Les données sont compatibles — même clés localStorage :
- `crm_btp_db` → Prospects et clients
- `cands_btp_v2` → Candidats
- `jtp_missions` → Missions
- `grilles_btp` → Grilles tarifaires
- `agence_btp` → Paramètres agence
- `tdb_cfg` → Configuration TDB

Pour migrer : Paramètres → Export JSON (dans l'ancienne version) → Importer JSON (dans la v2)

### 5. Test local (sans GitHub)

Ouvrir directement dans Chrome/Firefox via `file://` — **attention** : les notifications push ne fonctionnent pas en `file://`, uniquement en HTTPS (GitHub Pages).

Pour tester les notifications : utiliser GitHub Pages ou un serveur local (ex: `python3 -m http.server 8080`).

### 6. Cache navigateur GitHub Pages

Si une mise à jour ne s'affiche pas : ouvrir en **navigation privée** ou vider le cache (`Ctrl+Shift+R`).

---

## Raccourcis clavier (dans index.html)

| Touche | Action |
|--------|--------|
| `1` | Dashboard Today |
| `2` | Tableau de Bord |
| `3` | CRM Prospection |
| `4` | Base Candidats |
| `5` | Missions |
| `6` | Fiche Marge |
| `Escape` | Fermer drawer / modal |

---

## Données — Stockage localStorage

Toutes les données sont stockées localement dans votre navigateur.  
**Pas de serveur, pas de cloud, pas de synchronisation.**

Pour sauvegarder : **Paramètres → Export JSON complet** → sauvegarder le fichier .json  
Pour restaurer : **Paramètres → Importer JSON** → sélectionner le fichier

⚠️ Si vous videz les données du navigateur, les données JTIPilot sont perdues.  
Faire des exports réguliers.

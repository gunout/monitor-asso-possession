<div align="center">

## 🇫🇷 Monitor Asso Possession

> Dashboard de suivi des subventions aux associations de **La Possession** (La Réunion)

[![License: MIT](https://img.shields.io/badge/License-MIT-0033a0.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![Bash](https://img.shields.io/badge/Bash-5.0+-c8102e.svg?style=for-the-badge&logo=gnubash&logoColor=white)](https://www.gnu.org/software/bash/)
[![Chart.js](https://img.shields.io/badge/Chart.js-4.4-0033a0.svg?style=for-the-badge&logo=chartdotjs&logoColor=white)](https://www.chartjs.org/)
[![Data](https://img.shields.io/badge/Open_Data-Région_Réunion-c8102e.svg?style=for-the-badge)](https://data.regionreunion.com)

[![Status](https://img.shields.io/badge/Status-Active-1a7f37.svg?style=flat-square)]()
[![Couverture](https://img.shields.io/badge/Couverture-2022→2026-0033a0.svg?style=flat-square)]()
[![Associations](https://img.shields.io/badge/Associations-532-c8102e.svg?style=flat-square)]()
[![Total](https://img.shields.io/badge/Total-4.5_M€-0033a0.svg?style=flat-square)]()
[![Dernière MAJ](https://img.shields.io/badge/MAJ-Oct_2026-1a7f37.svg?style=flat-square)]()
</div>

---

## 📊 Aperçu

Dashboard interactif au **thème bleu-blanc-rouge** présentant **5 années de subventions** aux associations de La Possession, avec graphiques, tableaux et indicateurs clés.

| Année | Total | Associations | Source |
|:---:|---:|---:|:---|
| **2022** | 801 350 € | 88 | Dataset structuré |
| **2023** | 929 179 € | 128 | Dataset structuré |
| **2024** | 841 750 € | 106 | Dataset structuré |
| **2025** | 942 100 € | 99 | Délibération 03/04/2025 |
| **2026** | 1 017 600 € | 111 | Conseil municipal 18/02/2026 |

**📈 Évolution 2024 → 2026 : +20,9 %**

---

## ✨ Fonctionnalités

- 🇫🇷 **Thème bleu-blanc-rouge** (République française)
- 📊 **7 modules interactifs**
  - Vue d'ensemble (KPIs + évolution)
  - Évolution 2022→2026
  - Répartition thématique 2025
  - Top associations 2024
  - Subventions TCO
  - Fiches associations
  - Alertes
- 📈 **Graphiques Chart.js** (line, bar, doughnut)
- 🗂️ **Tableaux scrollables** avec en-têtes sticky
- 🎨 **Design responsive** (desktop, tablette, mobile)
- ⚡ **Génération automatique** depuis les sources Open Data

---

## 🚀 Installation

### Prérequis

- `bash` ≥ 4.0
- `curl`
- `jq`
- `python3` (pour le serveur local)

```bash
# macOS
brew install jq

# Debian / Ubuntu
sudo apt install jq curl
```

### Lancement

```bash
git clone https://github.com/gunout/monitor-asso-possession.git
cd monitor-asso-possession
chmod +x monitor.sh
./monitor.sh --once
```

Puis ouvrir :

```bash
open index.html          # macOS
xdg-open index.html      # Linux
```

Ou lancer le serveur local :

```bash
./monitor.sh --serve
# → http://localhost:8080/index.html
```

---

## 🛠️ Commandes

| Commande | Description |
|---|---|
| `./monitor.sh --once` | Génère `index.html` + `data.js` |
| `./monitor.sh --dashboard` | Idem (alias) |
| `./monitor.sh --serve` | Serveur HTTP local (port 8080) |
| `./monitor.sh --help` | Aide |

---

## 📁 Structure

```
monitor-asso-possession/
├── monitor.sh          # Script principal (génération)
├── index.html          # Dashboard (généré)
├── data.js             # Données JS (généré)
├── README.md
├── LICENSE
└── data/               # JSON intermédiaires
    ├── subv_2022.json
    ├── subv_2023.json
    ├── subv_2024.json
    ├── subv_2025_2026.json
    ├── tco.json
    └── fiches.json
```

---

## 🎨 Stack technique

| Composant | Technologie |
|---|---|
| Génération | Bash + `jq` |
| Dashboard | HTML5 + CSS3 (custom properties) |
| Graphiques | [Chart.js 4.4](https://www.chartjs.org/) |
| Typographie | JetBrains Mono + Inter |
| Sources | API Opendatasoft (Région Réunion) |

---

## 🔗 Sources de données

- [data.regionreunion.com](https://data.regionreunion.com) — Datasets subventions 2022-2024
- [data.gouv.fr](https://www.data.gouv.fr) — Organisation Mairie de La Possession
- Délibérations du conseil municipal (mars 2025, février 2026)
- [TCO](https://data.tco.re) — Subventions culturelles et Pulsation Patrimoine

---

## 📈 Modules du dashboard

### 📊 Vue d'ensemble
KPIs 2022-2026, courbe d'évolution, nombre d'associations par année.

### 📈 Évolution
Détail année par année avec courbe comparative.

### 🥧 Répartition 2025
Graphique doughnut par thématique (Sports, Culture, Vie de quartiers, Environnement, Scolaire, Social).

### 🏆 Top associations
Classement des 15 plus grosses subventions 2024.

### 🏛️ Subventions TCO
Pulsation Patrimoine, subventions culturelles 2026, T'COS.

### 📋 Fiches associations
Cartes synthétiques des associations clés.

### 🚨 Alertes
Diagnostic de disponibilité des données (2025/2026 en cours de publication).

---

## 🤝 Contribution

Les contributions sont bienvenues ! Pour proposer une amélioration :

1. Forkez le projet
2. Créez une branche (`git checkout -b feature/amelioration`)
3. Committez (`git commit -m 'Ajout fonctionnalité'`)
4. Poussez (`git push origin feature/amelioration`)
5. Ouvrez une Pull Request

---

## 📄 Licence

Ce projet est sous licence **MIT** — voir le fichier [LICENSE](LICENSE) pour plus de détails.

---

<div align="center">

## 👤 Auteur

**gunout** — [@gunout](https://github.com/gunout)
</div>

---

<p align="center">
  <sub>Fait avec ❤️ à La Réunion 🇷🇪</sub><br>
  <sub>Données ouvertes • Dashboard citoyen • Transparence publique</sub>
</p>

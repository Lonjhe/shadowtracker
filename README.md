# 🌟 Shadow Tracker

> Outil de suivi de collaborateurs — observations Shadow, démos, items observés et ressenti client.  
> Fonctionne entièrement dans le navigateur, sans serveur, sans compte, sans abonnement.

---

## 🔒 Confidentialité & stockage des données

**Aucune donnée n'est envoyée sur internet.**

Toutes les informations saisies dans l'application (collaborateurs, suivis Shadow, items, commentaires) sont stockées **uniquement dans le `localStorage` de votre navigateur**, sur votre appareil.

| Données | Où sont-elles stockées ? | Envoyées à un serveur ? |
|---|---|---|
| Noms des collaborateurs | Votre appareil (localStorage) | ❌ Jamais |
| Suivis Shadow | Votre appareil (localStorage) | ❌ Jamais |
| Items de checklist | Votre appareil (localStorage) | ❌ Jamais |
| Commentaires & notes | Votre appareil (localStorage) | ❌ Jamais |
| Mot de passe admin | Votre appareil (localStorage) | ❌ Jamais |

Le fichier hébergé sur GitHub Pages contient **uniquement le code de l'application** (HTML, CSS, JavaScript). GitHub ne reçoit aucune donnée métier.

---

## ⚠️ Important — ne pas perdre vos données

Le `localStorage` est lié à votre navigateur. Les données peuvent disparaître si vous :

- Videz le cache ou l'historique du navigateur
- Utilisez le mode navigation privée
- Désinstallez et réinstallez l'application
- Changez de navigateur sur le même appareil

**Recommendation : exportez régulièrement vos données via le bouton Export JSON dans la section Admin.**

---

## 📱 Utilisation

L'application est accessible via l'URL GitHub Pages depuis n'importe quel navigateur (iPhone, iPad, Mac, PC).  
Ajoutez la page à votre écran d'accueil sur iPhone pour une expérience app native.

### Ajouter à l'écran d'accueil (iPhone)
1. Ouvrez l'URL dans **Safari**
2. Appuyez sur le bouton **Partager** (rectangle avec une flèche)
3. Sélectionnez **Sur l'écran d'accueil**
4. Confirmez

---

## 🔄 Partager les données entre plusieurs appareils

Les données étant locales, elles ne se synchronisent pas automatiquement entre appareils.  
Pour travailler en équipe, utilisez le système d'**Export / Import JSON** intégré.

### Workflow quotidien recommandé

```
Matin :
  1. Un référent ouvre Admin → ↑ Export JSON
  2. Il partage le fichier .json via AirDrop ou iCloud Drive
  3. Chaque membre ouvre Admin → ↓ Import JSON

Soir :
  4. Chacun exporte ses suivis du jour
  5. Le référent consolide via Import JSON
```

### Règles de fusion à l'import
- Les suivis déjà présents (même identifiant unique) ne sont **pas dupliqués**
- Les nouveaux collaborateurs et items sont **ajoutés** sans écraser l'existant
- Aucune donnée n'est supprimée lors d'un import

---

## 🗂️ Fonctionnalités

### 📊 Magasin (tableau de bord)
- KPI en temps réel : taux de couverture, démos observées, moyenne d'items par shadow
- Graphique des items les plus observés
- Graphique de l'activité par semaine (8 dernières semaines)
- Top 5 collaborateurs avec barres de progression
- Liste des collaborateurs à relancer en priorité

### 👥 Équipe
- Vue grille de tous les collaborateurs avec compteur de shadows
- Ouverture d'un nouveau suivi Shadow en un tap
- Historique complet avec filtres par date et recherche textuelle
- Édition et suppression d'un suivi existant

### ⚙️ Admin (protégé par mot de passe)
- Ajout et suppression de collaborateurs
- Import de collaborateurs via fichier **CSV** (avec prévisualisation avant import)
- Suppression de tous les collaborateurs en une action (avec confirmation)
- Ajout et suppression des items de la checklist
- Changement du mot de passe admin
- **Export CSV** de tous les suivis
- **Export JSON** pour la synchronisation entre appareils
- **Import JSON** avec fusion intelligente

---

## 📄 Format CSV pour l'import de collaborateurs

Le fichier CSV peut utiliser `,` ou `;` comme séparateur.

```csv
nom,poste
Alice Dupont,Specialist
Thomas Bernard,Business Pro
Camille Martin,Expert
```

Les colonnes reconnues pour le nom : `nom`, `name`, `prenom`, `prénom`, `collaborateur`  
Les colonnes reconnues pour le poste : `poste`, `role`, `rôle`, `fonction`, `titre`, `job`

---

## 🛠️ Technologies utilisées

| Technologie | Usage |
|---|---|
| HTML / CSS / JavaScript | Application complète, aucun framework |
| [Chart.js 4](https://www.chartjs.org/) | Graphiques interactifs (CDN) |
| [Satoshi](https://www.fontshare.com/fonts/satoshi) | Typographie (CDN Fontshare) |
| `localStorage` | Stockage local des données |
| GitHub Pages | Hébergement du fichier statique |

---

## 🔐 Mot de passe admin par défaut

```
admin123
```

**Changez-le dès la première utilisation** via Admin → Sécurité & Export → Changer le mot de passe.

---

## 📦 Structure du projet

```
shadow_tracker.html   ← Fichier unique contenant l'application complète
README.md             ← Ce fichier
```

---

## 📝 Licence

Usage interne uniquement. Aucune donnée collectée, aucune télémétrie, aucun tracking.

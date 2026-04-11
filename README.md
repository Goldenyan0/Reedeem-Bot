# 🤖 Redeem BOT — Discord Reward Code Generator

<div align="center">

![Node.js](https://img.shields.io/badge/Node.js-339933?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Discord.js](https://img.shields.io/badge/Discord.js-5865F2?style=for-the-badge&logo=discord&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

**Bot Discord de génération de codes de récompense pour serveur GTA V RP**

</div>

---

## 📌 Présentation

**Redeem BOT** est un bot Discord permettant au staff d'un serveur GTA RP de **générer des codes de récompense uniques** pour les joueurs.

Les codes sont :
- Stockés en **base de données MySQL**
- Envoyés **en message privé** au joueur ciblé
- Notifiés dans le **salon Discord** configuré

### Types de récompenses supportés

| Type | Description |
|------|-------------|
| `money` | Attribuer de l'argent en jeu |
| `item` | Attribuer un objet en jeu |

---

## 🔑 Principe de fonctionnement

```
Staff → !create @Player money 5000
         ↓
    Génération du code unique
         ↓
    Insertion en base MySQL
         ↓
    Message privé → joueur
    Message public → salon Discord
```

---

## 🧰 Technologies utilisées

| Technologie | Rôle |
|-------------|------|
| **Node.js** | Runtime principal |
| **discord.js** | Interaction avec l'API Discord |
| **MySQL** | Stockage des codes générés |

---

## 🗃️ Structure de la base de données

Table : `codes`

| Colonne | Type | Description |
|---------|------|-------------|
| `code` | VARCHAR | Code unique généré |
| `type` | ENUM | Type de récompense (`money` / `item`) |
| `amount` | INT | Quantité attribuée |

---

## 💻 Commandes disponibles

### 🎟️ Créer un code
```
!create @user <type> <amount>
```

**Exemple :**
```
!create @Player money 5000
```

### 📖 Aide
```
!usage
```

---

## 🔐 Permissions

Seuls les membres possédant le rôle défini par `role_access_id` dans `config.json` peuvent utiliser les commandes du bot.

---

## ⚙️ Configuration

Fichier `config.json` à créer à la racine du projet :

```json
{
  "token": "BOT_TOKEN",
  "prefix": "!",
  "community_name": "Nom du serveur",
  "role_access_id": "ID_ROLE",
  "code_length": 8,
  "numbers_in_code": true,
  "database_host": "localhost",
  "database_user": "root",
  "database_password": "",
  "database_base": "dbname"
}
```

### Options de génération des codes

| Option | Description |
|--------|-------------|
| `code_length` | Longueur du code généré |
| `numbers_in_code: false` | Lettres uniquement |
| `numbers_in_code: true` | Lettres + chiffres |

---

## ▶️ Installation & lancement

### 1. Installer les dépendances
```bash
npm install
```

### 2. Configurer `config.json`
Renseigner le token Discord, les infos MySQL et l'ID du rôle autorisé.

### 3. Lancer le bot
```bash
node index.js
```

---

## ⚠️ Limites connues

- ❌ Pas de commande `redeem` côté Discord (création uniquement)
- ❌ Pas de protection contre les injections SQL
- ❌ Pas de vérification de doublons de codes
- ❌ Gestion d'erreurs minimale

---

## 🚀 Améliorations prévues

- [ ] Commande `!redeem <code>` pour utiliser un code
- [ ] Requêtes SQL préparées (sécurité)
- [ ] Expiration automatique des codes
- [ ] Vérification des doublons à la génération
- [ ] Logs admin et historique des codes utilisés
- [ ] Interface web d'administration

---

## 📊 Résumé

| Élément | Détail |
|---------|--------|
| **Langage** | Node.js |
| **Plateforme** | Discord |
| **Stockage** | MySQL |
| **Usage** | Outil staff — distribution de récompenses GTA RP |
| **Commandes** | `!create`, `!usage` |

---

<div align="center">
  <i>Outil staff pour serveur GTA V RolePlay — Génération & distribution de codes de récompense</i><br/>
  <i>Node.js · Discord.js · MySQL</i>
</div>

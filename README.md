🤖 Redeem BOT (GTA RP)
📌 Présentation

Ce bot Discord permet de générer des codes de récompense pour un serveur GTA RP.

Les codes créés sont stockés dans une base de données MySQL et peuvent être utilisés pour attribuer :

de l’argent (money)
des objets (item)
⚙️ Fonctionnement

Le bot permet à certains membres autorisés de créer des codes uniques destinés à d’autres joueurs.

🔑 Principe
Un staff génère un code via une commande
Le code est enregistré en base de données
Le joueur reçoit le code en message privé
Le serveur est informé de la création
🧰 Technologies utilisées
Node.js
discord.js
MySQL
🗃️ Base de données

Le bot utilise une table codes contenant :

code → code généré
type → type de récompense (money / item)
amount → quantité
🔐 Permissions

Seuls les utilisateurs ayant le rôle défini par role_access_id peuvent utiliser les commandes.

💻 Commandes
🎟️ Créer un code
!create @user <type> <amount>

Exemple :

!create @Player money 5000
📖 Aide
!usage
🧠 Détails techniques
Génération des codes
Longueur définie dans config.json
Possibilité d’inclure :
uniquement lettres
lettres + chiffres
Stockage
Insertion directe en base MySQL
Notifications
📩 Envoi du code en message privé
📢 Message dans le salon Discord
⚙️ Configuration

Fichier config.json :

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
▶️ Lancer le bot
npm install
node index.js
⚠️ Limites
Pas de système de redeem côté Discord (juste création des codes)
Pas de protection contre :
injections SQL
doublons de codes
Gestion d’erreurs minimale
🚀 Améliorations possibles
Ajouter une commande redeem
Sécuriser les requêtes SQL (requêtes préparées)
Ajouter une expiration des codes
Interface admin (logs, historique)
Vérification des codes déjà existants
📊 Résumé

👉 Ce bot sert principalement à :

générer des codes de récompense
les stocker en base
les envoyer aux joueurs

C’est donc un outil staff pour distribuer des récompenses sur un serveur GTA RP.

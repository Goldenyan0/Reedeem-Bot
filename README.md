🤖 Golden BOT
📌 Présentation

Golden BOT est un bot Discord développé pour faciliter la gestion d’un serveur tout en ajoutant des fonctionnalités de divertissement.

Il propose plusieurs catégories de commandes :

Modération (staff)
Statistiques
Musique
Fun
⚙️ Fonctionnalités
🛡️ Commandes Staff
ban <membre> → bannir un utilisateur
kick <membre> → expulser un utilisateur
clear <nombre> → supprimer un nombre de messages
📊 Commandes Statistiques
info <membre> → afficher les statistiques d’un utilisateur
stats → afficher les statistiques du serveur
🎵 Commandes Musique
play <url> → jouer une musique YouTube
skip → passer à la musique suivante
stop → arrêter la musique et déconnecter le bot
🎉 Commandes Fun
nitro → simule un gain de Nitro
meme → envoie un contenu humoristique
🧰 Technologies utilisées
Python
discord.py
API YouTube (lecture de musique)
🧩 Structure du projet (exemple)
golden-bot/
│── main.py
│── commands/
│   ├── moderation.py
│   ├── music.py
│   ├── fun.py
│   └── stats.py
│── config.json
│── requirements.txt
▶️ Installation
1. Cloner le projet
git clone https://github.com/ton-repo/golden-bot.git
cd golden-bot
2. Installer les dépendances
pip install -r requirements.txt
3. Configuration

Créer un fichier config.json :

{
  "token": "VOTRE_TOKEN_DISCORD"
}
🚀 Lancer le bot
python main.py
⚠️ Permissions nécessaires

Le bot doit avoir :

Administrateur (ou permissions spécifiques) :
Bannir des membres
Expulser des membres
Gérer les messages
Accès aux salons vocaux (pour la musique)
📉 Limites actuelles
Système musique dépendant de YouTube (peut casser selon les API)
Commandes basiques (pas de slash commands)
Peu de gestion d’erreurs
🚀 Améliorations possibles
Ajout des slash commands
Système de logs
Meilleure gestion des erreurs
Ajout de files d’attente musicale
Dashboard web
Permissions avancées (rôles)
📚 Auteur

Projet réalisé par Goldenyarn#5476

📄 Licence

Projet libre d’utilisation à but éducatif.

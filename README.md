# 📘 README – Automatisation & Déploiement Spring Boot avec Bash
🎯 Objectif du projet

Ce projet montre comment exécuter, arrêter, superviser et déployer une application Spring Boot dans un environnement de type Linux en utilisant des scripts Bash.
Il reproduit un contexte professionnel où les applications ne sont pas lancées depuis un IDE, mais via des scripts automatisés.

📁 Structure du projet

Le projet est organisé en deux parties :

src/ : contient le code de l’application Spring Boot

scripts/ : contient tous les scripts Bash utiles pour l’exécution, l’arrêt, la consultation des logs et le déploiement

logs/ : folder où seront enregistrés les fichiers de logs

pom.xml : configuration Maven

README.md : documentation du projet

Cette séparation améliore la clarté, la maintenance et la réutilisabilité.

# ⚙️ Technologies utilisées

Spring Boot (API REST)

Java 17+

Maven (build + exécution)

H2 Database (base en mémoire)

Bash (automatisation)

Linux-like environment (idéalement Git Bash ou WSL sous Windows)

📌 Fonctionnement des scripts Bash
🔹 Script de lancement

Démarre l’application Spring Boot en tâche de fond, tout en sauvegardant les logs dans un fichier dédié.

🔹 Script d’arrêt

Recherche le processus Spring Boot actif et le termine proprement.
Sur Windows, une version utilisant "taskkill" peut être utilisée.

🔹 Script des logs

Affiche les dernières lignes du fichier de logs pour faciliter la supervision et le debugging.

🔹 Script de déploiement

Compile le projet avec Maven, génère le fichier JAR puis lance la nouvelle version automatiquement.

# 🚀 Mise en route
1. Ouvrir un terminal compatible Bash

Sous Windows, utiliser Git Bash ou WSL, car PowerShell ne supporte pas les commandes Linux.

2. Donner les permissions d’exécution aux scripts (Linux/Git Bash)

Utiliser la commande d’attribution des droits d'exécution pour permettre l’appel des scripts.

3. Lancer l’application

Exécuter le script de démarrage pour mettre en route l’application Spring Boot.

4. Vérifier les logs

Consulter les logs récents grâce au script dédié, afin de s’assurer que l’application tourne correctement.

5. Arrêter le service

Utiliser le script d’arrêt pour libérer le port utilisé et stopper proprement l’application.

6. Accéder à l’application

Le serveur expose son API sur le port configuré via Spring Boot (par défaut : 8085).

# 🧪 Tests & Validation

Vérifier que l’application démarre sans erreurs

Vérifier que les logs sont correctement générés

Vérifier que le port 8085 est libéré après l’arrêt

Accéder à l’URL locale dans un navigateur

Tester le redémarrage complet


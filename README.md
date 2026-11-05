# Billed — débogage et tests d'une application de notes de frais

> Reprise d'une application SaaS de notes de frais : correction des bugs du parcours employé, écriture des tests unitaires et d'intégration avec Jest, et rédaction d'un plan de tests End-to-End.

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)
![Jest](https://img.shields.io/badge/Jest-C21325?logo=jest&logoColor=white)
![Testing Library](https://img.shields.io/badge/Testing_Library-E33332?logo=testinglibrary&logoColor=white)

## Sujet

Projet de formation OpenClassrooms. Billed édite des solutions SaaS pour les équipes RH. Suite au départ d'un développeur, la fonctionnalité « notes de frais » doit être fiabilisée en deux semaines : le back-end existe, mais le front-end contient des bugs et presque aucun test.

L'application propose deux parcours :
- **Employé** : se connecter, consulter ses notes de frais, en créer une avec un justificatif
- **Administrateur RH** : valider ou refuser les notes de frais

## Bugs corrigés

- Les notes de frais n'étaient pas triées : elles s'affichent désormais de la plus récente à la plus ancienne
- Connexion administrateur impossible : le formulaire lisait les champs du formulaire employé
- Le formulaire acceptait n'importe quel fichier comme justificatif : seuls les formats `.jpg`, `.jpeg` et `.png` sont acceptés

## Compétences acquises

- **Débogage** d'une application existante avec Chrome DevTools (points d'arrêt, inspection)
- **Tests unitaires** avec Jest et Testing Library (DOM, événements utilisateur)
- **Tests d'intégration** des appels API (GET et POST) avec un store mocké, y compris les erreurs 404 et 500
- **Couverture de code** suivie avec le rapport Jest (`--coverage`)
- **Plan de tests End-to-End** du parcours employé : [Bartz_Cyril_4_plan_test_052023.pdf](Bartz_Cyril_4_plan_test_052023.pdf)
- Lecture et compréhension d'un code écrit par d'autres

## Lancer le projet en local

```bash
npm install
npm test          # tests Jest + rapport de couverture
```

Pour utiliser l'interface, démarrer d'abord l'API fournie par OpenClassrooms ([Billed-app-FR-Back](https://github.com/OpenClassrooms-Student-Center/Billed-app-FR-Back), port 5678), puis servir ce dossier, par exemple avec `npx live-server`.

Comptes de test : `employee@test.tld` / `employee` et `admin@test.tld` / `admin`.

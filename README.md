# POPCORN 🍿

_Popcorn_ est une plateforme open source et (vraiment) sans frais ni commission qui aide les développeur-e-s freelance de {{MA_LOCALITE}} à trouver des projets : [Voir le site](https://{{MON_POPCORN}}.github.io/)

Les objectifs de _Popcorn_ pour les développeurs freelances :

- 📈 Etre un canal pour trouver des affaires à {{MA_LOCALITE}} sans commission ni intermédiaire
- 📗  Maitriser les fonctionnalités de la plateforme en contribuant à [la machine à Popcorn](https://github.com/popcorn-nantes/popcorn-machine).
- 💬 Faire circuler les tuyaux boulot entre freelances via le tchat.
- 💪 Offrir une alternative locale aux _market places_ de freelances centralisées

## Créer son profil

- Fork ce dépôt
- Ajoute ta fiche dans le dossier `content/persons` en prenant comme exemple le fichier `_exemple.md`. Le nom de ton fichier sera utilisé pour créer l'url de ton profil.
- Ajoute ta photo dans le dossier `/public/images` : **la photo doit faire 100ko maximum ⚠️**
- Fait une _pull request_ avec pour titre _Nouveau profil : {ton prénom}_ .
- Bienvenue sur _Popcorn_ ! ✨ Tu recevras également un mail pour t'inviter sur le tchat de _Popcorn_.

Pour soumettre une suggestion, signaler un bug, demander de l'aide, tu peux aussi tout simplement [ouvrir une issue sur ce repo](https://github.com/{{MON_POPCORN}}/{{MON_POPCORN}}/issues/new)

## FAQ

### Quelle est la différence avec des plateformes comme Malt ou Comet ?

- _Popcorn_ est une [association à but non-lucratif](https://opencollective.com/popcorn) et ne prélève pas de commission.
- _Popcorn_ est réservé aux **développeur·e·s de {{MA_LOCALITE}}**.
- _Popcorn_ est développé et maintenu par les développeur(e)s freelances eux-mêmes.
- _Popcorn_ n'est **pas** un intermédiaire ou une entreprise: les clients entrent directement en contact avec les freelances. _Popcorn_ ne joue aucun rôle dans les échanges qui suivent ensuite entre les deux parties.

## Documentation technique

Il s'agit d'un site généré statiquement par notre [machine à Popcorn](https://github.com/popcorn-nantes/popcorn-machine) qui repose sur [Nuxt.js](https://nuxtjs.org/).

## Installation

cloner ce dépôt puis

```sh
npm install
```

démarrer le serveur de dev

```sh
npm run dev
```

Générer la version statique du site

```sh
npm run generate
```

### Déployer

#### Configurer le repo

C'est la CI de travis qui s'occupe de publier le contenu statique généré sur le repo popcorn-{localite}.github.io (qu'il faut initialiser au préalable)

1. Générer un token sur github pour le dépot avec le droit de publish et de public_repo
2. Renseigner le token dans les settings de travis en ajoutant la variable d'environnement GITHUB_TOKEN récupérée à l'étape 1

#### Ajouter du contenu

3. merger la branche `master` dans la branche `published`
4. `git push`

Le déploiement du site est déclenché automatiquement par _Travis_ lors d'un _push_ sur la branche `published`. Il peut prendre quelques minutes avant d'être visible en production.

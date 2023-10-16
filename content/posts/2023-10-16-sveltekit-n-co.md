---
title: "Sveltekit & compagnie 🧡"
tags: [svelte, sveltekit, cloudflare, planetscale]
date: 2023-10-16T17:30:56+02:00
draft: false
ShowWordCount: true
---

Maintenant que j'ai quitté Django, j'ai besoin de vous parler de [Sveltekit](https://kit.svelte.dev/).

En regardant une vidéo plutôt intérressante de [Ben Davis](https://www.youtube.com/watch?v=vnkyMcw0TZE) j'ai décidé de tester un lot de nouvelles technologies qui semblent avoir une bonne synergie.

à savoir :
* SvelteKit
* DrizzleORM
* Vercel
* PlanetScale

## SvelteKit 🧡✨

est-ce un Framework, est-ce un Toolkit ? je ne sais pas mais d'après wikipedia il est classé comme [Framework Web](https://en.wikipedia.org/wiki/Svelte). Il se base sur __Svelte__, un langage et Framework de composants et lui apporte tout un tas de fonctionnalités pour gérer les requêtes côté client ET côté serveur.

L'un de ces avantages est la possibilité de le déployer sur pleins de plateformes différentes, allant du nodeJS au serverless.

Cependant il manque quelque chose pour créer une appli web dynamique : se connecter a une BDD et un ORM. Et c'est là qu'intervient [Drizzle](https://orm.drizzle.team/) !

## DrizzleORM 💧

Un ORM puissant et flexible apparu récemment sur le marché. Il promet d'être assez proche du SQL natif (moins d'abstraction).

Une comparaison un peu plus détaillée est disponible dans [cette vidéo de fireship](https://www.youtube.com/watch?v=4QN1BzxF8wM&ab_channel=BeyondFireship).

N'ayant jamais utilisé d'ORM typescript, je pourrais m'avancer un peu plus dessus dans un prochain article.

## PlanetScale & Vercel 💲🏎️

Je place ces deux outils dans le même paragraphe car ils sont tous les deux des solutions SaaS en mode abonnement. 
Même si c'est un point qui me rebute pas mal car cela implique une gestion des coups non maîtrisée, je dois avoué que j'ai été bluffé par les deux (free tier disponible).

Il permettent en contrepartie d'un delestage du portemonnaie d'accélérer la mise en production drastiquement.

### PlanetScale

PlanetScale est une BDD mysql compatible serverless (very nice 👍).

Celui-ci propose une interface entièrement Web très agréable et un système de branche du SGBD afin de pouvoir séparer la production du développement mais également de rendre les déploiement plus souples.

### Vercel

De l'autre côté Vercel est une plateforme all-in-one de Contiunous Delivery qui permet en quelques clics de mettre en production une application avec du TLS et ça c'est incroyable 😮

En résumé :
1. import depuis github/gitlab/...
2. définition des variables d'environnements (et un copié collé d'un `.env` suffit 🤩)
3. ajout d'un enregistrement dans le DNS

et voilà, appli en prod !

Alors déjà c'est très impressionnant, mais en plus de ça, on obtient des déploiements PAR COMMIT 🥲

Et bien évidemment toutes les logs, les metrics et insight sont également disponibles si on souhaite payer !


_Je me rend compte que je ne vous ai pas encore parlé de Playwright et Vitest... prochain article hehe_
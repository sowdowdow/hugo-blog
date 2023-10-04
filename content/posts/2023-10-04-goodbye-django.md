---
title: "Goodbye Django 🫡"
tags: [django, svelte, sveltekit, front-end, back-end]
date: 2023-10-04T16:45:21+02:00
draft: false
ShowWordCount: true
---

# Réflexion

Après avoir longtemps réfléchis, je me suis dis que construire une appli web rapidement c'est bien, mais dans un monde toujours plus concurrentiel, être capable de faire une app drivé par l'UX/UI est un gros avantage et quelque-chose qui e manquais avec django.

## Svelte & SvelteKIT

Traditionnellement (aka l'ancien monde), une application possède un __front-end__ et un __backend__. Et en front-end il existe aujourd'hui des Frameworks ultra populaires comme React, Vue et Angular. 

Ceci-dit, ils ont pour certain la réputation de soit être lent et peu efficace, soit avoir une courbe d'apprentissage très pentue.

Est apparue dans ce bel ecosystème [Svelte](https://svelte.dev/) 🤩, qui propose de la simplicité, et surtout qui est pré-compilé, au lieu d'avoir un virtual-DOM (bête noire d'Angular et React). Alors forçemment j'aime bien faire les choses différemment des autres, et je me suis laissé prendre au jeu.

_Eh ben c'est pas mal... franchement ça s'apprend très rapidement et on peut faire des choses très puissantes avec !_

## Intégration 💻↔️🖥️

Alors pour pousser le délire un peu plus loin j'ai essayé de l'intégrer avec Django Rest Framework (DRF) en backend.

Puis je me suis rendu compte qu'en fait SvelteKit possède un front ET un back. 🫥

Alors pour sécuriser les calls à l'API Rest de DRF, j'ai voulu faire en sorte que ce soit le backend de SvelteKIT qui fasse les requêtes. SAUF qu'en fait cela veut dire réécrire toutes les requêtes HTTP en rajoutant dans les en-têtes les cookies sessionid et csrf... 

__ultra-fastidieux__ 😖


_Il y a un problème là non ?_ 

Ben oui on a un front-end et DEUX back-end.
Alors pour éviter ça j'ai décider de réécrire le tout avec comme unique repository SvelteKit, pour le front ET le back.

La suite dans un prochain article (CloudFlare / PlanetScale / Vercel)
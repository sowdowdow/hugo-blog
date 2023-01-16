---
title: "Try Hard Django Partie 2 🐍"
tags: [python, django, tryhard]
date: 2023-01-15T10:34:12+01:00
draft: false
ShowWordCount: true
---

## Partie 5
Au deuxième jour de mon apprentissage je me suis concentré sur uniquement la partie 5 du tutoriel Django, pour cause ! Elle parle des Tests et observe donc un volume important.

Voilà ce que j'en retiens généralement : 

* Il faut écrire des tests, peut importe la quantité (mieux vaut trop que pas assez)
* Les débutants ne fonctionnent pas en TDD, mais il faut écrire des tests quand même
* Les tests c'est super pratique quand on est en équipe (pour ne pas casser le code du collègue et vice-versa)

Et d'un point de vue plus "tech" :
* on utilise beaucoup la fonction `from django.utils import timezone`
* on écrit une classe par Vue / Model au moins
* Il faut privilégier l'usage de `self.Assert<something>` plutôt que `assert`
* Il est possible de tester les vues dans le [shell](//google.fr/?q=python+manage.py+shell)
  * on importe l'environement `from django.setup.utils import setup_test_environment`
  * on l'applique `setup_test_environment()`
  * on peut ensuite faire des choses comme `r = client.get(reverse('polls:index'))`


## Partie 6
J'ai commencé la partie 6 du tutoriel sans succès, celle-ci traite des `STATIC_FILES`. Rendez-vous donc au prochain article pour la solution. 😉

## Svelte

Bon alors c'est quoi ? [Svelte](https://svelte.dev/) est un framework Javascript (comme React, Angular et Vue).

Alors pourquoi je m'intéresse à lui et pas aux mastodonte du secteur ?

D'abord parceque pas besoin d'apprendre le Typescript, on utilise les langages qu'on connaît (HTML, CSS, JS). Ensuite il n'utilise pas de VirtualDom et il est beaucoup plus performant que le reste de la concurrence ! 

À mon avis il s'imposera dans les [5 prochaines années](https://2022.stateofjs.com/en-US/libraries/front-end-frameworks/#front_end_frameworks_experience_linechart).

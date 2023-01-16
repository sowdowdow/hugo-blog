---
layout: blog
title: Try hard Django - partie 1 🐍
tags: [python, django, tryhard]
date: 2023-01-13T16:32:07.733Z
ShowWordCount: true
---
Je reprend donc l'apprentissage de Django en accéléré. J'ai pu revoir les 4 première partie du tutoriel du [site officiel](https://docs.djangoproject.com/fr/4.1/intro/tutorial04/).

Voici ce que j'ai pu revoir lors de ces 4 parties :

## Partie 1

La commande `python manage.py runserver` , les vues de base et le routing via le fichier `urls.py` .avec la fonction `path()` qui relie un url à quelque-chose.

## Partie 2

La deuxième partie s'ace autour de la définition des modèles dans `models.py`, leur activation via le `settings.py`, la création d'une migration, son dump en SQL brut et son application. On y joue également un peu avec [l'API django](https://docs.djangoproject.com/fr/4.1/intro/tutorial02/#playing-with-the-api) à travers la commande `python manage.py shell`. Pour finir, cette partie introduit l'interface d'administration à travers la création du **superuser** et l'enregistrement des modèles.

## Partie 3
C'est ici l'introduction en douceur de la gestion poussé des vues : utilisation d''argument en clé primaire, rédaction de template, [renvoie de context](https://docs.djangoproject.com/fr/4.1/intro/tutorial03/#a-shortcut-render) dans la méthode `render()`, gestion des 404, codage dynamique des urls via `{% url 'app:nom' argument %}` et pour finir les espaces de nom.

## Partie 4
La partie 4 se concentre sur [l'écriture d'un formulaire brut et son traitement](https://docs.djangoproject.com/fr/4.1/intro/tutorial04/#write-a-minimal-form), la gestion des erreurs via le `try: except:`, la redirection http, le raccourci `get_object_or_404()` et pour finir introduit les vues génériques.

Je ne me rappelle pas avoir utilisé ces vues génériques alors ce tutoriel vaut bien le coup !
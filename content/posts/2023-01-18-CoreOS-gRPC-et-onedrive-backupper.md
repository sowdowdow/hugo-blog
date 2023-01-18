---
title: "CoreOS, gRPC et onedrive-backupper"
tags: [CoreOS, gRPC, docker, onedrive-backupper]
date: 2023-01-15T17:48:25+01:00
draft: false
ShowWordCount: true
---

## CoreOS 🌱🐋
J'ai découvert hier [CoreOS](https://getfedora.org/coreos?stream=stable), c'est un système d'exploitation orienté container en rolling release. Qu'est-ce que ça veut dire ce charabiat ? Et bien une rolling release, c'est un OS qui est tout le temps à jour.

L'orientation container elle s'explique par quelque-chose de simple : il n'y a même pas de package manager (apt, pkg, snap, etc...) installé par défaut ! On peut juste y faire tourner des container et configurer l'OS avant même de le booter.

Il vise également a être remplacé facilement et clusterisé. Bref, pour faire tourner du container c'est plutôt sympathique.


## gRPC ↔️

J'en ai entendu parlé récemment mais pas encore mis en oeuvre. j'aimerais bien dès que j'en aurais le temps l'essayer.

C'est un framework RPC, ce qui veut dire qu'il implémente plusieurs standards de Remote Procedure Call (RPC) en bidirectionnel.

## Onedrive-backupper ☁️

Bon cette fois-ci ce n'est pas implémenté, mais promis je vais faire l'effort rapidement !

L'idée est de créer un container qui viendrait se plugger sur un volume docker pour en extraire un répertoire de fichiers, en créer un backup, et l'envoyer vers mon onedrive personnel pour faire des sauvegardes.
Créer une image docker qui viens se plugger sur un volume pour backupper + rotation a interval régulier des backups sur un système de fichiers.

Au fur et à mesure des optimisations pourrait-être ajoutés, je pense notamment à une rotation des backups, et l'ajout d'un client qui pourrait décompresser un backup d'une date spécifique pour le remettre en production.

Mais pour ce soir je vais déjà essayer de créer le script python qui permet simplement de sauvegarder un fichier dans onedrive sans interaction humaine. 😁

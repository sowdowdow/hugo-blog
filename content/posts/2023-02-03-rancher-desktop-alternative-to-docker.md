---
title: "Rancher Desktop, an Alternative to Docker"
tags: [rancher, docker, containerd, moby]
date: 2023-02-03T20:09:29+01:00
draft: false
ShowWordCount: true
---

Nous avons récemment fait face à un problème de taille au sein de mon équipe : la façon par défaut de travailler avec docker sur une machine windows est d'installer Docker Desktop. Or cet outil nécéssite une licence payant pour les entreprises de plus de 250 employés.

**Comment utiliser docker sur Windows sans passer par Docker Desktop ?**

Le premier reflexe que j'ai eu a été d'installer [Podman Desktop](https://podman-desktop.io/), une interface graphique accompagné d'un backend podman, une alternative à Docker que j'ai présenté dans l'article précédent.

à première vue très intérressant, celui-ci ne nous a pas spécialement désservie de par ses performances.
En effet une build native maven sur la même machine windows à pris ~2min30, tendis que podman aura passé près de 16 minutes pour la même tâche.

Il a donc fallu chercher ailleurs.

## Rancher Desktop

Sur les conseils d'un DevOps expérimenté, je me suis tourné vers [Rancher Desktop](https://rancherdesktop.io/), une solution alternative et qui propose plus de flexibilité.

Effectivement Rancher Desktop embarque un cluster Kubernetes qui tourne dans une instance WSL2 et il est capable de tourner sur deux backends distincts (*container engines*) : **containerd** ou **dockerd**. 

Dans un premier temps j'ai testé containerd, mais sans succès. Celui-ci nécéssite de fonctionner avec une CLI différente de dockerCLI, autrement dit on ne peut pas utiliser la commande `docker <command>`, il faut alors passer par la CLI `nerdctl`, mais celle-ci aura refusé de fonctionner dans notre cas.

## Moby

En changeant de container engine, donc de containerd vers dockerd on obtient une commande `docker` fonctionnelle. L'objectif de remplacer Docker Desktop par quelque-chose d'autre est atteint ! 🎊

ce fameux container engine *dockerd* est en fait [Moby](https://github.com/moby/moby). Quand le projet Docker à trop grossit, le monolithe a été splitté en plus petits composants. Un ensemble de ces composants s'est retrouvé dans le projet Moby.
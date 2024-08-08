---
title: Apprentissage de Golang 🐀 - partie 1
description: ""
date: 2024-08-08T14:15:44.087Z
preview: ""
draft: false
tags: [golang, apprentissage, GOPATH]
ShowWordCount: true
---

## $GOPATH
Le `$GOPATH` est une variable système qui détermine l'endroit on sont placé les packages go.
Ce même chemin contiendra par convention un dossier  🖿 `<mon_nom>.go` qui contiendra lui-même les projets.

## Packages
On peut créer des dossier dans lesquels on découpe le code en plusieurs fichiers.
Chaque fichier contient l'en-tête `package <nom_du_dossier>` le **nom_du_dossier** est une convention.

exemple :
```text
🖿 $GOPATH
|--- 🖿 src
		|---- 🖿 sowdowdow.go
		|		|---- main.go
		|		|---- 🖿 inputs
		|				|---- mouse.go <----- première ligne "package inputs"
		|				|---- keyboard.go  <----- première ligne "package inputs"
		|---- 🖿 organization.go
				|---- ...
```

## import

`import "<nom>"` permet de récupérer des fonctions, structs... depuis un autre package (= fichier différent).
ensuite on peut faire `<nom>.Fonction()`

## Organisation des fichiers

> ❗ Toujours TOUT stocker à l'intérieur du `$GOPATH` ❗

conventions de nommage :
 - nom de fichier.go en minuscule
 - dossier avec le même nom que le package
 
 ```text
🖿 $GOPATH
|--- 🖿 bin <---------- contient tous les binaires installés via `go install <nom>`
|--- 🖿 pkg <---------- bibliothèques intermédiaires
|--- 🖿 src <---------- projets perso triés par organisation
|		|---- 🖿 sowdowdow.go
|				|---- main.go
|				|---- ...
```

### sources

[cours Udemy de Robin Penea](https://www.udemy.com/course/le-langage-go-formation-complete/learn/lecture/12751087#overview), 2022
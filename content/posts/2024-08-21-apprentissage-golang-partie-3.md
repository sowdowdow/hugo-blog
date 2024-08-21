---
title: Apprentissage de Golang 🐀 - partie 3
description: ""
date: 2024-08-13T14:19:54.453Z
preview: ""
draft: false
tags: [golang, apprentissage, fonctions, array, slices]
ShowWordCount: true
---

## Conversion de type (casting)
exemple : 
```go
var a := int("2")
```
## fonctions
```go
func nom(param1 int, param2 string) string {}
```
La logique publique/privé s'applique toujours avec la première lettre en majuscule ou minuscule.

### retour multiples
```go
func nom() (int, string) {
	return 1, "example"
}

// first var ignored
_, text := nom()
```
## Array
Les tableaux ont une taille fixe
```go
var nom[5]int
// ou bien
tableau := [3]string{"bob", "moran"}
```
## Slices

Un Slice est un "array de taille dynamique"
```go
nums := make([]int, <taille>, <capacité>)
```
on double toujours la capacité initiale. Deux fonctions utiles pour vérifier capacité et taille sont : `len()` et `cap()`

## boucle for

```go
for <initialisation>;<condition>;<action> {
	// action
}
```
### boucle while
```go
for <condition> {
	// action
}
```
### forever
```go
for {
	// action
}
```
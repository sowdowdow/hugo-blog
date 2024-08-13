---
title: Apprentissage de Golang 🐀 - partie 2
description: ""
date: 2024-08-13T14:19:54.453Z
preview: ""
draft: false
tags: [golang, apprentissage, variables, modules, switch]
ShowWordCount: true
---

### Documentation
La liste des librairies standard : https://pkg.go.dev/std
## Variables
Elles sont **fortement typées** et il en existe plusieurs types : `bool`, `string`, `int`, `byte`, `float32`, `float64`
Il existe d'autres types comme `rune` pour l'unicode.

exemple d'usage  : `var age int = 20`
> short syntax : `nom := 123`

Première lettre en :
*  MAJUSCULE -> publique
* minuscule -> privé

## Module
1. go mod init <nom.go>
2. go mod tidy
3. ajouter ligne import `<nom.go>/<dossier>`

## Contrôle de flux
```go
if count := 1; count > 1 {
	...
}
```
la variable `count` ne sera accessible qu'entre les guillemets avec cette syntaxe.

Comme de nombreux langage, il existe le `switch` :
```go
switch <var> {
case <1>:
	// cas 1
case <2>:
	// cas 2
default:
	// cas par défaut
}
```
---
title: Back to Ubuntu
description: ""
date: 2024-06-08T15:57:59.772Z
draft: false
tags:
    - Atuin
    - Ubuntu
    - Front-matter
ShowWordCount: true
---

Après maintenant quelques mois consacrés au sport me voilà de nouveau dans la sphère apprentissage.

Je viens de recréer une VM Ubuntu 24.04 et cherche à nouveau les derniers outils tendance. 

## Atuin

J'ai ainsi trouvé un utilitaire qui viens remplacer l'historique classique linux par une BDD sqlite, permettant d'obtenir des stats mais également d'avoir un historique beaucoup plus long et potentiellement le synchroniser entre différentes machines. 

Cet utilitaire écrit en Rust se nomme [Atuin](https://atuin.sh/).

```bash
➜  hugo-blog git:(main) ✗ atuin stats
[▮▮▮▮▮▮▮▮▮▮] 40 ls         
[▮▮▮▮▮▮▮▮▮ ] 37 cd         
[▮▮▮▮▮▮▮▮▮ ] 36 rclone     
[▮▮▮▮      ] 19 resume     
[▮▮▮       ] 15 atuin      
[▮▮        ] 11 resumed    
[▮▮        ] 11 mkdir      
[▮▮        ] 11 nano       
[▮▮        ] 11 npm install
[▮▮        ] 10 exit       
Total commands:   410
Unique commands:  251
```
> exemple d'output de Atuin

## Front-Matter
Un second outil qui va me permettre également d'être plus rapide sur l'écriture d'article : [Front-Matter](https://marketplace.visualstudio.com/items?itemName=eliostruyf.vscode-front-matter).

Cette extension pour VSCode permet de gérer beaucoup plus simplement et efficacement le contennu de la pluspart des CMS, et dans mon cas Hugo.

## JSON resume

Étant également dans une période de recherche d'emploi j'ai très régulièrement des demandes concernant des références, un dossier technique, ou bien encore un CV dans un format un peu différent. Souhaitant structurer un peu mieux mon CV actuel, j'ai trouvé un outil qui se veux normalisé : [JSON Resume](https://jsonresume.org/).

Celui-ci comme son nom l'indique permet de créer un CV sous forme de JSON et de l'exporter au format html/pdf.
## Certifications

Depuis maintenant trois ans que j'exerce dans le milieu de l'IT je n'ai pas encore passé de certifications !
Je me suis donc renseigné pour savoir quels sont les formations qui sot les plus valorisés par les entreprises dans le milieu du DevOps, et voici quelques-unes d'entre elles :
- Docker Certified Associate (DCA)
- AWS Certified DevOps Engineer - Professional
    ou Microsoft Certified: DevOps Engineer Expert
    ou Google Professional Cloud DevOps Engineer
- Certified Kubernetes Administrator (CKA)
- HashiCorp Certified: Terraform Associate

Ces certifications coûtent cher et sont chronophage, j'ai donc interêt a bien étudier ces dernières avant de me jeter dans le bain. Docker étant l'outil que je connais depuis le plus longtemps il me semble cohérent de commencer par la première de ces certifications -> DCA.

Je vais donc y réfléchir plus sérieusement dans les semaines à venir car se fixer un tel objectif et le découper en étapes est le premier pas vers le succès.
---
title: "Try Hard Django Partie 3 🐍"
tags: [python, django, tryhard]
date: 2023-01-15T17:48:25+01:00
draft: false
ShowWordCount: true
---

## Partie 6 - Fichiers statiques
Finalement la partie 6 du tutoriel django était assez simple, j'avais juste besoin de redémarrer le serveur. 😋

## Partie 7 - Formulaire

Dans cette partie, on plonge dans les formulaires et la customisation de la vue d'administration. on y découvre comment rajouter un champ de recherche `search_fields`, un filtrage sur la date `list_filter`, mais aussi, et le plus important : l'inlining.

### Inlining

L'inlining permet de créer des sous-objets d'un objet directement dans la même vue. Par exemple créer les réponses à une question dans le même formulaire. pour ce faire on rajoute le champ `inlines` dans le ModelAdmin.
```python
class QuestionAdmin(admin.ModelAdmin):
    fieldsets = [
        (None, {'fields': ['question_text']}),
        ('Date Information', {'fields': ['pub_date']})
    ]
    inlines = [ChoiceInline] # <---------
    list_display = ["question_text", "pub_date", "was_published_recently"]
    list_filter = ['pub_date']
    search_fields = ['question_text']
```
celui-ci est lié a une classe qui lie un model avec un inline.
```python
class ChoiceInline(admin.TabularInline):
    model = Choice
    extra = 1
```

Pour terminer, cette partie quatre montre aussi comment surcharger le gabarit (template) d'une vue d'administration.

## Hors tuto : vues génériques

N'ayant pas tout vue des vues (haha...) j'ai décidé de pousser un peu plus loin l'apprentissage des vues génériques. 

J'y découvre alors qu'il est possible de créer des "vues sans vue". On défini uniquement un pointage de urls.py vers un template HTML.

Pour accélérer le développement il est également possible d'utiliser des vues très basiques de CRUD. Voici un exemple : 
```python
from django.views import generic

class CreateView(generic.CreateView):
    model = Question
    fields = ['question_text', 'pub_date']


class EditView(generic.edit.UpdateView):
    model = Question
    fields = ['question_text']
```

Ces deux vues nécéssitent tout de même la création d'un template dans `polls/templates/polls/question_form.html`.

Il est également important de noter que les autres vues génériques vont chercher un template avec un nom par défaut, sinon il faut le préciser via la propriété `template_name` (ex. `template_name = 'polls/index.html'`).


## Conclusion

Il me reste maintenant à voir l'authentification et je devrais être capable de réécrire le blog en Django. 💪
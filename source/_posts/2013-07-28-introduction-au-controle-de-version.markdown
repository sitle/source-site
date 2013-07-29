---
layout: post
title: "Introduction au contrôle de version"
date: 2013-07-28 17:26
comments: true
categories:
  - version
  - git
---
Bien que pour certains, faire du contrôle de version parait évident, pour d'autres (dont je fais indéniablement parti), ça ne l'est pas du tout. Revenir à une version antérieure, voir les modifications apportées à un fichier ou à un ensemble de fichier ou bosser sur un même script à plusieurs... ça ne me parle pas énormément (voir pas du tout dans certains cas).

Pourtant, force est de constater, pour ma part, que j'adopte déjà des pratiques assez similaires. En effet, avant de modifier un script (par exemple), je fais systèmatiquement une copie de sauvegarde de celui-ci en y ajoutant une date pour distinguer les différentes "versions". Il n'est pas rare de se retrouver dans ces conditions avec 50 copies d'un fichier dans le même répertoire.

Autre exemple, dans chaques entêtes de mes scripts, je mets systématiquement les changement apportés à celui-ci. Après plusieurs modifications, cette liste de changement est systématiquement sorti du script pour le mettre dans un fichier bien à part, celui-ci porte généralement le nom de "changelog".

Doit on faire du contrôle de version ? En fait, on le fait déjà, on ne sait simplement pas, qu'on le fait. Dans les articles qui vont suivre, je parlerais surtout de [Git](http://fr.wikipedia.org/wiki/Git). Celui-ci semble être un outil très interessant notamment du fait de sa décentralisation. On en reparlera...
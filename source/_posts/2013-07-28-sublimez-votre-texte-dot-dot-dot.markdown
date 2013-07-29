---
layout: post
title: "Sublimez votre texte ..."
date: 2013-07-28 12:53
comments: true
categories: 
  - sublime
  - editeur de texte
---

Mon éditeur de texte préféré est sans nul doute [ViM](http://fr.wikipedia.org/wiki/Vim), celui-ci se veut léger et totalement personalisable. Cependant, il n'est pas portable sur des systèmes non unix (à moins bien sûre d'installer certains prérequis tel que [Cygwin](http://fr.wikipedia.org/wiki/Cygwin) par exemple sur des systèmes "Microsoft Windows" mais, je trouve ça lourd juste pour un éditeur de texte...). [Eclipse](http://fr.wikipedia.org/wiki/Eclipse_%28projet%29) est portable sur différent système, cependant il est écrit en Java et suivant le système que vous utilisez, il peut être très très lent rien que pour son chargement. C'est là qu'entre en jeux [Sublime Text](http://www.sublimetext.com/).

Pour tout vous dire, je suis tombé dessus complètement par hasard (en regardant des conférences sur [Youtube](http://www.youtube.com)). Cet éditeur de texte fonctionne nativement sur tout les systèmes (OSX, Gnu/Linux et Microsoft Windows). Il a été conçu comme une extension à [ViM](http://fr.wikipedia.org/wiki/Vim) mais est très vite passé en mode "standalone". Il est personalisable, extensible et léger. Ce logiciel n'est pas gratuit mais bizarrement, vous pouvez l'utilisez indéfiniment (il n'a pas de date d'expiration). Il ne fait aucuns doutes qu'avec un tel modèle de licensing, il y a de très forte chance que j'achète la license si celui-ci correspond à mes besoins (tout de même extrêmement spécifiques). Passons directement à l'installation de ce produit.

## Installation de [Sublime Text](http://www.sublimetext.com/) sur ma Debian

Il existe des paquets sur internet pour Ubuntu ou Debian. Cependant, j'ai choisi de l'installer à partir du paquet source. Pas d'inquiétude, il n'y a pas de compilation à faire. L'archive contient un binaire et est téléchargeable via [ce lien](http://www.sublimetext.com/2). Une version 3 est en cours de gestation à l'heure où j'écris cette article et c'est cette version que j'ai choisi d'installer. 
### Récupération, décompression et implantation
Les commandes suivantes doivent être taper dans un terminal :
```bash
wget http://c758482.r82.cf2.rackcdn.com/sublime_text_3_build_3047_x64.tar.bz2
tar -xvjf sublime_text_3_build_3047_x64.tar.bz2
sudo mv sublime_text_3 /opt
sudo ln -s /opt/sublime_text_3/sublime_text /usr/bin/sublime
```
Etant donné que j'utilise Gnome3 sous ma Debian, je créé le fichier ```/usr/share/applications/sublime.desktop``` avec le contenu suivant :
```
[Desktop Entry]
Encoding=UTF-8
Version=3
Name=Sublime Text
GenericName=Editor
Type=Application
Exec=sublime
Icon=/opt/sublime_text_3/Icon/48x48/sublime-text.png
Categories=TextEditor;IDE;Development
```

## De quoi ça à l'air

On dit souvent qu'un dessin vaut mieux qu'un long discours. Voilà à quoi ressemble cet éditeur.
{% img /images/2013-07-28-sublimez-votre-texte-dot-dot-dot-1.png %}
Il ne paie pas de mine de prime abord mais il ne tient qu'à vous de le personnaliser comme bon vous semble. De toute manière, ça ne coûte rien de l'essayer...

## Pour conclure ...
Je ne couvre pas dans mon article les possibilités infinies de [Sublime Text](http://www.sublimetext.com/). Je vous laisse le soin de vous renseigner par vous même. Pour ma part, je l'utilise pour créer des articles ou créer des modules puppet avec la coloration syntaxique qui va bien en écran splitté avec une console en mode texte. Pour ce que j'en fais, je penses qu'il est une alternative viable en mode graphique.
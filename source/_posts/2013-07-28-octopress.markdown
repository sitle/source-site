---
layout: post
title: "Octopress, c'est quoi ?"
date: 2013-07-28 02:22
comments: true
categories: octopress 
---

[Octopress](http://octopress.org) c'est avant tout un moteur de blog tels que Wordpress par exemple. Il utilise le moteur [Jekyll](http://jekyllrb.com/) (écrit en [Ruby](http://fr.wikipedia.org/wiki/Ruby_on_rails)), celui-ci permet de générer des pages HTML statiques à partir de fichier texte au format [markdown](http://fr.wikipedia.org/wiki/Markdown). J'aime beaucoup ce format, je trouve qu'il se rapproche de la façon la plus naturelle d'écrire du texte.

Le principal avantage de cette solution, c'est qu'il n'a pas besoin de base de donnée comme backend. Il en résulte pas mal de chose. Premièrement, l'installation du serveur permettant la diffusion de notre blog est des plus simple (notre site étant entièrement statique). La deuxième chose, c'est qu'en terme de réactivité, il n'y a pas photo, le site réagit très rapidement. Autre avantage (et non des moindres), les pages web généré adopte d'office le principe du "[responsive design](http://fr.wikipedia.org/wiki/Responsive_Web_Design)". Celui-ci permet d'adapter le site à n'importe quel résolution d'écran, la mobilité étant dorénavant une donnée à ne pas négliger dans ce type d'application.

## Passons à l'installation du produit

Comme évoqué dans l'introduction, [Octopress](http://octopress.org) est basé sur [Jekyll](http://jekyllrb.com) et utilisant [Ruby](http://fr.wikipedia.org/wiki/Ruby_on_rails). Il nous faut installer un certain nombre de pré-requis.

### Pré-requis

Suivant le système que vous utilisez, ça sera plus ou moins simple à installer. Il faut surtout s'assurer que vous installer une version de [Ruby](http://fr.wikipedia.org/wiki/Ruby_on_rails) **"> 1.9.3"***. En ce qui me concerne et étant donné que le système d'exploitation que j'utilise est une Debian, j'installe ruby de cette manière :

```bash
sudo apt-get install ruby ruby-dev
```
*Le paquet 'ruby-dev' est nécessaire afin de pouvoir compiler et installer d'autres pré-requis par la suite.*

On va, ensuite, installer le gem bundler, celui-ci permet d'installer des gems plus rapidements. Etant donné qu'on a installé [Ruby](http://fr.wikipedia.org/wiki/Ruby_on_rails), il suffit de taper la commande suivante :

```bash
sudo gem install bundler
```

### C'est parti pour octopress !!!

[Octopress](http://octopress.org) est disponible directement sur [Github](https://github.com/imathis/octopress.git). Pour le récupérer, on va installer Git :
```bash
sudo apt-get install git-core
```
On va, ensuite créer un répertoire d'acceuil. Dans mon cas, je le met dans le répertoire '/home/mon_compte/Documents' mais libre à vous de le mettre ou bon vous semble. Autre précision, vous mettez le nom du répertoire que vous voulez. Ici, je l'appelle 'site'.
```bash
cd ~/Documents
mkdir site
cd site
```
On finit ensuite par le télécharger :
```bash
git clone git://github.com/imathis/octopress.git .
```
On a finit avec l'installation d'[Octopress](http://octopress.org), passons maintenant à sa configuration.

## Configuration

L'arborescence du produit est la suivante :
```
CHANGELOG.markdown
config.rb
config.ru
_config.yml
Gemfile
Gemfile.lock
plugins
Rakefile
README.markdown
```
Avant d'aller plus loin, il nous faut modifier le fichier *'_config.yml'*. Pas d'inquiétude, ce fichier est terriblement explicite. On va modifier l'entête comme ceci :
```
url: http://yoursite.com
title: Infrastructure
subtitle: 
author: Léonard TAVAE
simple_search: http://google.com/search
description:
```
On lance l'installation du thème par défaut :
```bash
rake install
```

## Création de notre première article

Pour créer notre première article, on lance la commande suivante :
```bash
rake new_post['mon premier post']
```
Cette commande va générer un fichier dans le répertoire "source/_posts", celui-ci est nommé avec le format suivant : *"ANNEE-MOIS-JOUR-mon-premier-post.markdown"*. C'est dans ce fichier que vous rédigerez votre article au format [markdown](http://fr.wikipedia.org/wiki/Markdown).

Quand vous avez fini, il faut générer votre site avec la commande suivante :
```bash
rake generate
```

Pour visualiser votre article, on va lancer un mini-serveur web avec la commande suivante :
```bash
rake preview
```

Ouvrez un navigateur et saisissez le lien suivant dans celui-ci :
```
http://localhost:4000
```

Pour résumer tout ça, le workflow restera toujours le même :

1. On créer un nouvel article ```rake new_post['mon_post']```
2. On édite l'article ```source/_posts/ANNEE-MOIS-JOUR-mon-post.markdown```
3. On regénère le site ```rake generate```
4. On visualise ```rake preview```

## Aller plus loin ...

Je n'ai pas traité le déploiement de votre site. En fait, pour le déployer, il suffit simplement de copier l'intégralité du répertoire *"public"* sur votre serveur web. Des méthodes automatisées sont possibles mais je ne les ai pas expérimenté moi même. Je vous invite à consulter le site d'Octopress directement pour cette partie.
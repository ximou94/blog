---
layout:     post
title:      Jekyll !!!
summary:    Petit tuto pour comprendre comment Jekyll marche
author:     Maxime Grangier
categories: Jekyll Tuto
---

[Jekyll](https://jekyllrb.com/) est generateur de site statique basé sur Ruby, tu auras donc besoin
d'installer Ruby sur ta machine.

## Si tu es sur linux:
  1. Installe ruby via la commande:
  {% highlight sh %}
  sudo apt-get install ruby ruby-dev make gcc nodejs
  {% endhighlight %}
  2. Puis le package gem pour installer Jekyll
  {% highlight sh %}
  gem install jekyll bundler
  {% endhighlight %}

## Si tu es sur windows:
  1. installe ruby [via le rubyinstaller](https://rubyinstaller.org/downloads/)
  2. Tu te laisse guider par le "wizzard" de mémoire tu laisse tous par défaut, à la fin un shell devrait s'ouvrir
  3. Tu lances les instructions dans l'ordre 1 puis 2 puis 3.
  4. Tu ouvres un prompt tu verifie que tu as bien ruby et gem d'installer avec la commande:
  {% highlight sh %}
  ruby -v
  gem -v
  {% endhighlight %}
  5. Si tu ne rencontre pas d'erreurs avec ces 2 commandes tu peux ensuite lancer la commande: 
{% highlight sh %}
gem install jekyll bundler
{% endhighlight %}
  6. Maintenant on verifie que Jekyll est bien installé :
{% highlight sh %}
jekyll -v
{% endhighlight %}

## Créer un site from "scratch"

Maintenant que ton environnement ruby est prêt on va pouvoir créer notre site !!

Pour cela rend toi dans tes documents ouvre un shell et lance la commande:
{% highlight sh %}
# Create a new Jekyll site at ./myblog
jekyll new myblog

# Change into your new directory
cd myblog

# Build the site on the preview server
bundle exec jekyll serve

# Now browse to http://localhost:4000
{% endhighlight %}

## Récuperer mon dépot github [ici](https://github.com/ximou94/blog)

Ensuite pour toi tous se passe dans le dossier _posts/

Pour rédiger tes articles tu as deux possibilités

  * Le html
  * [Le markdown](https://daringfireball.net/projects/markdown/basics)

Le nom de ton fichier doit respecter un format précis: *year-month-day-title*



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
### Code, with syntax highlighting

Here's an example of some ruby code with line anchors.

{% highlight php %}
namespace App\Providers;

use Illuminate\Support\Facades\Gate;
use Illuminate\Foundation\Support\Providers\AuthServiceProvider as ServiceProvider;

class AuthServiceProvider extends ServiceProvider
{
    /**
     * The policy mappings for the application.
     *
     * @var array
     */
    protected $policies = [
        'App\Model' => 'App\Policies\ModelPolicy',
    ];

    /**
     * Register any authentication / authorization services.
     *
     * @return void
     */
    public function boot()
    {
        $this->registerPolicies();

        //
    }
}

}
{% endhighlight %}

{% highlight ruby lineanchors %}
# The most awesome of classes
class Awesome < ActiveRecord::Base
  include EvenMoreAwesome

  validates_presence_of :something
  validates :email, email_format: true

  def initialize(email, name = nil)
    self.email = email
    self.name = name
    self.favorite_number = 12
    puts 'created awesomeness'
  end

  def email_format
    email =~ /\S+@\S+\.\S+/
  end
end
{% endhighlight %}

Here's some CSS:

{% highlight css %}
.foobar {
  /* Named colors rule */
  color: tomato;
}
{% endhighlight %}

Here's some JavaScript:

{% highlight js %}
var isPresent = require('is-present')

module.exports = function doStuff(things) {
  if (isPresent(things)) {
    doOtherStuff(things)
  }
}
{% endhighlight %}

Here's some HTML:

{% highlight html %}
<div class="m0 p0 bg-blue white">
  <h3 class="h1">Hello, world!</h3>
</div>
{% endhighlight %}

# Headings!

They're responsive, and well-proportioned (in `padding`, `line-height`, `margin`, and `font-size`).
They also heavily rely on the awesome utility, [BASSCSS](http://www.basscss.com/).

##### They draw the perfect amount of attention

This allows your content to have the proper informational and contextual hierarchy. Yay.

### There are lists, too

  * Apples
  * Oranges
  * Potatoes
  * Milk

  1. Mow the lawn
  2. Feed the dog
  3. Dance

### Images look great, too

![desk](https://cloud.githubusercontent.com/assets/1424573/3378137/abac6d7c-fbe6-11e3-8e09-55745b6a8176.png)

_![desk](https://cloud.githubusercontent.com/assets/1424573/3378137/abac6d7c-fbe6-11e3-8e09-55745b6a8176.png)_


### There are also pretty colors

Also the result of [BASSCSS](http://www.basscss.com/), you can <span class="bg-dark-gray white">highlight</span> certain components
of a <span class="red">post</span> <span class="mid-gray">with</span> <span class="green">CSS</span> <span class="orange">classes</span>.

I don't recommend using blue, though. It looks like a <span class="blue">link</span>.

### Footnotes!

Markdown footnotes are supported, and they look great! Simply put e.g. `[^1]` where you want the footnote to appear,[^1] and then add
the reference at the end of your markdown.

### Stylish blockquotes included

You can use the markdown quote syntax, `>` for simple quotes.

> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Suspendisse quis porta mauris.

However, you need to inject html if you'd like a citation footer. I will be working on a way to
hopefully sidestep this inconvenience.

<blockquote>
  <p>
    Perfection is achieved, not when there is nothing more to add, but when there is nothing left to take away.
  </p>
  <footer><cite title="Antoine de Saint-Exupéry">Antoine de Saint-Exupéry</cite></footer>
</blockquote>

### There's more being added all the time

Checkout the [Github repository](https://github.com/johnotander/pixyll) to request,
or add, features.

Happy writing.

---

[^1]: Important information that may distract from the main text can go in footnotes.

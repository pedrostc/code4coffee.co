---
layout: post
title:  "Automatização de tarefas"
date:   2015-12-04 10:30:15 -0200
categories: update automatizacao
published: false
---

Atualmente trabalho com desenvolvimento no ambiente Java (digo ambiente porque de vez em quando preciso escrever um script em Groovy ou decido criar uma meta ferramenta - código para me livrar de tarefas repetitivas como, por exemplo, abrir a tela do sistema que estou mexendo - em Scala, e por aí vai), e como todo desenvolvedor Java (no mínimo mediano), conhece o Maven... E ele acaba te deixando "mau acostumado" devido a suas facilidades, bastando um 'mvn clean package' pra que ele limpe o projeto, compile, execute testes de unidade e integração e empacote (dependendo da sua configuração, ele até faz o deploy pra você), sem contar que você não precisa ficar enchendo o seu controle de versões com suas dependências, apenas as define na configuração do arquivo (pom.xml)... Em parte por causa disso eu acabei ficando um bom tempo "preso" nesse ambiente, sem estudar coisas novas... Até que descobri que o Javascript/NodeJS também possui esse tipo de ferramenta, mesmo que de forma granulada (cada ferramenta tem uma finalidade específica).


You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: http://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
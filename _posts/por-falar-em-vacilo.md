---
layout: post
title:  "Por falar em vacilo..."
date:   2016-03-21 12:45:37 -0200
categories: jekyll update vacilo eldius
published: true
---


Pra começar bem esse negócio, vamos falar de vacilos que "um amigo" fez no código daquela aplicação que você trabalha...

Pra começar, precisamos deixar alguns conceitos base bem claros:
1. **NUNCA** devemos apagar um código legado, temos que manter ele lá para manter um histórico, mesmo que ele esteja em um controle de versão...
2. Se tem algo no código que você irá mexer que parece não fazer sentido, ele não merece atenção, ignore e siga adiante (se fosse importante você saberia)...

E pra exemplificar bem o que acabo de dizer, tenho um exemplo tirado de produção, que encontrei certa vez quando estava corrigindo um bug...

{% highlight java %}
    for ( Item item :itemList ) {
        if(item.getSubitem() != null) {
            Subitem subItem = sistemaRepository
                    .getSubitemById(item.getSubitemId().longValue());
            if(subItem != null){
            // continue;
            }
        }
        [...]
    }
{% endhighlight %}

Acredito que originalmente havia um motivo para que este if estivesse aí, porém alguém deve ter descoberto que esse *continue* estava dando problemas e comentou esta linha, como dito no primeiro ítem, e ignorou todo o resto, como dito no segundo...
Se você observar, ao ignorar o restante do código, mantiveram uma consulta ao banco de dados (que pode ou não fazer um fetch de joins) a cada elemento da iteração, levando a um tempo maior de execução do trecho de código...

Mas ao menos isso pode ser usado para quando o usuário reclamar de lentidão no sistema...

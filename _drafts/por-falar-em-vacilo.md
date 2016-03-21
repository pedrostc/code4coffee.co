---
layout: post
title:  "Por falar em vacilo..."
date:   2015-12-02 10:30:15 -0200
categories: jekyll update vacilo eldius
published: true
---


Pra começar bem esse negócio, vamos falar de vacilos que "um amigo" fez no código daquela aplicação que você trabalha...

Pra começar, precisamos deixar bem claro que *NUNCA* devemos apagar um código legado, temos que manter ele lá para manter um histórico, mesmo que ele esteja em um controle de versão...

Eu lembro que encontrei esse trecho de código quando estava corrigindo um bug... Acabou que ele chamou mais a atenção que o próprio bug...

{% highlight java %}
    for ( Item item :itemList ) {
        if(item.getSubitem() != null) {
            Subitem subItem = sistemaRepository.getSubitemById(item.getSubitemId().longValue());
            if(insumoStok != null){
            // continue;
            }
        }
        [...]
    }
{% endhighlight %}

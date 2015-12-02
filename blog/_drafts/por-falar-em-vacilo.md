---
layout: post
title:  "Por falar em vacilo..."
date:   2015-12-02 10:30:15 -0200
categories: jekyll update vacilo eldius
published: true
---


Pra começar bem esse negócio, vamos falar de vacilos que "um amigo" fez no código daquela aplicação que você trabalha...

Pra comelçar, precisamos saber que *NUNCA* devemos apagar código legado, temos que manter ele lá pra termos um histórico de código, mesmo que esse esteja em um controle de versão...

{% highlight java %}
    for ( Medicamento medicamento : medicamentoList ) {
        if(medicamento.getInsumoId() != null) {
            Insumo insumoStok = stokRepository.getInsumoById(medicamento.getInsumoId().longValue());				
            if(insumoStok != null){
            // continue;
            }
        }
        [...]
    }
{% endhighlight %}
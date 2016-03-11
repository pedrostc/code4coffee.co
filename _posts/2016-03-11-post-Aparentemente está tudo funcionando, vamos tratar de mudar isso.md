---
layout: post
title:  "Aparentemente está tudo funcionando, vamos tratar de mudar isso."
date:   2016-03-11 10:48:15 -0300
categories: jekyll update dev
comments: true
---
E está tudo funcionando com o ***static-publisher***.
Como não poderia deixar de ser eu tenho algumas coisas que quero implementar, creio que vou fazer um fork dele e brincar com essas funcionalidades.
Pretendo utilizar ele como base por quê ele já está preparado para o heroku e pq está funcionando e pq estou com preguiça de testar outro. XD
Algumas das funcionalidades que pretendo colocar são as seguintes:

 - Permitir instalar gems no deploy da aplicação no heroku (não sei se é exatamente possível, mesmo pq não saco mt ainda desse ambiente);
 - Permitir colocar as credênciais do GitHub para acessar repositórios privados no painel de administração (posso olhar como base o gitbook/nuts);
 - Talvez configurar repositórios diferentes para os posts e o site como um todo, não sei ao certo se vai ser muito legal/útil mas me pareceu interessante.
 - Adicionar o log na tela de administração, não quero ter q acessar o heroku pra verificar logs.

E é isso ai, vamos ver no que dá.
E sim, vou fazer o step-by-step de como foi fazer essa trosoba funcionar.
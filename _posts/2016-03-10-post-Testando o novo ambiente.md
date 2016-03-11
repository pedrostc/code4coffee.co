---
layout: post
title:  "Testando o novo ambiente"
date:   2016-03-10 22:19:15 -0300
categories: jekyll update dev
comments: true
---
Este post é para testar o ambiente de desenvolvimento que levantei para o Jekyll.
A ideia é levantar tudo que é necessário e subir uma aplicação no Heroku para "compilar" o blog e publicar automaticamente no S3.
A ação deve ser disparada através de um WebHook do GitHub que deve ser disparado quando for publicada uma atualização no branch Master do repositório do blog.
Outro ideia é manter no repositório apenas os artigos, para tal precisa ser dicidido como e aonde ficarão as configurações e os temas do blog.

Instalação do ambiente:

- JRE (o s3_website precisa);
- Ruby (renv facilita muito a vida);
- gem jekyll;
- gem jekyll-sitemap;
- gem s3_website.

Processo:

- Baixar o repositório do blog;
- escrever os artigos;
- jekyll build;
- s3_website push.
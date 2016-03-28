---
layout: post
title:  "GIT: Uma abordagem NatGeo"
date:   2016-03-15 14:30 -0300
categories: GIT, NatGeo
comments: true
author: Pedro Osternack Corrêa
---

# GIT - Uma abordagem NatGeo

## Objetivo

Este artigo tem por objetivo apresentar a ferramenta GIT e algumas de suas principais funcionalidades. Ele será desenvolvido tendo em mente os documentários sobre vida animal considerando 4 questões básicas:
- O que é?
- Aonde vive?
- Como se relaciona?
- Como se alimenta?

## 1. O que é?

Como é definido no [site oficial][GitScm] da ferramenta: 

> Git é um sistema de controle de versão distribuído, gratúito e de código aberto projetado para lidar com tudo, desde pequenas a grandes projetos com rapidez e eficiência.

Muito embora a definição acima seja muito direta e concisa, ficam ainda alguns pontos a serem definidos tais como, "O que é um controle de versão?".

Caso você seja um desenvolvedor de softwares a resposta mais simples é: algo que você deveria estar utilizando.

Um sistema controle de versão, basicamente, guarda, gerencia e controla versões de coisas, qualquer coisa, a bem da verdade qualquer arquivo digital. Este controle é feito em um **repositório** de arquivos que é, na prática, um banco de dados com todos as versões dos arquivos controlados.

O *git* não é o único de sua espécie, existem diversos outros sistemas de controle de versão como o *svn* e o *mercurial*. Cada um possui seus comportamentos específicos, habitats preferenciais e dinâmicas particulares. Nós vamos ignorar quase que completamente a existência desses outros sistemas, salvo em pontos aonde eles serviram como comparação, pois, como deve ter ficado explicito no título, o foco deste artigo é o *git*.

## 2. Aonde vive?

Como foi posto anteriormente, o *git* é um sistema de controle de versão distribuído. Ok, o que isso quer dizer?

Bem, isso quer dizer, de forma simples e direta, que o repositório dos arquivos não fica em apenas 1 lugar e sim distribuido em vários pontos diferentes. Que lugares tão diversos são estes? Eles são os computadores de todas as pessoas que estão acessando um repositório.

Cada pessoa que está trabalhando em um repositório no *git* possui uma cópia completa deste repositório armazenada localmente em seu computador. Sim, uma cópia ***completa*** do repositório, podendo navegar com toda a liberdade na árvore de versões dele, assim ***quase*** todas as operações são feitas localmente, sem necessidade de se comunicar com um servidor remoto.

Como comparação, no caso do *svn* o repositório fica única e exclusivamente em um servidor remoto (ok, caso a sua maquina seja o servidor ele é local, mas você entendeu a ideia.) e todas as operações são feitas diretamente neste servidor.

Você deve ter notado o "quase" em destaque. Ele está assim pois existem operações que são feitas remotamente. Em projetos compartillhados, ou qualquer projeto, pode ser utilizado um repositório remoto afim de possibilitar o acesso ao mesmo a todos os desenvolvedores no projeto em questão. Nestes casos os desenvolvedores irão se "comunicar" através deste repositório remoto. Isso não significa que os usuários vão usar somente o repositório remoto, cada um continua tendo o seu repositório local em suas maquinas e passa a ter um local aonde deixar a cópia de seus arquivos para que os demais tenham acesso. Este processo será descrito mais adiante.

## 3. Como é a sua organização social?



TODO: Descrever integração entre repositório local e remoto e de outros desenvolvedores, GitTree, branchs e afins.

## 4. Como se alimenta?
TODO: Descrever os principais processos de controle de versão, árvore de versões, staging area e processo de "commit".

## 5. Considerações gerais
TODO: Ferramentas e opções afim.

[GitScm]: https://git-scm.com/
---
layout: post
title:  "Criando logins para usuários órfãos no MS SQL Server"
date:   2016-11-02 15:50:00 -0400
categories: sql sqlserver mssql orphaned-users
published: true
---

**[tl;dr; cadê o código?](https://gist.github.com/pedrostc/6a429ae77485fbe3768eb36a09d8d1e4)**

Recentemente eu me deparei com uma situação interessante, me pediram para subir um banco SQL Server e recuperar o backup de uma aplicação existente, até então tudo certo, o ponto é, o controle de acesso de usuários a essa aplicação era feita utilizando a autenticação no banco, assim toda vez que algum usuário era criado no sistema ele era criado como um **login** no SQL Server e mapeado como um **user** no banco da aplicação com todas as regras de acesso sendo mapeadas da mesma forma. Legal né?

Um problema que isso traz é o fato de que o backup do banco só traz os dados e as regras de acesso, mas não os logins do dos usuários, ou seja, precisaríamos recriar todos os usuários novamente para que eles acessem o sistema sem problemas. Essa abordagem poderia provavelmente trazer outros problemas como problemas do remapeamento do novo login com o usuário já presente no banco, remapeamento das regras de acesso e afins, entre outras delícias.

Eu decidi usar uma abordagem um pouco mais simples e menos traumática, pelo menos a princípio, que consiste em utilizar a procedure **[sp_change_users_login](https://msdn.microsoft.com/en-us/library/ms174378.aspx)**. Essa proc facilita bastante o trabalho porém existem planos de remove-la em versões futuras do MSSQL, sendo assim o procedimento deverá ser feito através do **[ALTER USER](https://msdn.microsoft.com/en-us/library/ms176060.aspx)** em ambientes de trabalhos mais recentes. Como este caso era um suporte pontual, eu achei que a utilização dessa proc não traria muitos problemas.

Neste caso em específico eu precisava recuperar o acesso de 30+ usuários, fazer isso na mão seria um trabalho bem árduo então eu escrevi o seguinte código para facilitar a minha vida:

<script src="https://gist.github.com/pedrostc/6a429ae77485fbe3768eb36a09d8d1e4.js"></script>

Esse código faz basicamente 3 coisas:
1. Salva a lista de todos os usuários com problemas no banco atual e salva a lista em uma variável do tipo tabela;
2. Percorre a tabela e cria um novo login para cada um dos usuários listados nela e atualiza o mapeamento entre os dois.
3. Imprime no console um log do processamento para cada usuário.

Algumas observações:
- Como eu queria criar um novo login para os usuários eu passo o parâmetro *LoginName* da proc como *null*, sendo assim ela vai criar um novo login com o mesmo nome do usuário sendo processado;
- Caso eu passasse um nome no parâmetro *LoginName* a proc iria tentar apenas mapear o usuário para o login com o nome que eu informei e, já que neste caso os logins não existem, iria resultar em um erro;
- Eu deixei uma senha fixa para todos os novos logins para ser simples. Eu tenho noção de que isso é um problema de segurança e abre algumas brechas para usuários mal-intencionados fazerem besteira. Uma alternativa seria gerar as novas senhas por alguma função específica e adiciona-lo a saída de log no final do processamento do usuário.

Bem, por enquanto é só. Espero que alguém ache isso útil.

Até a próxima.
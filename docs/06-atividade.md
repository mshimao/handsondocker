# Atividade 06

## Acessando os containeres 

Nesta atividade vamos acessar o prompt do container e acessar os dados do MySQL a partir do VS Code.

#### Passo 1

Vamos habilitar a conexão de fora do container do usuário root do MySQL, para isso vamos acessar o prompt do container do MySQL.

Executar o comando `docker ps` para listar os containeres que estão sendo executados. Copie o nome do container do MySQL.

![docker ps](imagens/dockerps2.png)

#### Passo 2

Para acessar o bash do container do MySQL vamos usar o comando `docker exec -it handsondocker-db-1 /bin/bash`, sendo que handsondocker-db-1 é o nome do container.

![bash](imagens/containerbash.png)

#### Passo 3

Agora vamos logar no MySQL, usando o comando `mysql -u root -p`. Informar a senha "Agl@1234".

![mysql](imagens/mysqlprompt.png)

#### Passo 4

Vamos habilitar o usuário para login externo, usando o comando `ALTER USER 'root' IDENTIFIED WITH mysql_native_password BY 'Agl@1234';`.

![mysql](imagens/mysqlprompt2.png)

#### Passo 5

Vamos acessar o MySQL com o VS Code, para isso clicar no item "MYSQL" do panel Explorer do VS Code. E clicar no ícone "Add Connection".

![mysql](imagens/mysqlpanel.png)

Preencher o hostname com "localhost" e dar um enter.

![mysql](imagens/mysqlconn1.png)

Preencher o usuário com "root" e dar um enter.

![mysql](imagens/mysqlconn2.png)

Preencher a senha com "Agl@1234" e dar um enter.

![mysql](imagens/mysqlconn3.png)

Manter o valor 3306 no campo porta e dar um enter.

![mysql](imagens/mysqlconn4.png)

Manter o campo do certificado em branco e dar um enter

![mysql](imagens/mysqlconn5.png)

A conexão com o MySql vai aparecer no painel do VS Code.

![mysql](imagens/mysqlpanel2.png)

#### Passo 6

Vamos fazer uma query na tabela wp_posts da base de dados exampledb. Para isso, clicar no ícone ">" e abrir a lista de tabelas da base de dados exampledb.

![mysql](imagens/mysqltables.png)

Clicar com o botão direito do mouse sobre a tabela wp_posts e clicar na opção "Select Top 1000".

![mysql](imagens/mysqlquery.png)

Será executado a query e apresentado o resultado no VS Code.

![mysql](imagens/mysqlquery2.png)


Próximo: [Atividade 07](07-atividade.md)

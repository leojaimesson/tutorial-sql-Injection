<p align="center">
    <img src="img/brasao.png" alt="brasao da universidade federal do ceará." width="100px">
</p>

<h3 align="center">Universidade Federal do Ceará</h3>

<p align="center">Repositório dedicado para a elaboração de um laboratório sobre Injeção SQL para disciplina de Segurança da Informação.</p> 

---

## Sumário

- [Leia-me](#leia-me)
- [Objetivo](#objetivo)
- [Linguagem de Consulta Estruturada](#linguagem-de-consulta-estruturada)
- [Injeção SQL](#injeção-sql)
- [Ferramentas](#ferramentas)
- [Configuração de Ambiente](#configuração-de-ambiente)
- [Práticas](#práticas)

## Leia-me

Como previsto na **Lei 12.737/2012 no Art. 154-A**.  Invadir dispositivo informático alheio, conectado ou não à rede de computadores, mediante violação indevida de mecanismo de segurança e com o fim de obter, adulterar ou destruir dados ou informações sem autorização expressa ou tácita do titular do dispositivo ou instalar vulnerabilidades para obter vantagem ilícita, resultará em **Pena – detenção, de 3 (três) meses a 1 (um) ano, e multa**.

Lei Nº 12.737, de 30 de novembro de 2012.

## Objetivo

O objetivo deste laboratório será o de explorar e apresentar processos de detecção e exploração de falhas de injeção SQL.

## Linguagem de Consulta Estruturada

Linguagem de Consulta Estruturada ou SQL, é uma linguagem de pesquisa declarativa padrão de gerenciamento de dados que interage com os principais bancos de dados baseados no modelo relacional.

**Exemplos**:

SQL que retorna todos os elementos da tabela usuários:

```sql
SELECT * FROM usuarios;
```

SQL que retorna um usuário desde que seu login e sua senha sejam iguais aos campos passados:

```sql
SELECT * FROM usuarios WHERE login = 'campo_login' AND senha = 'campo_senha';
```
## Injeção SQL

**Injeção SQL trata-se de uma técnica para realizar ataques por meio de manipulação de código SQL**. O ataque ocorre quando o atacante consegue inserir uma série de instruções SQL dentro de uma consulta (*query*) através da manipulação das entradas de dados de uma aplicação.

**Exemplo**:

O atacante injeta os comandos sql no sistema alvo: 

![exemplo de injecao sql](img/exemplo_injecao_sql.png)

O resultado será que a consulta irá ficar da seguinte maneira:

```sql
SELECT * FROM Users WHERE Name ="" or ""="" AND Pass ="" or ""="";
```


## Ferramentas

**Ferramentas que serão utilizadas**:

[Vulnweb](http://testphp.vulnweb.com/) é uma aplicação web deliberadamente inseguro disponibilizado pela *Acunetix* que permite que desenvolvedores e estudantes interessados testem vulnerabilidades normalmente encontradas em aplicações baseados na linguagem de programação PHP que usam componentes de código comuns e populares. 

[SQLmap](http://sqlmap.org) é uma ferramenta de teste de penetração de software livre. Essa ferramenta permite automatizar o processo de detecção e exploração de falhas de injeção SQL. Ele vem com um poderoso mecanismo de detecção, diversos recursos para o testador de penetração e uma ampla variedade de opções como impressão digital do banco de dados, busca de dados do banco de dados, acesso ao sistema de arquivos subjacente e a execução de comandos no sistema operacional.


## Configuração de Ambiente

Neste laboratório será necessário a ferramenta *SQLmap* na versão 1.2.

Para baixar e descompactar a ferramenta execute os seguintes comandos:

```console
wget https://codeload.github.com/sqlmapproject/sqlmap/tar.gz/1.2 -O sqlmap-1.2.tar.gz
```

```console
tar -vzxf sqlmap-1.2.tar.gz
```

## Práticas
Para obter o passo a passo click em um dos links a seguir:
- [Injeção Manual](#)
- [Ferramenta SQLmap](https://raw.githubusercontent.com/leojaimesson/tutorial-sql-injection/master/pdf/Tutorial%20SQL%20Injection%20Com%20SQLMAP.pdf)
# Curso de Padrões de Projeto em Java na Prática

Plataforma: Udemy

Instrutor: Leonardo Moura Leitao (Cod3r)

---------------------------------------------------------------------------------------------------------------

## Padrões Criacionais

### Factory Method

Problemas: 
- classes instanciadas precisam variar dentro de uma mesma interface;
- deixar o código desacoplado das clases concretas.

Solução:
- extrair a lógica de criação de objetos para um método (factory method);
- invocar o factory method para receber uma instância qualquer que implemente uma determinada interface.

O padrão Factory Method sugere que você substitua chamadas diretas de construção de objetos (usando o operador new) por chamadas para um método fábrica especial (os objetos ainda são criados através do operador new, mas esse está sendo chamado de dentro do método fábrica).

#### Exemplo 1 - criação de Iphones

Antes de aplicar o padrão:

![image](https://github.com/user-attachments/assets/0987cb19-4102-41b0-bad0-6479e2e602a8)

Aplicando o padrão considerando uma factory por modelo de Iphone:

![image](https://github.com/user-attachments/assets/f3287c81-e154-4135-b54e-7f5ccfdd7c6c)

Aplicando o padrão considerando uma factory por versão de Iphone:

![image](https://github.com/user-attachments/assets/8c1db3f8-ae95-423c-97e6-edf99506dde4)

Aplicando o padrão considerando uma factory única para todos modelos de Iphone:

![image](https://github.com/user-attachments/assets/e53cce0d-0e21-473e-99a0-d027fa4ecdcb)

#### Exemplo 2 - criação de conexão com banco de dados

Antes de aplicar o padrão: 
- cliente instância diretamente a classe de conexão do banco de dados que será utilizado (Ex: OracleDb)
- se precisar mudar o banco de dados utilizado será necessário alterar o código e instânciar a classe do novo banco de dados.

Aplicando o padrão utilizando uma factory por tipo de banco de dados:

### Abstract Factory

Problemas:
- como escrever código onde as classes instanciadas possam variar dentro de uma mesma interface?
- como garantir que um conjunto de objetos relacionados possam ser criados mantendo o contexto único?

O Abstract Factory é um padrão de projeto criacional que permite que você produza famílias de objetos relacionados sem ter que especificar suas classes concretas.



---------------------------------------------------------------------------------------------------------------

## Padrões Estruturais

---------------------------------------------------------------------------------------------------------------

## Padrões Comportamentais

---------------------------------------------------------------------------------------------------------------

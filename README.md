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

Fornece uma interface para criação de **famílias de objetos** relacionados ou dependentes sem especificar suas classes concretas.

Diferentemente do Factory Method que trabalha com a factory baseada em uma interface/classe abstrata, por exemplo IPhone, o Abstract Factory trabalha com factory baseada em uma família de interfaces/classes abstratas relacionados ou dependentes.

#### Factory Method x Abstract Factory

![image](https://github.com/user-attachments/assets/c1c2ad70-22b6-4de8-afe5-5abcac81c1d9)

#### Diferentes maneiras de estruturar o Abstract Factory

Retornando serviços de usuários e carros para serem consumidos de uma maneira específica (REST ou EJB)

![image](https://github.com/user-attachments/assets/8e5403b0-de9e-4982-a3cb-921f6e2ec97f)

Retornando um serviço específico (usuário ou carro) e duas maneiras diferentes de ser usado (REST e EJB)

![image](https://github.com/user-attachments/assets/a21848e5-e98d-490b-8b52-2873e311e188)


### Singleton

Garantir que uma classe tenha somente uma instância e fornecer ponto global de acesso para a mesma.

Passos:
- Tornar o construtor private.
- Definir um ponto de criação estático para retornar a instância única.

### Builder

Separar a construção de um objeto complexo da sua representação de modo que o mesmo processo de construção possa criar diferentes representações.

Permite construir objetos complexos por etapas. Para isso deve-se constuir uma classe auxiliar, chamada de builder, que será responsável por construir o objeto desejado. Cada método da classe builder configura uma parte específica do objeto. 

É comum utilizar uma biblioteca chamada Fluent para implementação da classe builder pois essa biblioteca permite encadear chamadas de métodos de forma fácil.

#### Criação de objeto "Refeição de Fast Food"

![image](https://github.com/user-attachments/assets/537f6ce6-1019-48fa-b801-210c0bcd43f6)

### Prototype

Especificar os tipos de objetos a serem criados usando uma instância como protótipo e criar novos objetos pela cópia desse protótipo.



---------------------------------------------------------------------------------------------------------------

## Padrões Estruturais

Padrões que se preocupam com a forma como classes e objetos podem ser compostos para formar estruturas maiores. Eles utilizam a herança para compor interfaces ou implementações.

### Adapter

Permite que classes com interfaces incompatíveis trabalhem em conjunto.

#### Adapter de Objeto

![adapter-objeto](https://github.com/user-attachments/assets/0a985fdd-8333-4241-b4f0-a403d1f7d915)

#### Adapter de Classe

![adapter-classe](https://github.com/user-attachments/assets/8e1cf004-25e4-4a90-ac62-97079d426167)

### Bridge

Desacoplar uma abstração da sua implementação, de modo que as duas possam variar independentemente.

![design-patterns-bridge](https://github.com/user-attachments/assets/d5dc94ff-0bc7-4895-8c70-f28640207899)

### Composite

Trata parte e todo a partir de uma mesma interface, permitindo assim a criação de estruturas recursivas.

Estrutura de árvore é um bom exemplo de representação do padrão.

Exemplo de aplicação: sistema de arquivos onde a pasta e os arquivos possuem a mesma interface.

*Problema:*
- Como seria possível criar uma estrutura onde uma unidade e um conjunto delas possam ser tratadas de forma transparente e sem diferenças?

*Solução:*
- Definir uma composição que possa se comportar tanto como um elemento apenas ou como um conjunto desse elemento. 

> GOF: Compor objetos em estruturas de árvore para representar hierarquias todo-parte. Composite permite que clientes tratem objetos individuais e composições de objetos de maneira uniforme.

#### FileSystem

![alt text](design-patterns-composite.jpg)

### Decorator

Permite extender a funcionalidade de uma classe a partir de composição.

*Problema:*
Como adicionar funcionalidades dinamicamente em um objeto?

*Solução:*
Com objetos decorators é possível adicionar novas responsabilidades para um objeto.

> GOF: Anexar responsabilidades adicionais a um objeto dinamicamente. Decorators oferecem uma alternativa flexível ao usuo de herança para estender uma funcionalidade.

#### Coffe Shop

Incrementando bebidas existentes utilizando o padrão decorator:

![alt text](design-patterns-decorator.jpg)

---------------------------------------------------------------------------------------------------------------

## Padrões Comportamentais

---------------------------------------------------------------------------------------------------------------

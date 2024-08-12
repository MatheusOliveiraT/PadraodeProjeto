# Padrao de Projeto

Exercícios de aplicação de Padrões de Projeto

## Singleton

### Qual problema ele resolve?

O Singleton grante que uma classe tenha apenas uma única instância. Ele também foprnece um ponto de acesso global para aquela instância. Desta forma, ele viola o princípio de responsabilidade única. Por exemplo, caso eu queira ter uma instância que acessa um banco de dados e quero manter a consistência dos dados guardados, o Singleton pode ser de grande utilidade. Com apenas uma "porta" de acesso ao banco de dados, fica mais fácil de manter os dados organizados.

### Como ele resolve?

Para resolver isso o Singleton implementa um construtor especial, pois ele funciona de forma diferente do comum: ao construir o objeto pela primeira vez ele deve ser guardado para que seja retornado caso o construtor seja chamado novamente.

### Exemplo código:

No exemplo apresentado no arquivo <a href="https://github.com/MatheusOliveiraT/PadraodeProjeto/blob/main/singleton.py">singleton.py</a> a classe Singleton tem como metaclass SingletonMeta, esta que implementa a construção de objetos desse tipo. Ao executar o código é possível verificar que os dois objetos Singleton criados ao final referenciam a mesma instância.

### Exemplo UML:

<img width="500px" src="https://github.com/MatheusOliveiraT/PadraodeProjeto/blob/main/UML/singleton.png">

## Bridge

### Qual problema ele resolve?

O Bridge resolve o problema de escalabilidade quando acontece várias hierarquias importantes em uma implementação. No exemplo dado no <a href="https://refactoring.guru/pt-br/design-patterns/bridge">refactoring guru</a> é utilizado o exemplo de duas hierarquias importantes: forma e cor.

### Como ele resolve?

Para resolver esse problema o Bridge utiliza da composição para a classe ter duas dimensões diferentes, criando de fato duas hierarquias de herança. No problema exemplo, forma possui uma referência a cor, criando uma ponte entre as classes Forma e Cor.

### Exemplo código:

No exemplo apresentado no arquivo <a href="https://github.com/MatheusOliveiraT/PadraodeProjeto/blob/main/bridge.py">bridge.py</a> existe a classe Abstraction que faz ponte (Bridge) com Implementation, desta forma Abstraction pode ter suas classes filhas e continua ligado com a classe Implementation.

### Exemplo UML:

<img width="500px" src="https://github.com/MatheusOliveiraT/PadraodeProjeto/blob/main/UML/bridge.png">

## Fonte:

<a href="https://refactoring.guru/pt-br/design-patterns/bridge">Refactoring Guru</a>

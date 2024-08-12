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

## Iterator

### Qual problema ele resolve?

O Iterator resolve o problema de leitura/manipulação de coleção de dados. Existem diversas formas de armazenar dados, podendo ser listas simples, encadeadas, pilhas, árvores, entre outras. Cada estrutura tem uma maneira diferente de percorrer seus dados, então o Iterator vem para ir de elemento em elemento na coleção sem ter que acessar os mesmos elementos repetidamente. Quando se acessa listas contíguas, não necessariamente é um problema, porém ao acessar estruturas mais complexas pode se gerar um transtorno.

### Como ele resolve?

Para isso o Iterator extrai o comportamento de travessia de uma coleção para um objeto separado, chamado de iterador. A função deste é servir como interface de cada tipo de navegação, encapsulando todos os detalhes de travessia. Todos os iteradores devem implementar a mesma interface, para que o código seja compatível com qualquer tipo de coleção ou algoritmo de travessia desde que existe um iterador.

### Exemplo código:

Para criar um Iterator em Python existem duas classes abstratadas da biblioteca "collections": Iterable e Iterator.
No exemplo apresentado no arquivo <a href="https://github.com/MatheusOliveiraT/PadraodeProjeto/blob/main/iterator.py">iterator.py</a> existe a classe WordCollection que serve basicamente como uma lista de palavras (que é "iterável" por herdar Iterable), e existe a classe AlphabeticalOrderIterator que é um iterador de coleções do tipo WordCollection (herda Iterador). Ao passar por parâmetro a coleção mais a ordem de iteração a classe, a coleção chama o iterador com o método "--iter--" que percorre por toda a coleção. 

### Exemplo UML:

<img width="500px" src="https://github.com/MatheusOliveiraT/PadraodeProjeto/blob/main/UML/iterator.png">

## Fonte:

<a href="https://refactoring.guru/pt-br/design-patterns/bridge">Refactoring Guru</a>

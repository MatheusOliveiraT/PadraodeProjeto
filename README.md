# Padrao de Projeto

Exercícios de aplicação de Padrões de Projeto

## Singleton

### Qual problema ele resolve?

O Singleton grante que uma classe tenha apenas uma única instância. Ele também foprnece um ponto de acesso global para aquela instância. Desta forma, ele viola o princípio de responsabilidade única. Por exemplo, caso eu queira ter uma instância que acessa um banco de dados e quero manter a consistência dos dados guardados, o Singleton pode ser de grande utilidade. Com apenas uma "porta" de acesso ao banco de dados, fica mais fácil de manter os dados organizados.

### Como ele resolve?

Para resolver isso o Singleton implementa um construtor especial, pois ele funciona de forma diferente do comum: ao construir o objeto pela primeira vez ele deve ser guardado para que seja retornado caso o construtor seja chamado novamente.

### Exemplo

No exemplo apresentado no arquivo <a href="https://github.com/MatheusOliveiraT/PadraodeProjeto/blob/main/singleton.py">singleton.py</a> a classe Singleton tem como metaclass SingletonMeta, esta que implementa a construção de objetos desse tipo. Ao executar o código é possível verificar que os dois objetos Singleton criados ao final referenciam a mesma instância.

### Exemplo UML:

<img width="500px" src="https://github.com/MatheusOliveiraT/PadraodeProjeto/blob/main/UML/structure-pt-br.png">

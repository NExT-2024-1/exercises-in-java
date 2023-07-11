# Lógica estruturada

## Básico

1. Escreva um programa que, com base em uma temperatura em graus celsius, a converta e exiba em Kelvin (K), Réaumur (Re), Rankine (Ra) e Fahrenheit (F), seguindo as fórmulas: F = C * 1.8 + 32; K = C + 273.15; Re = C * 0.8; Ra = C * 1.8 + 32 + 459.67

2. Tem-se um conjunto de dados contendo a altura e o sexo (masculino, feminino) de 10 pessoas. Fazer um algoritmo que calcule e escreva:
a. a maior e a menor altura do grupo;
b. média de altura dos homens;
c. o número de mulheres.

3. Criar um programa que calcule a média de salários de uma empresa, pedindo ao usuário a grade de funcionários e os salários, e devolvendo a média salarial.

4. Uma parede em formato retangular, cuja altura é hp (altura da parede) e a largura lp (largura da parede) precisa ser coberta por azulejos também retangulares. O azulejo retangular tem dimensões ha (altura do azulejo) e la (largura do azulejo). Escreva um programa que leia as quatro medidas hp, lp, ha e la, calcule e imprima quanto azulejos com as medidas dadas são necessários para cobrir a parede dada.

5. Calcular e apresentar o valor do volume de uma lata de óleo, utilizando fórmula: V = 3.14159 * R * R * A, em que as variáveis: V, R e A representam respectivamente o volume, o raio e a altura.
Vamos declarar as variáveis V, R e A como double e definir um valor qualquer para as variáveis de altura e de raio. Agora vamos escrever a fórmula, conforme dita no enunciado e, em seguida, exibir na tela uma mensagem contendo o resultado do volume encontrado.

6. Escreva um programa para determinar a quantidade de cavalos necessários para se levantar uma massa de m quilogramas a uma altura de h metros em t segundos. Considere cavalos = (m * h / t) / 745,6999

## Repetições

7. Fazer uma classe Ex1Primos para:
    * Receber um inteiro N do usuário
    * Testar se este inteiro é primo ou não e informar
8. Fazer uma classe Ex2Sorteio para:
    * Sortear um número de 0 a 1000 (dica: usar Math.random())
    * Pedir um palpite ao usuário. Se ele errar, informar se o palpite é maior ou menor do que o número sorteado.
    * Pedir novos palpites até que o usuário acerte e, depois disso, mostrar em quantas tentativas ele acertou.
9. Fazer um programa para receber dois números do tipo int do usuário e determinar se um número é permutação do outro ou não. Ex: 431 é permutação de 143, 42 é permutação de 204, 1211 é permutação de 1112, etc. O programa só deve aceitar números positivos.

10. Fazer um programa para medir os reflexos do usuário. O programa deve:
    * Mostrar a palavra “Agora!” após um tempo aleatório e um número, também aleatório
    * Contar o tempo até que o usuário digite o número pedido e mostrar esse tempo.
    * Dicas: usar o método getTimeInMillis da classe Calendar ou o método nanoTime da classe System.

---

## vetores (Arrays)

11. Criar um vetor A com 5 elementos inteiros. Construir um vetor B de mesmo tipo e tamanho e com os "mesmos" elementos do vetor A, ou seja, B[i] = A[i].

12. Criar um vetor A com 8 elementos inteiros. Construir um vetor B de mesmo tipo e tamanho e com os elementos do vetor A multiplicados por 2, ou seja: B[i] = A[i] * 2.

13. Criar um vetor A com 15 elementos inteiros. Construir um vetor B de mesmo tipo e tamanho, sendo que cada elemento do vetor B deverá ser o quadrado do respectivo elemento de A, ou seja: B[i] = A[i] * A[I].

14. Criar um vetor A com 15 elementos inteiros. Construir um vetor B de mesmo tamanho, sendo que cada elemento do vetor B deverá ser a raiz quadrada do respectivo elemento de A, ou seja: B[i] = sqrt(A[i]).

15. Criar um vetor A com 10 elementos inteiros. Construir um vetor B de mesmo tipo e tamanho, sendo que cada elemento do vetor B deverá ser o respectivo elemento de A multiplicado por sua posição (ou índice), ou seja: B[i] = A[i] * i.

16. Criar dois vetores A e B cada um com 10 elementos inteiros. Construir um vetor C, onde cada elemento de C é a soma dos respectivos elementos em A e B, ou seja: C[i] = A[i] + B[i].

17. Criar dois vetores A e B cada um com 10 elementos inteiros. Construir um vetor C, onde cada elemento de C é a subtração dos respectivos elementos em A e B, ou seja: C[i] = A[i] – B[i].

18. Criar dois vetores A e B cada um com 10 elementos inteiros. Construir um vetor C, onde cada elemento de C é a multiplicação dos respectivos elementos em A e B, ou seja: C[i] = A[i] * B[i].

---

## String

19. Fazer uma classe ExecString que:
    * Recebe duas strings do usuário (usar TextConsole.getString())
    * Conta e informa quantas vezes a segunda string ocorre dentro da primeira
    * Informa uma estatística dos caracteres contidos nas 2 strings.
12. Faça um programa que receba um nome completo na forma de uma String e mostre a abreviatura deste nome. Não se devem abreviar as palavras com 2 ou menos letras. A abreviatura deve vir separada por pontos. Ex: Paulo Jose de Almeida Prado. Abreviatura: P. J. de A. P.

13. Fazer um programa que receba uma string do usuário e mostre o conteúdo desta string de forma invertida.

14. Um dos sistemas de encriptação mais antigos é atribuído a Júlio César: se uma letra a ser encriptada é a letra de número N do alfabeto, substitua-a com a letra (N+K), onde K é um número inteiro constante (César utilizava K = 3).
Usualmente consideramos o espaço como zero e todos os cálculos são realizados com módulo-27. Dessa forma, para K = 1 a mensagem “Ataque ao amanhecer” se torna “bubrfabpabnboifdfs”. Faça um programa que receba como entrada uma mensagem e um valor de J e retorne a mensagem criptografada pelo código de César. Fraquezas: apenas 26 chaves possíveis. É possível utilizar conhecimento da linguagem para facilitar a busca.

---

## Array

15. Fazer uma classe Ex3Array com as seguintes características:
    * Atributos: array de inteiros e duas variáveis para controlar o número atual e máximo de elementos inseridos no array
    * Métodos:
        - Construtor que recebe o tamanho do array como parâmetro e inicializa o objeto (cria array, etc.)
        - public boolean adicionar(int n) – adiciona elemento ao final do array, retornando true se bem sucedido e false caso contrário
        - public int calculaMedia() – retorna a média aritmética dos números armazenados no array

    Fazer a classe Ex3ArrayControle que:
    * Pergunta, via console, qual o tamanho N do array que o usuário quer instanciar
    * Instancia um objeto da classe Ex1Array, passando N como argumento
    * Pergunta N números ao usuário e armazena no objeto instanciado
    * Chama o método para calcular a média aritmética e mostra o resultado

16. Adaptar o exercício 3 para utilizar um objeto da classe ArrayList ao invés de um array comum.

17. Fazer um programa para receber um número do usuário e decompô-lo em fatores primos. Os fatores primos devem ser armazenados em um array com o tamanho exato (dica: primeiro determinar quantos são os fatores primos, depois criar o array para armazená-los).

18. A distância entre várias cidades é dada pela tabela abaixo (em km):

    |   |  1 |  2 |  3 |  4 |  5 |
    |:-:|:--:|:--:|:--:|:--:|:--:|
    | 1 | 00 | 15 | 30 | 05 | 12 |
    | 2 | 15 | 00 | 10 | 17 | 28 |
    | 3 | 30 | 10 | 00 | 03 | 11 |
    | 4 | 05 | 17 | 03 | 00 | 80 |
    | 5 | 12 | 28 | 11 | 80 | 00 |

    Implemente um programa que:
    * leia a tabela acima em um array bidimensional. O programa não deve perguntar distâncias já informadas (por exemplo, se o usuário já forneceu a distância entre 1 e 3 não é necessário informar a distância entre 3 e 1, que é a mesma) e também não deve perguntar a distância de uma cidade para ela mesma, que é 0.
    * leia um percurso fornecido pelo usuário em um array unidimensional. Calcule e mostre a distância percorrida. Por exemplo: dado o percurso 1, 2, 3, 2, 5, 1, 4, para a tabela mostrada como exemplo teremos: 15 + 10 + 10 + 28 + 12 + 5 = 80 km.

---

## Exceções

19. Adaptar o exercício 2 para:
    * lançar a exceção MenorQueException caso o número arriscado seja menor do que o sorteado
    * lançar a exceção MaiorQueException caso o número arriscado seja maior do que o sorteado
    * capturar essas exceções e tratá-las, mantendo a lógica original.
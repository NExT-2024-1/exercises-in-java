# Orientação a Objeto

## Básico
1. Criar a classe Pessoa com as seguintes características:
    * atributos: idade e dia, mês e ano de nascimento, nome da pessoa
    * métodos:
        - calculaIdade(), que recebe a data atual em dias, mês e an     -s e calcula e armazena no atributo idade a idade atual da pessoa
        - informaIdade(), que retorna o valor da idade
        - informaNome(), que retorna o nome da pessoa
        - ajustaDataDeNascimento(), que recebe dia, mês e ano de nascimento como parâmetros e preenche nos atributos correspondentes do objeto.
    * Criar dois objetos da classe Pessoa, um representando Albert Einstein (nascido em 14/3/1879) e o outro representando Isaac Newton (nascido em 4/1/1643)
    * Fazer uma classe principal que instancie os objetos, inicialize e mostre quais seriam as idades de Einstein e Newton caso estivessem vivos.

---

## Relacionamentos entre classes

3. Fazer um programa com as seguintes características:
    * Uma classe chamada Universidade que terá como atributo um nome e terá um método para informar o seu nome.
    * Relacionar a classe Pessoa para com a classe Universidade. Cada pessoa poderá ser associada a uma Universidade.
    * A classe Pessoa, por sua vez, terá um método que dirá seu nome e em que universidade trabalha.
    * Criar dois objetos da classe Pessoa, um representando Albert Einstein (nascido em 14/3/1879) e o outro representando Isaac Newton (nascido em 4/1/1643)
    * Criar dois objetos de Universidade, associando um para Einstein e outro para Newton.
        - Einstein trabalhou como professor de física em Princeton (Nova Jersey     - Estados Unidos da América).
        - Newton trabalhou como professor de matemática em Cambridge (Inglaterra).

4. Fazer um programa para:
    * Criar uma classe Departamento que permita relacionar um objeto (Departamento) à classe Universidade por composição (Universidade “contém” Departamento)
    * Adaptar a classe Pessoa para que ela possua uma referência ao departamento que trabalha, ou seja, ela deve possuir uma associação com a classe Departamento, permitindo que cada objeto Pessoa tenha a referência de um objeto Departamento.

    Adaptar o enunciado anterior para:

    * alterar a relação entre Universidade e Departamento para uma agregação, ou seja, uma Universidade pode inicialmente não ter Departamento porém eles podem ser criados posteriormente

    Adaptar o primeiro enunciado para:

    * Fazer com que uma Universidade possa ter 50 Departamentos.
    * Fazer com que um Departamento referencie a Universidade a qual está filiada.
    * Criar mais Departamentos filiando -os às Universidades.

5. Fazer uma classe Aluno que possua as seguintes características:
    * dois atributos do tipo inteiro: primeira nota parcial (de 0 a 100) e Segunda nota parcial (de 0 a 100)
    * um atributo String representando o nome do aluno
    * possua métodos para ler e escrever os atributos (ou uma construtora) 

    Fazer uma classe Controle que:

    * pergunte ao usuário o nome e as duas notas parciais de um aluno. Caso o nome entrado seja “fim” isso significa que o usuário não quer inserir mais nenhum aluno, do contrário deve ser instanciado um objeto da classe Aluno e armazenados os dados digitados.

        Dicas: usar um objeto da classe ArrayList de Java para armazenar as referências para os objetos instanciados). Usar o método equals da classe String para verificar se o valor do nome entrado é igual a “fim”. 

    * Calcular, ao final da inserção de todos os alunos, a média da turma, quantos alunos foram aprovados, quantos foram para a final e quantos foram reprovados e mostrar os códigos de todos os alunos cujas notas ficaram abaixo da média da turma.

6. Fazer um sistema de calculadora simples, composto das seguintes classes:

    CalcControle: controle da calculadora (“processador”), com os seguintes métodos:

    * public void executar() – faz a calculadora funcionar através dos seguintes passos:
        - Recebe primeiro operando do usuário através de CalcInterface e armazena no objeto de CalcDados
        - Recebe segundo operando do usuário através de CalcInterface e armazena no objeto de CalcDados
        - Recebe operação do usuário através de CalcInterface e armazena no objeto de CalcDados. Se a operação for igual a ‘s’, finaliza o programa (System.exit(0) ).
        - Executa a operação (método opera) e mostra o resultado através de CalcInterface.
        - Armazena resultado como primeiro operando para a próxima operação e volta para o segundo passo

    * private double opera(double opn1, double opn2, char op)   - executa a operação desejada e retorna o resultado.

    CalcDados: implementa a parte da calculadora que armazena os dados (operandos e operação) para o seu funcionamento (“memória”). Possui as seguintes características:

    Atributos: dois números do tipo double para armazenar os operandos e um dado do tipo char para armazenar a operação.

    Métodos:
    * public void setOperando(int i, double valor) – armazena o i   -ésimo operando com o valor expresso em valor
    * public double getOperando(int i) – retorna o valor do i   -ésimo operando
    * public void setOperacao(char op) – armazena o caracter op como sendo a operação atual
    * public char getOperacao() – retorna o valor da operação atual

    CalcInterface: implementa a parte da calculadora que coleta e exibe informações ao usuário (display e teclado da calculadora). Possui os métodos:
    * public double recebeOperando(int i) – recebe o operando i da operação (i vale 1 ou 2) e retorna.
    * public char recebeOperacao() – recebe um char representando uma operação válida (+,   -,    * ou /) e retorna.
    * public void mostraResultado(double res) – mostra o resultado recebido como parâmetro.

    Criar a classe Principal, cujo único objetivo é instanciar os objetos de controle, dados e interface e criar os vínculos (associações) entre eles. Todas as classes citadas devem possuir, além dos atributos citados, outros atributos que representem as referências para os outros objetos (criando as associações entre eles).

---

## Herança e polimorfismo
7. Implementar a classe PolReg, que define um polígono regular
    * Atributos: número de lados, tamanho do lado
    * Métodos: cálculo do perímetro, cálculo do ângulo interno e cálculo de área. Este último deve retornar o valor zero, dado que não é possível calcular a área de um polígono regular genérico
    * Construtora que inicializa os valores dos atributos

    Fazer a classe TrianguloEqderivada de PolReg, que:
    * redefine o método de cálculo de área para calcular e retornar a área do triângulo equilátero

    Fazer a classe Quadrado, também derivada de PolReg, que:
    * redefine o método de cálculo de área para calcular e retornar a área do quadrado

    Fazer um programa que:
    * pergunte ao usuário que tipo de objeto ele quer criar (polígono regular, triângulo equilátero ou quadrado)
    * pergunte número de lados (se for polígono regular) e tamanho dos lados
    * instancie o objeto e mostre o valor do perímetro, ângulo interno e área calculados

8. Escrever a classe Complexo, que pretende representar um modelo para a criação de números complexos. A classe Complexo deve possuir:
    * 2 atributos float: real e imag
    * 1 construtora que recebe a parte real e a parte imaginária do número e inicializa os atributos
    * 1 método Modulo() que retorna o módulo do número complexo.
    * 1 método Angulo() que retorna o ângulo do número complexo em graus.

    Escrever a classe Real, derivada da classe Complexo, que  retende representar um modelo para a criação de números reais. A classe Real deve:
    * possuir uma construtora que recebe o valor do número como parâmetro e chama a construtora da base.
    * adicionar o método Sinal(), que retorna 1 se o número for positivo e  -1 se for negativo.

    Escrever um programa em Java para testar estas classes (instanciar objetos, chamar métodos, etc.)

9. Escrever a classe Pessoa com as seguintes características:
    * atributos: nome e idade
    * métodos: construtora para inicializar os parâmetros e mostraDados() que exibe os dados da pessoa no console na forma:
    
        Nome da pessoa: xxx
    
        Idade da pessoa: yyy
    
    Escrever a classe Aluno, derivada de Pessoa, com as seguintes características:

    * atributos: nome do curso que está cursando
    * métodos: construtora para inicializar os atributos e redefinição do método mostraDados() para exibir as seguintes mensagens:

        Nome do aluno: xxx

        Idade do aluno: yyy

        Curso do aluno: zzz

    Elaborar um programa em Java que:
    * declare uma referência para objeto da classe Pessoa
    * pergunte ao usuário, via console, se ele deseja instanciar um aluno ou uma pessoa
    * crie o objeto correspondente, referencie com a referência já criada e chame o método mostraDados() para exibir os dados da pessoa ou do aluno

10. Alterar o exercício sobre polígonos regulares, triângulos e quadrados para que a classe PolReg não apresente uma definição para o método de cálculo de área; ou seja, a classe PolReg deve ser transformada em uma classe abstrata
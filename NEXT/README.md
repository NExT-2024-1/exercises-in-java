# Exercicios NExT

## HERANÇA

1. Uma loja tem 2 tipos de funcionários: vendedores e administrativos. Para ambos a empresa precisa ter o registro do nome e RG do funcionário.
    - Os vendedores têm um salário base, mas ganham também comissão de suas vendas. Os administrativos têm um salário base, mas podem ganhar horas extras adicionais.
    - Faça uma hierarquia de classes que tenha uma classe ancestral que implemente o que for comum aos dois tipos de funcionários e uma classe descendente para cada tipo.
    - Os vendedores devem ter um método que acumule o total de vendas durante o mês e um método que imprima seu salário total, considerando que a comissão é de 5%. 
    - Para os administrativos as horas extras é que são acumuladas e pagas com o valor de um centésimo do salário por hora. Nos dois casos, o método que imprime o salário a receber, zera os valores acumulados.
    Na classe principal, crie objetos e teste suas classes.

2. Crie duas classes: Funcionário e Gerente.
    - Gerente deve ser classe filha de Funcionário
        - Os atributos de Funcionário são: nome, CPF , salário e departamento
    - A classe Funcionário tem um método bonificar(), que não recebe nenhum parâmetro, e acrescenta 10% ao salário dele
    - A classe Gerente deve ter atributos adicionais de senha e número de funcionários gerenciados
    - A classe Gerente tem dois métodos a mais
        - O método autenticarSenha(String senha), que apenas compara a senha do parâmetro com o valor do atributo senha, retornando true ou False
        - O método bonificarGerente(), que acrescenta ao gerente o valor de 5% ao seu salário e mais 10% usando o método bonificar() do funcionário.
    
    Na classe principal, crie objetos e teste suas classes.

---

## POLIMORFISMO

3. Implemente em JAVA a seguinte situação:
    - Crie uma classe de Eletrônicos aos quais possuem as características consumo, voltagem e status; assim como os comportamentos ligar(que define o status para true), desligar(que define o status para false) e isLigado(que informa se o eletrônico está ligado)

    - Uma TV é um Eletrônico que possui polegada e canal. Ao utilizar o comportamento ligar seu status será ligado e o seu canal será modificado para 12.

4. Um Rádio também é um eletrônico que possui:
    - Características
        - AM / FM - ambos constantes, com valor 1 e 2, respectivamente
        - banda, sintonia e volume
    - Comportamentos
        - desligar
            - Torna seu status desligado(de acordo com a classe Eletrônico) e volume zero
        - ligar
            - Torna seu status ligado(de acordo com a classe Eletrônico) , sintonia 88.1 e volume 10.

---

# CLASSES ABSTRATAS E INTERFACES
5. Implemente, em Java, uma classe abstrata de nome Quadrilatero onde são declarados dois métodos abstratos: 
    - float calcularArea();
    - float calcularPerimetro();
    Crie, como subclasse de Quadrilatero, uma classe de nome Retangulo cujas instâncias são caracterizadas pelos atributos lado e altura ambos do tipo float.

    Implemente na classe Retangulo os métodos herdados de Quadrilatero e outros que ache necessários.

6. Implementar uma aplicação que declara uma Interface do tipo OperacaoMatematica que deve realizar uma operação matemática e imprimir o seu resultado, de acordo com o diagrama abaixo.

    - OBS 1: Não defina a e b como atributos. 
    - OBS 2: Implemente um construtor padrão para cada uma das classes.

![diagrama](/NEXT/images/interface.png)

7. Implemente as classes conforme o diagrama:
    - O método abastecer deve adicionar o valor passado por parâmetro ao atributo combustivelNoTanque
    - O método equals deve retornar true se o valor do atributo placa for o mesmo para os dois objetos.
    - Método viajar - Moto: o método deve considerar que uma moto faz 30km com 1 litro de combustível. Logo, deve verificar se o combustível no tanque é suficiente para percorrer a distância passada como parâmetro do método. Caso seja, deverá reduzir essa quantidade do atributo combustívelNoTanque e adicionar o valor da distância ao valor do atributo quilometragem. Retorne o valor true caso seja possível realizar a viagem. Caso contrário, retorne false.
    - Método viajar - Carro: Deve considerar que um carro faz 10km com um litro de combustível. Fazer as mesmas operações que as descritas no método viajar da classe Moto.
    - Na classe principal instancie objetos das classes implementadas e teste.

![diagrama](/NEXT/images/abstract.png)

---

## ASSOCIAÇÃO

8. Implemente as classes conforme o diagrama:
    - Lembre-se de implementar os métodos de acesso e definição.
    - Os construtores das classes
    
    Na classe principal crie instâncias das classes implementadas para teste.
---

# Proposta de projeto JAVA / POO

Ver modelo UML com as classes, as associações entre as classes, os atributos e os métodos a serem criados.

## CLASSES

1. Implementar classe conta – conforme diagrama UML.

2. Implementar classe conta corrente – conforme diagrama UML.

    a. Os métodos debitar e creditar devem, respectivamente, subtrair do saldo e adicionar ao saldo o valor recebido.

3. Implementar a classe conta poupança – conforme diagrama UML.
    
    a. O método debitar deve subtrair do saldo o valor recebido.
    
    b. O método debitar deve adicionar ao saldo o valor recebido mais o percentual do valor recebido correspondente à taxa de bônus.

4. Implementar o repositório de correntista – conforme diagrama UML e código de referência.

5. Implementar o repositório de conta – conforme diagrama UML e código de referência.

6. Implementar o mediator de correntista – conforme o diagrama UML, as funcionalidades (abaixo) e o código de referência.

7. Implementar o mediator de conta – conforme o diagrama UML, as funcionalidades (abaixo) e o código de referência.

8. Implementar a tela do sistema – conforme o diagrama UML e o código de referência.
    
## FUNCIONALIDADES (compõem o menu da tela).

9. Incluir correntista

    a. Ler os dados do correntista do teclado.

    b. Validar CPF (tem que ser maior que zero) e nome (tem que estar preenchido). Não é permitido haver CPF duplicado na lista de correntistas.

    c. Instanciar um objeto do tipo correntista.

    d. Incluir tal objeto no repositório que contém a lista de correntistas.

10. Incluir conta corrente ou conta poupança.

    a. Ler do teclado a opção de cadastrar conta corrente ou conta poupança.

    b. Ler os dados de uma conta corrente do teclado (número da agência, número da conta, CPF do correntista e tarifa. OU

    c. Ler os dados de uma conta poupança do teclado (número da agência, número da conta, CPF do correntista e taxa de bônus).

    d. Buscar o correntista pelo CPF informado.

    e. Validar CPF (tem que existir na lista de correntistas), número da agência (tem que ser maior que zero) e número da conta (tem que ser maior que zero), tarifa OU taxa de bônus (ambas têm que ser maior ou igual a zero). Não pode existir na lista de contas a combinação agência + número duplicada.

    f. Instanciar um objeto do tipo conta corrente ou conta poupança.

    g. Incluir tal objeto no repositório que contém a lista de contas.

11. Debitar

    a. Ler do teclado número da agência, o número da conta e valor a ser debitado.

    b. Validar o valor a ser debitado (deve ser maior que zero).

    c. Buscar a conta pelos números da agência e da conta informados.

    d. Se a conta for encontrada, realizar a operação de débito na conta. A operação de débito só deve ser realizada se o saldo da conta for maior ou igual ao valor a ser debitado.

12. Creditar

    a. Ler do teclado número da agência, o número da conta e valor a ser creditado.

    b. Validar o valor a ser creditado (deve ser maior que zero).

    c. Buscar a conta pelos números da agência e da conta informados.

    d. Se a conta for encontrada, realizar a operação de crédito na conta.

13. Listar contas ordenadas por saldo em ordem crescente.

    a. Consultar todas as contas do repositório.

    b. Ordenar o resultado por saldo em ordem decrescente.

    c. Mostrar no console a lista de contas (saldo, agência e número).

14. Listar correntistas ordenados por nome em ordem crescente.

    a. Consultar todos os correntistas do repositório.

    b. Ordenar o resultado por nome em ordem crescente.

    c. Mostrar no console a lista de correntistas (nome e cpf).

## DIAGRAMAS

Diagrama da conta Corretista
![diagrama corretista](/NEXT/images/contaCorrentista.jpg)

Diagrama do tipo produto
![diagrama corretista](/NEXT/images/produtoTipoProduto.jpg)
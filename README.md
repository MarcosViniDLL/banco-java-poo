# Sistema Bancário em Java

Este projeto é um sistema bancário simples desenvolvido em Java. Ele permite a criação de contas correntes e contas poupança, além de operações básicas como saque, depósito e transferência.

## Estrutura do Projeto

O projeto está estruturado em várias classes, cada uma responsável por diferentes aspectos do sistema bancário:

- **Banco.java**: Representa o banco e mantém uma lista de contas.
- **Cliente.java**: Representa um cliente do banco.
- **Conta.java**: Classe abstrata que representa uma conta bancária. Implementa as operações básicas de saque, depósito e transferência.
- **ContaCorrente.java**: Subclasse de Conta que representa uma conta corrente.
- **ContaPoupanca.java**: Subclasse de Conta que representa uma conta poupança.
- **IConta.java**: Interface que define as operações que uma conta deve implementar.
- **Main.java**: Classe principal que demonstra a criação de contas e a impressão de extratos.

## Funcionalidades

- **Criação de contas correntes e poupança**: Cada conta possui um cliente associado, uma agência, um número e um saldo.
- **Operações bancárias**:
  - Saque
  - Depósito
  - Transferência entre contas
- **Impressão de extratos**: Mostra as informações da conta, incluindo titular, agência, número e saldo.

## Exemplo de Uso

No método `main` da classe `Main.java`, criamos um cliente chamado Vinicius e associamos a ele uma conta corrente e uma conta poupança. Em seguida, imprimimos os extratos dessas contas.

```java
public class Main {
    public static void main(String[] args) {
        Cliente vinicius = new Cliente();
        vinicius.setNome("Vinicius");

        Conta cc = new ContaCorrente(vinicius);
        Conta poupanca = new ContaPoupanca(vinicius);

        cc.imprimirExtrato();
        poupanca.imprimirExtrato();
    }
}
```

A saída será algo como:

```
--- Extrato da Conta Corrente ---
Titular: Vinicius
Agencia: 1
Numero: 1
Saldo: 0.00

--- Extrato da Conta Poupança ---
Titular: Vinicius
Agencia: 1
Numero: 2
Saldo: 0.00
```

## Como Executar

1. Clone este repositório para a sua máquina local.
2. Compile as classes Java:
   ```sh
   javac Banco.java Cliente.java Conta.java ContaCorrente.java ContaPoupanca.java IConta.java Main.java
   ```
3. Execute a classe principal:
   ```sh
   java Main
   ```

## Contribuição

Sinta-se à vontade para contribuir com este projeto. Você pode abrir issues e enviar pull requests. 

## Observação

Este projeto é um desafio da Dio.

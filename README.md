## 👨‍💼 Simulador de Processo Seletivo em Java

Este projeto simula um processo seletivo automatizado com candidatos, entrevistas e tentativa de contato. Ele foi desenvolvido em Java e utiliza conceitos fundamentais da linguagem, como arrays, laços de repetição, métodos, geração de números aleatórios e controle de fluxo.

---

### 🎯 Objetivo

Automatizar o processo de:

* Avaliação de salário pretendido
* Seleção de candidatos
* Tentativas de contato telefônico com candidatos selecionados

---

### 📌 Funcionalidades

#### ✅ 1. `selecaoCandidato()`

Seleciona até **5 candidatos** com base no **salário pretendido** em relação ao salário base de R\$ 2000,00.

```java
if (salarioPretendido <= salarioBase) {
    // Candidato selecionado
}
```

Os salários pretendidos são gerados aleatoriamente entre **R\$1800 e R\$2200** usando:

```java
ThreadLocalRandom.current().nextDouble(1800, 2200);
```

---

#### ✅ 2. `entrandoEmContato(String candidato)`

Simula até **3 tentativas de ligação** para cada candidato. O atendimento ocorre com chance aleatória (1 em 3).

```java
boolean atendeu = new Random().nextInt(3) == 1;
```

Mensagens exibidas:

* **Contato realizado com sucesso**
* **Número máximo de tentativas atingido**

---

#### ✅ 3. `analisarCandidato(double salarioPretendido)`

Avalia o salário do candidato em relação ao salário base:

* Se for menor → **"LIGAR PARA CANDIDATO"**
* Se for igual → **"LIGAR PARA O CANDIDATO COM OUTRA PROPOSTA"**
* Se for maior → **"AGUARDANDO O RESULTADO DOS DEMAIS CANDIDATOS"**

---

#### ✅ 4. `imprimirSelecionados()`

Lista os candidatos com seus respectivos índices:

```
O candidato de nº 1 é FELIPE
O candidato de nº 2 é ARTUR
...
```

---

### 🧪 Exemplo de Execução

```text
O candidato FELIPE Solicitou este valor de salário 1984.23
o candidato FELIPE foi selecionado para a vaga

CONTATO REALIZADO COM SUCESSO
CONSEGUIMOS CONTATO COM FELIPE NA 2ª TENTATIVA
```

---

### 📂 Estrutura do Código

```java
main()                     // Chama os métodos principais
selecaoCandidato()         // Simula a seleção por salário
entrandoEmContato()        // Simula tentativas de ligação
analisarCandidato()        // Avalia salário pedido
valorPretendido()          // Gera salário aleatório
imprimirSelecionados()     // Lista os candidatos
```

---

### 📚 Conceitos Utilizados

* Estruturas de repetição (`for`, `while`, `do-while`)
* Vetores (`String[]`)
* Métodos reutilizáveis
* Geração de números aleatórios (`Random`, `ThreadLocalRandom`)
* Simulação de condições reais em processos seletivos
* Boas práticas de estruturação de código

---

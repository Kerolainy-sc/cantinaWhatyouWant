# Cantina UCB - Sistema de Gestão e Caixa 

Sistema desenvolvido em linguagem **C** para gerenciar o atendimento, o cálculo de pedidos, simulações de descontos e relatórios de vendas de uma cantina acadêmica. O projeto conta com validações robustas de entrada de dados, tratamento de erros e uma calculadora integrada.

---

## 🚀 Funcionalidades do Sistema

O programa apresenta um menu interativo com 5 opções principais:

1. **Novo Pedido:**
   * Permite escolher produtos por código com base em um cardápio pré-definido.
   * Solicita a quantidade desejada de cada item (validando valores maiores que zero).
   * Acumula múltiplos itens em um mesmo pedido.
   * Calcula automaticamente descontos progressivos com base no valor total bruto.
   * Atualiza as estatísticas globais da sessão.

2. **Calculadora Rápida:**
   * Uma mini calculadora com operações básicas: Soma, Subtração, Multiplicação e Divisão (com proteção contra divisão por zero).

3. **Simular Desconto:**
   * Permite inserir um valor arbitrário para testar o percentual e o valor do desconto progressivo que seria aplicado.

4. **Relatório da Sessão:**
   * Exibe um resumo consolidado contendo:
     * Total de pedidos realizados.
     * Quantidade total de itens vendidos.
     * Faturamento bruto.
     * Total de descontos concedidos.
     * Faturamento final líquido.

0. **Sair:**
   * Encerra a execução do programa com segurança.

---

## 📋 Cardápio e Regras de Negócio

### Produtos Disponíveis
| Código | Produto | Preço Unitário |
| :---: | :--- | :--- |
| **1** | Sanduíche | R$ 12,00 |
| **2** | Refrigerante | R$ 6,00 |
| **3** | Suco | R$ 8,00 |
| **4** | Salgado | R$ 7,00 |
| **5** | Café | R$ 4,00 |

### Faixas de Desconto Progressivo
O desconto é aplicado de acordo com o valor total bruto do pedido:
* **Abaixo de R$ 30,00:** `0%` de desconto
* **De R$ 30,00 a R$ 59,99:** `5%` de desconto
* **De R$ 60,00 a R$ 99,99:** `10%` de desconto
* **R$ 100,00 ou mais:** `15%` de desconto

---

## 🛠️ Tecnologias Utilizadas

* **Linguagem C** (Padrão C99 ou superior).
* Bibliotecas padrão: `<stdio.h>`.

---

## ⚙️ Como Compilar e Executar

Certifique-se de ter um compilador C instalado em sua máquina (como **GCC**, **Clang** ou **MinGW**).

### 1. Clonar ou baixar o repositório
Salve o código-fonte em um arquivo chamado `cantina.c`.

### 2. Compilar via terminal
Abra o terminal na pasta onde o arquivo foi salvo e execute o comando de compilação:
```bash
gcc cantina.c -o cantina

# Calculadora Pós-Fixada
Esse código implementa uma calculadora para avaliar expressões matemáticas na notação pós-fixada (também conhecida como notação polonesa reversa) e converter essas expressões para a notação infixa correspondente.


## Implementação

### Estrutura de Dados Utilizada

**Pilha:**  
A estrutura de pilha é utilizada para armazenar valores intermediários e subexpressões durante o processamento da expressão. Os principais elementos da pilha incluem:
- **Valores:** Array para armazenar números.
- **Expressão:** Array bidimensional para armazenar subexpressões em strings.
- **Topo:** Índice que aponta para o elemento mais recente.

---

### Funções

#### OperadorB e OperadorA
Identificam operadores e funções matemáticas:
- **OperadorB:** Reconhece operadores binários (`+`, `-`, `*`, `/`, `^`).
- **OperadorA:** Reconhece funções como `raiz`, `sen`, `cos`, `tg` e `log`.

#### ConversorRad
Converte valores de graus para radianos, necessários para cálculos trigonométricos.

#### getValor
Avalia expressões em notação pós-fixada:
1. Divide a string em tokens.
2. Verifica se o token é número ou operador.
3. Realiza operações binárias (com dois operandos) ou unárias (com um operando).
4. Retorna o valor final como resultado.

#### getFormaInFixa
Converte uma expressão pós-fixada para a notação infixa:
1. Empilha subexpressões como strings.
2. Combina subexpressões para formar expressões infixas com parênteses.
3. Retorna a expressão final em formato infixo.

#### main
1. Processa várias expressões pós-fixadas.
2. Usa `getValor` para calcular o resultado e `getFormaInFixa` para obter a notação infixa.
3. Exibe os resultados na tela.

---

## Características e Funcionalidades

- **Suporte a Operadores e Funções Matemáticas:**
  - Operações básicas (`+`, `-`, `*`, `/`, `^`).
  - Funções trigonométricas (`sen`, `cos`, `tg`) e logarítmicas.
  - Conversão entre graus e radianos.

- **Suporte a Decimais e Números Negativos:**
  - Permite cálculos complexos com precisão.

- **Tratamento de Erros:**
  - Verifica condições como divisão por zero e operações inválidas.

---

## Limitações

1. **Tamanho da Pilha:**  
   Expressões muito grandes podem exceder o tamanho máximo da pilha.
   
2. **Precisão Numérica:**  
   Atualmente utiliza `float`, o que pode limitar a precisão com números muito grandes ou pequenos. O uso de `double` é recomendado para maior precisão.

---
## Como Usar

1. Clone o repositório:
    ```sh
    git clone https://github.com/LeticiaParreiras/Calculadora_PosFixia.git
    ```
2. Navegue até o diretório do projeto:
    ```sh
    cd Calculadora_PosFixia
    ```
3. Compile o código:
    ```sh
    gcc -o calculadora main.c
    ```
4. Execute a calculadora:
    ```sh
    ./calculadora
    ```


<img src="https://drive.google.com/uc?id=1SOzRTjUt7cuBJpSqoK90fcAiKBrnpUJo" width="400">

**Curso:** Engenharia Civil
**Disciplina:**  Raciocinio Logico e Algoritmos
**Código/Turma:** T998-21
**Professor:** Ricardo Carubbi <br>
**Data:** 22/03
**Aluno(a):** Cauã Aguiar
**Matrícula:** 2410595

**1a chamada (Sim/Não):** SIM  <br>
**2a chamada (Sim/Não):** preencha com a opção correta

# Avaliação Diagnóstica 1

## Normas e exigências

Avaliação diagnóstica (**AD**) consiste em exercícios ou projetos desenvolvidos em grupo ao longo da disciplina. <br>
A primeira avaliação diagnóstica (**AD1**) será composta por exercícios e equivale a 30% da nota da primeira avaliação (**AV1**).

Segue abaixo a expressão para o cálculo da **AV1**, sendo sendo **AF1** equivale a primeira avaliação formativa e **AD1**, a primeira avaliação diagnóstica.

$$AV_1 = AF_1 \times 0,30 + AD_1 \times 0,70$$

A **AD1** é formada pela entrega dos exercícios (**EX1**) na data prevista e apresentação (**AP1**) de um dos exercícios escolhido pelo professor.
Segue abaixo a expressão para o cálculo da **AD1**.

$$AD_1 = EX1_1 + AP_1 $$

A **EX1** é avaliada mediante a **correção dos exercícios**, sendo a avaliação no intervalo de 0% (não atende a questão), 50% (atende parcialmente) e 100% (atende em sua totalidade).
Por exemplo, se o exercício equivale a 2 pontos e sua correção atente parcialmente a questão, então sua avaliação deste exercício será 1 ponto.

A **AP1** é avaliada mediante aos pré-requisitos de **clareza, organização e domínio do conteúdo**. Portanto, o aluno deve demonstrar um bom entendimento do algoritmo, explicando seus princípios fundamentais, seu propósito e como ele funciona passo a passo. <br>

A avaliação da **AP1** é apenas considerada no intervalo de 0% (não atende os pré-requisitos), 50% (atende parcialmente) e 100% (atende em sua totalidade).
Por exemplo, se na apresentação do exercício, o aluno atenter parcialmente os pré-requisitos, então sua avaliação da apresentação será 5,0.

## Lista de questões

### Questão 1 - Troca dos valores de duas variáveis (1 ponto)

Dadas duas variáveis, $a$ e $b$, implemente e teste um algoritmo para trocar os valores atribuídos a elas.
#### Fluxograma (0.25 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B{{"Digite o valor de A"}}
B --> C[/A/]
C --> D{{"Digite o valor de B"}}
D --> E[/B/]
E --> F(Mem = B)
F --> G(B = A)
G --> H(A = Mem)
H --> I{{A, B}}
I --> J([FIM])
```

#### Pseudocódigo (0.5 ponto)
```
Algoritmo TrocaValores
DECLARE A, B, Mem: float
INICIO
ESCREVA "Digite o valor de A"
LEIA A
ESCREVA "Digite o valor de B"
LEIA B
Mem = B
B = A
A = Mem
ESCREVA A, B
FIM_ALGORITMO
```


#### Teste de mesa (0.25 ponto)

|  A  |  B  |  VALORES  |  INVERSO  |
| --  | --  |  --       |   --      |
|  4  | 8   | 4 , 8     |  8 , 4    |
|  2  | 7   | 2 , 7     |  7 , 2    |
### Questão 2 - Contagem (1 ponto)

Dado um conjunto $n$ de notas de alunos em um exame, implemente e teste um algoritmo para fazer uma contagem $cont$ do número de alunos que foram aprovados no exame. 
Será considerado aprovado o aluno que tirar $nota$ 50 ou maior (no intervalo de 0 a 100).

#### Fluxograma (0.25 ponto)

```mermaid
flowchart TD
A([INICIO])
A --> C[N_aprov = 0]
C --> D{{Digite a quanidade de notas para avaliar}}
D --> E[/N_notas/]
E --> F{N_notas > 0}
F --FALSE--> G{{Digite uma quantidade válida}}
G --> E
F --TRUE--> H{N_notas = N_ver}
H --TRUE--> I{{A quantidade de notas aprovadas foi N_aprov}}
H --FALSE--> J{{Insira a nota}}
J --> K[/nota/]
K --> L{nota >= 50 e nota <= 100}
L --TRUE--> M[N_aprov =+ 1]
M --> N[ i  =+ 1]
L --FALSE--> N
N --> H
I --> Z([FIM])
```
#### Pseudocódigo (0.5 ponto)
```
Algoritimo aprovação
DECLARE i , N_aprov, N_notas, i: Int
	notas: Float
INICIO
N_aprov = 0 
ESCREVA "Digite a quanidade de notas para avaliar"
LEIA N_notas
ENQUANTO N_notas <= 0 REPITA
	ESCREVA "Digite uma quantidade válida"
	LEIA N_notas
PARA i DE 1 ATÉ N_notas FAÇA [PASSO 1]
	ESCREVA "Insira a nota"
	LEIA nota
	SE nota >= 50 E nota <= 100
		N_aprov =+ 1
	FIM_SE
FIM_PARA
ESCREVA "A quantidade de notas aprovadas foi", N_aprov
FIM_ALGORÍRIMO
```

#### Teste de mesa (0.25 ponto)

|              |  ALUNO 01    |  ALUNO 02    |  ALUNO 03    |  ALUNO 04  |  ALUNO 05     | 
|    --        |  --          |  --          |   --         |   --       |    --         | 
|   NOTAS      | 70           |  60          |   55         |  80        |  10           |
|  SITUAÇÃO    | APROVADO     |  APROVADO    |   APROVADO   |  APROVADO  | REPROVADO     |


### Questão 3 - Soma de um conjunto de números (1 ponto)

Dado um conjunto de $n$ números, implemente e teste um algoritmo para calcular a soma desses números. <br>
Aceite apenas $n$ maior ou igual a zero.

#### Fluxograma (0.25 ponto)

```mermaid
flowchart TD
A([INICIO])
A --> C[soma = 0]
C --> D{{Digite o número de elementos do conjunto que você quer somar}}
D --> E[/num_som/]
E --> F{num_som > 0}
F--FALSE--> G{{Digite uma quantidade válida}}
G --> E
G --TRUE--> H{num_som = num_somados}
H --FALSE--> I{{Digite um número}}
I --> J[/num/]
J --> K[soma = soma + num]
K --> L[num_somados =+ 1]
L --> H
H --TRUE--> M{{A valor da soma total é soma}}
M --> N([FIM])
```

#### Pseudocódigo (0.5 ponto)

```
Algoritmo soma_de_valores
DECLARE num_somados, num_soma: Int
	num, soma: Float
INICIO
soma = 0
ESCREVA "Digite o número de elementos do conjunto que você quer somar"
LEIA num_soma
ENQUANTO num_soma <= 0 FAÇA
	ESCREVA "Digite uma quantidade válida"
	LEIA num_soma
FIM_ENQUANTO
PARA num_somados DE 1 até Num_soma [PASSO 1] FAÇA
	ESCREVA "Digite um número"
	LEIA num
	soma =+ num
FIM_PARA
ESCREVA "O valor da soma total é", soma
FIM_ALGORITMO
```

#### Teste de mesa (0.25 ponto)

| SEQUENCIA DE NÚMEROS  |   VALOR DA SOMA TOTAL  |
|      --               |        --              |
| 2 , 4 , 20 , 49, 39   |        114             |
| 1 , 2 , 3 , 4 , 5 ,6  |        21              |

### Questão 4 - Cálculo de uma série (1 ponto)

Calcular o valor de S, conforme definido pela seguinte série infinita:

$$ S = \frac{1}{2} + \frac{3}{4} + \frac{5}{6} + \frac{7}{8} + \dots $$

#### Fluxograma (0.25 ponto)
```mermaid
flowchart TD
A([INICIO]) --> B[S = 0]
B --> D{{Digite a quantidade de termos da série que voce quer somar}}
D --> E[/Num_termo/]
E --> F{Num_termo > 0}
F --FALSE--> G{{Digite uma quantidade válida}}
G --> E
F --TRUE--> H{Num_termo = termo}
H --FALSE--> I[termo =+ 1]
I --> J["S =+ (2 * termo - 1)/(2 * termo)"]
J --> H
H --TRUE--> K{{"O valor da soma de Num_termos termo(s) da série é S"}}
K --> L([FIM])
```

#### Pseudocódigo (0.5 ponto)
```
Algoritmo soma_da_serie
DECLARE Num_termo, termo: Int
	S: Float
INICIO
S = 0
ESCREVA "Digite a quantidade de termos da série que você quer somar"
LEIA Num_termo // 3 
ENQUANTO Num_termo < 0 FAÇA
	ESCREVA "Digite uma quantidade válida"
	LEIA Num_termo
FIM_ENQUANTO
PARA termo DE 1 ATÉ Num_termo [PASSO 1] FAÇA
	S =+ (2 * termo - 1)/(2 * termo)
FIM_PARA
ESCREVA "O valor da soma de", Num_termo, "termo(s) da série é", S
FIM_ALGORITMO
```

#### Teste de mesa (0.25 ponto)

| nome_coluna1 | nome_coluna2 | nome_coluna3 | nome_coluna4 | nome_coluna5 | 
|      --      |      --      |      --      |      --      |      --      | 
| Adicione     | espaço       | se quiser    |  alinhar     | as barras    |
| verticais,   | mas          | não é        | obrigatório. | Entendido ?  |

### Questão 5 - Cálculo fatorial (2 pontos)

Dado um número $n$, calcular o fatorial de $n$ (escrito como $n!$), onde $n ≥ 0$.

#### Fluxograma (0.5 ponto)

```mermaid
flowchart TD
A([INICIO]) --> B[fato = 1]
B --> R[n_mult = 0]
R-->C{{Digite o numero do fatorial que voce quer calcular}}
C --> D[/n/]
D --> E{n >= 0}
E --FALSE--> F{{Digite um fatorial válido}}
F --> D
E --TRUE--> G{n = n_mult}
G --FALSE--> H[n_mult =+ 1]
H --> I[fato = fato * n_mult]
I --> G
G --TRUE--> Y{{O valor do fatorial de n é fato}}
Y --> Z([FIM]) 
```
#### Pseudocódigo (1.0 ponto)

```
Algoritmo fatorial
DECLARE fato, n_mult, n: Int
INICIO
n_mult = 0
ESCREVA "Digite o numero do fatorial que voce quer calcular"
LEIA n
ENQUANTO n < 0 FAÇA
	ESCREVA "Digite um fatorial válido"
	LEIA n
FIM_ENQUANTO
PARA n_mult DE 1 PARA n [PASSO 1] FAÇA
	n_mult =+ 1
	fato = fato * n_mult
FIM_PARA
ESCREVA "O valor do fatorial de", n, "é", fato 
FIM_ALGORITMO
```

#### Teste de mesa (0.5 ponto)

| NÚMERO!  |  CÁCULO   | VALOR DO FATORIAL |
| --       |  --       |   --              |
| 5!       | 5*4*3*2*1 |  120              |
| 3!       | 3 * 2 * 1 |   6               |

### Questão 6 - Geração da sequência de Fibonacci (2 pontos)

Gerar e imprimir os $n$ primeiros termos da sequência de Fibonacci, onde $n ≥ 1$. <br>
Os primeiros termos são: $0, 1, 1, 2, 3, 5, 8, 13, \dots$ <br>
Cada termo, além dos dois primeiros, é derivado da soma dos seus dois antecessores mais próximos.

#### Fluxograma

```mermaid
flowchart TD
A([INICIO]) --> B{{"Número de termos da série Fibonacci:"}}
B --> C[a = 0]
C --> D[b = 1]
D --> E[[i=1 ATÉ n PASSO 1]]
E --"i > n"--> J([FIM])
E --"i=1,2,...,n"--> F{{a}}
F --> G[termo_atual = a + b]
G --> H[a = b]
H --> I[b = termo_atual]
I --LOOP--> E 
```

#### Pseudocódigo (2 pontos)
 NÃO CONSEGUI FAZER PROFESSOR 
```
Algoritmo GeraFibonacci
INICIO
...
FIM
```
#### Teste de mesa

| it | n  | a  | b  | i  | saída | termo_atual = a + b | a = b | b = termo_atual |
| -- | -- | -- | -- | -- | --    | --                  | --    | --              |
| 1  | 5  | 0  | 1  | 1  | 0     | 0 + 1 = 1           | 1     | 1               |
| 2  | 5  | 1  | 1  | 2  | 1     | 1 + 1 = 2           | 1     | 2               |
| 3  | 5  | 1  | 2  | 3  | 1     | 1 + 2 = 3           | 2     | 3               |
| 4  | 5  | 2  | 3  | 4  | 2     | 2 + 3 = 5           | 3     | 5               |
| 4  | 5  | 3  | 5  | 5  | 3     | 3 + 5 = 8           | 5     | 8               |


### Questão 7 - Inversão dos dígitos de um número inteiro (2 pontos)

Inverter a ordem dos dígitos de um número inteiro positivo.

```mermaid
flowchart TD
A([INICIO]) --> B{{Digite um número inteiro: }}
B --> C[\num\]
C --> D{num >= 0}
D --TRUE--> G[num_inv = 0]
G --> H{num > 0}
H --FALSE--> Z{{"Número invertido:", numero_inv}}
Z --> W([FIM])
H --TRUE--> I[digito = num % 10]
I --> J[num_inv = num_inv * 10 + digito]
J --> K[numero = numero // 10]
K --LOOP--> H
D --FALSE--> E{{O número deve ser positivo!}}
E --> W
```

#### Pseudocódigo (2 pontos)
NAO CONSEGUI FAZER PROFESSOR 
```
Algoritmo InverteInteiro
INICIO
...
FIM
```

#### Teste de mesa

| it | num | num_inv | num > 0 | digito | num = num // 10 | num_inv = (num_inv * 10) + digito | Saída                       |
| -- | --  | --      | --     | --      | --              | --                                | --                          |
|    | -1  | 0       | False  |         |                 |                                   | O número deve ser positivo! |
| 1  | 0   | 0       | False  |         |                 |                                   | Número invertido:: 0        |
| 1  | 42  | 0       | True   | 2       | 4               | 2                                 |                             |
| 2  | 4   | 2       | True   | 4       | 0               | 24                                |                             |
| 3  | 0   | 24      | False  |         |                 |                                   | Número invertido:: 24       |

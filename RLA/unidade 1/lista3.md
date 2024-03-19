# UNIFOR
**Nome**: Cauã Aguiar
**Disciplina**: Raciocínio lógico algorítmico
### Exercício 01 
Atualize o algoritmo para determinar se um número inteiro e positivo é par ou ímpar, usando uma laço condicional para aceitar apenas números maiores ou iguais a zero. 

#### Fluxograma 

#### Pseudocódigo 

#### Teste de mesa 

### Exercicio 02
Faça um algoritmo que exiba na tela uma contagem de 0 até 30, exibindo apenas os múltiplos de 3.
obs;duvida all

#### Fluxograma 
 ```mermaid
flowchart TD
A([INICIO]) --> B[/n, num/]
B --> C[n = 30]
C --> D[num = 1]
D --> E{num <= n}
E --FALSE--> H([FIM])
E --TRUE--> F{{"'Número ', num"}}
F --> G[num =+ 1]
G --> E
```
#### Pseudocódigo 
```
	ALGORITMO contagem_1_a_30
	DECLARE n, num: INTEIRO
	INICIO
	n <- 30
	num <- 1
	ENQUANTO num <= n FAÇA
		ESCREVA “Número ”, num
		num ← num + 1
	FIM_ENQUANTO
	FIM
```

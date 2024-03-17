# UNIFOR 
**Disciplina:** Raciocinio Lógico e Algoritimos
**Orientador**:Prof: Ricardo Carubbi 

## Lista de exercícios 
### Exercício 01
Represente, em fluxograma e pseudocódigo, um algoritmo para calcular a média aritmética entre
duas notas de um aluno e mostrar sua situação, que pode ser aprovado ou reprovado;

#### Fluxograma 
```mermaid
flowchart TD
    A(Início) --> B{{Entrada da primeira nota}}
    B --> C{{Entrada da segunda nota}};
    C --> D[/Calcular a média aritmética/];
    D --> E(Verificar se a média é maior ou igual a 6);
    E --> F(Sim);
    F --> G(Aprovado)
    G --> H(FIM)
    E --> I(Não)
    I --> J(Reprovado)
    J --> H(Fim)
 ```

#### Pseudocódigo

### Exercício 02
Represente, em fluxograma e pseudocódigo, um algoritmo para calcular o novo salário de um
funcionário. Sabe-se que os funcionários que recebem atualmente salário de até R$ 500 terão
aumento de 20%; os demais terão aumento de 10%.

#### Fluxograma

```mermaid
flowchart TD
   
    A(Início) --> B(Entrada do salário atual);
    B --> C(Verificar se o salário atual é menor ou igual a R$ 500);
    C --> D(Sim);
    D --> E(Calcular aumento de 20%);
    E --> F(Calcular novo salário);
    F --> G(Imprimir novo salário);
    G --> H(Fim);
    C --> I(Não);
    I --> J(Calcular aumento de 10%);
    J --> K(Calcular novo salário);
    K --> G;


```
#### Pseudocódigo 



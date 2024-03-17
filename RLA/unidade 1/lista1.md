
###Fluxograma
```mermaid
flowchart TD
    A(Início) --> B(Entrada da primeira nota);
    B --> C(Entrada da segunda nota);
    C --> D(Calcular a média aritmética);
    D --> E(Verificar se a média é maior ou igual a 6);
    E --> F(Sim);
    G --> H(Imprimir "Aprovado");
    I --> J(Fim);
    E --> I(Não);
    I --> J(Imprimir "Reprovado");
    J --> H(Fim);
```

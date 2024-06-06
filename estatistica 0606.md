# Amostragem

## Amostragem aleatória simples

### Exemplo
O teor de nicotina, em mg, de 40 cigarros de certa marca foi registrado como segue:

    0.72, 0.85, 1.09, 1.24, 1.37, 1.40, 1.47, 1.51, 1.58, 1.63, 1.64, 1.64, 1.67, 1.68, 1.69, 1.69, 1.70, 1.74, 1.75, 1.75, 1.79, 1.79, 1.82, 1.85, 1.86, 1.88, 1.90, 1.92, 1.93, 1.97, 2.03, 2.08, 2.09, 2.11, 2.17, 2.28, 2.31, 2.37, 2.46, 2.55


## Amostragem sistemática

    k = N/n,
    onde N = tamanho da população
         n = tamanho da amostra

    x entre 1 e k

### Exemplo

Dada a população do exemplo anterior:
    
    0.72, 0.85, 1.09, 1.24, 1.37, 1.40, 1.47, 1.51, 1.58, 1.63, 1.64, 1.64, 1.67, 1.68, 1.69, 1.69, 1.70, 1.74, 1.75, 1.75, 1.79, 1.79, 1.82, 1.85, 1.86, 1.88, 1.90, 1.92, 1.93, 1.97, 2.03, 2.08, 2.09, 2.11, 2.17, 2.28, 2.31, 2.37, 2.46, 2.55

Retire uma amostra sistemática de tamanho 10.

    k = 40/10
    k = 4

    x = rand() entre 1 e 4
    digamos que rand() sorteou 2

Assim, temos as 10 posições da amostra:

    2º -> 6º -> 10º -> 14º -> 18º -> 22º -> 26º -> 30º -> 34º -> 38º 


## Amostragem estratificada

Quando temos um grupo que possui diferentes estratos, no qual há significativa diferença entre os estratos, mas pouca dentro deles, esse tipo de amostragem é útil. Pensamos em uma pesquisa eleitoral para reitor: há estratos que votam diferentemente em bloco - os docentes, os estudantes e os técnicos.

Tipos:
- AE uniforme
- AE proporcional


### Exemplo
Supondo que a população anterior

    0.72, 0.85, 1.09, 1.24, 1.37, 1.40, 1.47, 1.51, 1.58, 1.63, 1.64, 1.64, 1.67, 1.68, 1.69, 1.69, 1.70, 1.74, 1.75, 1.75, 1.79, 1.79, 1.82, 1.85, 1.86, 1.88, 1.90, 1.92, 1.93, 1.97, 2.03, 2.08, 2.09, 2.11, 2.17, 2.28, 2.31, 2.37, 2.46, 2.55

está dividida em três estratos:

Extratos | nº de elementos
---------|----------------
<= 1.5|7
1.5 até 2.0| 23
2.0 ou mais|10

Retire uma amostra estratificada uniforme e proporcional de tamanho 12:

Extratos    | nº de elementos | AE Uniforme | AE proporcional
------------|-----------------|-------------|----------------
<= 1.5      | 7               | 4           | 2.1 -> 3
1.5 até 2.0 | 23              | 4           | 6.9 -> 7
2.0 ou mais | 10              | 4           | 3
   
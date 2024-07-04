# Distribuição por amostragem

    Com reposição: N^n

    Sem reposição: C de n em N

sendo isso o número de amostras de tamanho “n” que poderão ser extraídas da população de tamanho N;

## Distruibuição amostral da média

## Distruibuição amostral da frequência relativa
### Exemplo

Seja x uma população infinita, p a probabilidade do sucesso e q = (1 - p), ou seja, a probabilidade do insucesso. Sorteando uma amostra aleatória de N elementos dessa população e supondo que tenha ocorrido x vezes o evento sucesso. Então, x, que é a frequência absoluta, é uma variável binomial com média n\*p e variância n\*p\*q.

    mi(f) = mi(x/n) * E(x) = (1/n) * n * p = p
    mi(f) = p


    V(f) = V(x/n) * E(x) = 1/n^2 * n * p * q = pq/n

Assim:

    f ~ N(p, pq/n)

Essa aproximação será válida para

    n * p >= 5
    n * p * q >= 5

    ou

    p -> 0.5
    n > 30

## Distrubuição amostral da variância

A estatística S^2 = sum(i = 1 até n, (xi - x̄)^2/n-1), por usar x̄ (amostral), no lugar de mi (populacional) tem um grau de liberdade a menos, ou seja, tem *n - 1* graus de liberdade. 

Isso porque o cálculo dessa estatística pressupõe que já se tenha calculado x̄ anteriormente. E, para tal, já usamos uma vez todos os valores da amostra. os quais estariam sendo usados pela segunda vez para calcular S^2. 

Então, ao usar novamente os valores da amostra para calcular S^2, dados quaisquer *n - 1* valores da amostra, o valor restante estará perfeitamente determinado (pelo fato de já conhecermos sua média x̄), não sendo, portanto, livre.


# Capítulo 7: Estimação de parâmetros

Queremos conhecer a população e seus parâmetros. Mas não vamos ter acesso aos dados da população como um todo. Faremos então uma amostragem e obteremo esses parâmetros para a amostra. Agora, a partir de uma inferência, buscamos encontrar os parâmetros para a população.

## Intervalo de confiança

### IC para média populacional

    P(x̄ - e0 <= mi <= x̄ + eo) = 1 - alpha

Caso 1: A variância populacional sigma^2 é conhecida

    e0 = Z(alpha/2) * sigma / sqrt(n) (ou se n >= 30)

    z é a normal

Caso 2: A variância populacional sigma^2 é desconhecida

    e0 = t v, alpha/2 * S/sqrt(n)

    t é a t de student

    onde v = n - 1


### Exemplo

A distribuição dos diâmetros dos parafusos produzidos por uma certa máquina é normal, com desvio-padrão igual a *0.17mm*. Uma amostra de seis parafusos retirada ao acaso da produção apresentou os seguintes diâmetros em mm:

    25.4, 25.2, 25.6, 25.3, 25.0, 25.4

Construa um IC de 95% para o diâmetro médio da produção da produção máquina.

    sigma = 0.17
    x̄ = 25.32
    n = 6

    z (5%/2) = 1.96

    e0 = z(alpha/2) * sigma/sqrt(n) = 1.96 * 0.17/sqrt(6) = aprox 0.14

    P (25.132 - 0.14 <= mi <= 25.46 + 0.14)
    P (25.18 <= mi <= 25.46) = 95% de probabilidade da média real cair dentro desse intervalo.



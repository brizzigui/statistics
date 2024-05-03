# Estatística 24/04

## Distribuição de Poisson

    (e^-lambda * lambda^k) / k!
    sendo E(x) = lambda; V(x) = lambda
    (a esperança)
    

### Exemplo

> Numa estrada há dois acidentes para cada 100 km. Qual a probabilidade de que em:

a) Em 100 km, não ocorram acidentes?
    
    P(x=0) = P(x=k)

    (e^-2 * 2^0) / 0! = 0,1353

b) Em 250 km, ocorram pelo menos 3 acidentes 

    P(x >= 3) = 1 - P(x < 3)

    1 - (P(x=0) + P(x=1) + P(x=2))
    1 - ((e^-5 * 5^0)/0! + (e^-5 * 5^1)/1! + (e^-5 * 5^2)/2!)
    1 - 18,5*e^-1 = 0,8753

    = 0,8753

c) Em 300 km, ocorram 5 acidentes

    P(x = 5) = P(x = k)

    lambda para 300 km = 6
    
    (e^-6 * 6^5)/5! = 0,1606


### Exemplo 2
> 2% dos refrigeadores produzidos por uma empresa são defeituosos. Se um comprador comprar 1000 refrigeradores, qual a chance de que nenhum seja defeituoso?

    P(x=0)

    lambda para 1000 = 20


    (e^-20 * 20^0)/0! = 2,06 * 10^-9


## Distribuição Geométrica

    P(x=k) = p*(1-p)^(k-1)

### Exemplo

> A probabilidade de se encontrar aberto o sinal de trânsito numa esquina é 0,2. Qual a probabilidade de que seja necessário passar pelo local 5 vezes para encontrar o sinal aberto pela primeira vez?

P(x=5) = 0,2 * 0,8^4 = 0,0819 = 8,19%


## Distribuição Hipergeométrica

    P(x=k) = Comb(r, k) * Comb(N - r, n - k) / Comb(N, n)

    em que:
            N = população de elementos
            n = amostra de elementos
            r = nº de elementos com a condição observada
            k = o que queremos

### Exemplo

> Pequenos motores são guardados em caixas de 50 unidades. Um inspetor de qualidade examina cada caixa antes da posterior remessa testando 5 motores. Se nenhum motor for defeituoso, a caixa é aceita. Se pelo menos um motor for defeituoso, todos os motores, todos os motores são testados. Supondo que há 6 motores defeituosos numa caixa, qual a probabilidade de de que seja necessário examinar todos os motores dessa caixa.

    P(x>=1) = 1 - P(x = 0) 
    
    = 1 - Comb(6, 0) * Comb(50 - 6, 5 - 0) / Comb(50, 5)
    = 1 - 0.5126 = 0.4874



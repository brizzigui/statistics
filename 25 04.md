# Distribuição normal

### Exemplo

Uma fábrica de carros sabe que os motores de sua fabricação tem duração normal de média de 150000km e desvio padrão de 5000km.
Qual a probablidade de que um carro escolhido ao acaso dos fabricados por essa firma tenha um motor que dure:

    sabe-se:

    X: km de duração dos motores
    X~N(150000, (5000)^2)
    mi = 150000; sigma = 5000
    
    Z = (x-mi)/sigma
    sendo x o que nós queremos
    mi, a média
    e sigma, o desvio padrão

a) menos de 170000km

    Z = (170000 - 150000)/5000 = 4
    pela tabela 0.4999
    P(x<170000) = P(z<4) = 0.5 + 0.4999

b) entre 140000km e 165000km

    Z = (140000 - 150000)/5000 = -2
    Z = (165000 - 150000)/5000 = 3

    P(140000<x<165000) = P(-2<z<3) = 0.4772 + 0.4987 = 0.9759

c) menos de 145000km
    
    Z = (145000 - 150000)/5000 = -1
    P(x<145000) = P(z<-1) = 0.5 - 0.3413 = 0.1587
    

d) mais de 160000km

    Z = (160000 - 150000)/5000 = 2
    P(x>160000) = P(z>2) = 0.5 - P(z<2) = 0.5 - 0.4772 = 0.0228

e) entre 160000km e 170000km

    Z = (160000 - 150000)/5000 = 2
    Z = (170000 - 150000)/5000 = 4

    P(160000<x<170000) = P(2<z<4) = 0.4999 - 0.4772 = 0.0227

f) se a fábrica substitue o motor que apresenta por ação inferior à garantia, qual deve ser essa garantia para que a porcentagem de motores substituídos seja inferior a 0,2%

    P(x) < 0.002
    0.5 - P(Z) < 0.002
    0.5 - 0.498 < 0.002

    aprox. Z = - 2.88
    - 2.88 = (x - 150000)/5000
    x = 135600 km
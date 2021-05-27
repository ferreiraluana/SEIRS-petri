# SEIRS-petri
Projeto final de Redes de Petri - Modelo epidemiológico compartimental SEIRS
Professor Leandro Dias
Luana Júlia Nunes Ferreira

# Modelo SEIRS

Esse modelo epidemiológico estuda o comportamento da infecção viral causada pelo coronavírus em uma população baseado no modelo SEIR. A adaptação feita foi a adição de uma imunidade temporária ao invés de uma imunidade permanente. Sendo assim, os indivíduos ficam suscetíveis a reinfecção após algum tempo. Esse modelo não considera possíveis mutações do vírus.

* Susceptible -> Exposed -> Infected -> Recovered -> Susceptible
* ds/dt = mi - beta(t)*S*I - mi*S
* dE/dt = beta(t)*S*I - (mi+alpha)*E
* dI/dt = alpha*E - (mi+gamma)*I
* dR/dt = gamma*I - mi*R
* S(t) = S(0)*exp(-R0*(R(t)-R(0))/N)
* R0 = beta0*alpha/((mi+alpha)(mi+gamma))


### Parâmetros do modelo

O modelo foi implementado em Python e encontra-se disponível [aqui](https://github.com/ferreiraluana/SEIRS-petri/blob/main/seirs.ipynb) 

* S(0) é a população inicial suscetível ao vírus.
No código: S0 = 1000000 (1 milhão de pessoas)
* N0 é o número de reprodução básico, ou seja, quantas pessoas serão infectadas a partir de cada indivíduo infeccioso.
* Neste modelo, o número de reprodução básico adotado foi R0 = 2.1
* mi é a taxa de mortalidade. Vamos considerar que a taxa de mortalidade é igual a taxa de natalidade neste modelo, mi = 0.0001422
* N é a constância da população, N = 2200000;
* período latente médio para a doença: alpha = 14 dias
* período infeccioso médio: gamma = 14 dias

### Resultados da simulação das equações diferenciais

[Indivíduos Suscetíveis](https://github.com/ferreiraluana/SEIRS-petri/blob/main/s.pdf)

[Indivíduos expostos](https://github.com/ferreiraluana/SEIRS-petri/blob/main/e.pdf)

[Indivíduos infecciosos](https://github.com/ferreiraluana/SEIRS-petri/blob/main/i.pdf)

[Indivíduos recuperados](https://github.com/ferreiraluana/SEIRS-petri/blob/main/r.pdf)

### Relatório com detalhes da simulação:

//todo


# sscalc

## Sobre
Implementação OpenCPU da "Sample Size Calculator" que está em: https://wnarifin.github.io/ssc_web.html

Esta implementação é feita para as calculadoras de tamanho de amostra para Modelagem de Equações Estruturais utilizando RMSEA e CFI.

Como essas calculadoras requerem a implementação precisa do algoritmo de Ding para calcular a distribuição qui-quadrado não central (e então o parâmetro de não centralidade ncp para um determinado grau de liberdade usando o algoritmo de Kim), elas dependem da função `qchisq()` em R. A implementação em Javascript do algoritmo de Ding não consegue lidar com grandes graus de liberdade (conceito utilizado para descrever a quantidade de valores independentes que podem variar em uma análise).

É usado OpenCPU como uma alternativa ao 'Shiny', que o programador/autor considera bastante lento para carregar.

As funções disponíveis podem ser encontradas em `R/ss_sem_fun.R`, e os exemplos em `long_example/ss_sem_examples.R`. 

## Referências
Referências:
1. Brown, T. A. (2015). Confirmatory factor analysis for applied research.  New York: The Guilford Press.
2. Ding, C. G. (1992). Algorithm AS 275: computing the non-central χ 2 distribution function. Journal of the Royal Statistical Society. Series C (Applied Statistics), 41(2), 478-482.
3. Kim, K. H. (2005) The Relation Among Fit Indexes, Power, and Sample Size in Structural Equation Modeling. Structural Equation Modeling: A Multidisciplinary Journal, 12(3), 368-390. DOI: 10.1207/s15328007sem1203_2

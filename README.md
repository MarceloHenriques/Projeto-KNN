![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)

# Projeto KNN - Classificação de Perfil de Investidores
Este projeto foi desenvolvido como parte do curso de Engenharia de Dados da ADA Tech em parceria com o Santander Coders. O objetivo é implementar o algoritmo K-Nearest Neighbors (KNN) do zero, utilizando apenas as ferramentas e técnicas de Python aprendidas até o momento, sem a utilização de bibliotecas externas como NumPy ou Math.

## Descrição do Problema
O desafio consiste em classificar clientes de uma empresa de investimentos de acordo com o seu perfil de investidor: Conservador, Moderado ou Agressivo. A classificação é feita com base nos valores da carteira de investimento de cada cliente. Para isso, usamos o algoritmo KNN para prever o perfil de investidores ainda não classificados.

Os dados possuem o seguinte formato:
- CPF: Identificação única do cliente.
- Perfil do Investidor: Conservador, Moderado ou Agressivo (string).
- Carteira de Investimento: Uma tupla com os valores investidos em diferentes produtos (ex: ações, renda fixa, fundos).

## Algoritmo KNN
O KNN é um algoritmo supervisionado de Machine Learning que pode ser utilizado tanto para problemas de classificação quanto de regressão. Abaixo estão os passos do algoritmo implementado:

1 - Escolher um valor para K: Quantidade de vizinhos mais próximos a serem considerados.
2 - Calcular a distância entre o ponto a ser classificado e os demais pontos do conjunto de dados. No nosso caso, utilizamos a distância Euclidiana.
3 - Identificar os K vizinhos mais próximos.
4 - Classificar o ponto de interesse: Se for classificação, utilizamos a moda das classes dos vizinhos; se for regressão, usamos a média dos valores.

## Métodos Utilizados
- distancia_euclidiana(p1, p2): Calcula a distância Euclidiana entre dois pontos.
- vizinhos(data, no_class): Retorna os K vizinhos mais próximos de um ponto a ser classificado com base nas distâncias calculadas.
- classificar(vizinhos): Atribui uma classe ao ponto com base na classe mais frequente entre os vizinhos mais próximos (moda).

## Detalhes da Implementação
- Input do Usuário: O número de vizinhos (K) é definido pelo usuário.
- Distância Euclidiana: Implementada manualmente para calcular a distância entre as carteiras de investimento dos clientes.
- Ordenação de Vizinhos: Utiliza o método .sort() com uma função chave para ordenar as distâncias de forma crescente.
- Classificação Final: Atribuímos o perfil com maior frequência entre os vizinhos mais próximos.

## Regras do Projeto
- Não foi permitido o uso de bibliotecas externas como NumPy ou Math.
- Apenas as técnicas e ferramentas ensinadas no curso foram utilizadas.
- O modelo não foi otimizado, o foco é a construção do algoritmo KNN do zero.

## Conclusão
Este projeto ilustra como é possível implementar o algoritmo KNN de forma didática, sem depender de bibliotecas externas, proporcionando uma melhor compreensão do funcionamento do algoritmo e da importância de técnicas como o cálculo de distância e a ordenação.




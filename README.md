# Projeto Final - Trabalho Nuvem - Pós Cesar School Engenharia de dados 2022.2

## Jammesson Cabral

| **Tipo de Projeto**                                                 | **Ferramental**               | **Linguagem**        |  **Data Entrega** |
| ----------------------------                                        | ----------------------        | -------------        | ------------- |
| Trabalho final cadeira de cloud aws pós cesar school de Imagens<br> | Google Colab                  | Python With Pandas   | 21/05/2023    |



# Documentação código Colab
| **id**  | **Pergunta** |
| ------  | -----------  |
| 1.1.    | Quantos filmes estão disponíveis no dataset?  |
| 1.2.	  | Qual é o nome dos 5 filmes com melhor média de avaliação? |
| 1.3.	  | Quais os 9 anos com menos lançamentos de filmes?  |
| 1.4.	  | Quantos filmes que possuem avaliação maior ou igual a 4.7, considerando apenas os filmes avaliados na última data de avaliação do dataset?  |
| 1.5.	  | Dos filmes encontrados na questão anterior, quais são os 10 filmes com as piores notas ?  |
| 1.6.	  | Quais os id's dos 5 customers que mais avaliaram filmes e quantas avaliações cada um fez?   |


## 1.1.	Quantos filmes estão disponíveis no dataset?
| **Função Utilizda** | **Link Documentação** | **Explicação de uso na atividade**|
| -----               | -----                 | ------ |
| value_counts()      | [pandas.Series.value_counts](https://pandas.pydata.org/docs/reference/api/pandas.Series.value_counts.html). | Essa função tem como objetivo contar os valores contidos em uma Data Series ou seja uma coluna especifica, como a coluna Movie_Id é uma primary_key ou seja um valor unico para cada filme, então podemos contar a quantidade de valores nessa coluna e retornar |
| sum()               | [pandas.DataFrame.sum](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.sum.html)  | Essa função soma todos os valores, então, na primeira função contamos a quantidade de Movie_ID, e somamos com a função sum() para retornar um valor total.|


## 1.2.	Qual é o nome dos 5 filmes com melhor média de avaliação?
| **Função Utilizda** | **Link Documentação** | **Explicação de uso na atividade**|
| -----               | -----                 | ------ |
| Groupby()           | [pandas.DataFrame.groupby](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.groupby.html)  | A função group By do pandas ele agrupa os valores por grupo ou categoria de valores, retornando o count, uma média, uma agregação. Para nossa finalidade utilizamos para tirar a média dos Rantings|


## 1.3.	Quais os 9 anos com menos lançamentos de filmes?
| **Função Utilizda** | **Link Documentação** | **Explicação de uso na atividade**|
| -----               | -----                 | ------ |
| Value_counts()      | [pandas.Series.value_counts](https://pandas.pydata.org/docs/reference/api/pandas.Series.value_counts.html). | Contamos a quantidade de filmes com a coluna ano e retornamos o as ultimas linhas do DataFrame  |
| tail()              | [pandas.DataFrame.tail](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.tail.html)  | Retorna as ultimas linhas do dataFrame, utilizamos para retornar as ultimas 9 linhas do DF  |

## 1.4.	Quantos filmes que possuem avaliação maior ou igual a 4.7, considerando apenas os filmes avaliados na última data de avaliação do dataset?
| **Função Utilizda** | **Link Documentação** | **Explicação de uso na atividade**|
| -----               | -----                 | ------ |
| max()               | [pandas.Series.max](https://pandas.pydata.org/docs/reference/api/pandas.Series.max.html#pandas.Series.max)  | Essa função retorna o valor maximo de um DataFrame ou Data Series, o problema solicita as notas da última data de avaliação do dataset, então usamos a função max() para retornar a ultima data de avaliação do dataset.  |
| loc()               | [pandas.DataFrame.loc](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.loc.html)  | A função loc do DataFrame faz um filtro em cima das condições colocada dentro da função, como a condição para a nossa resposta é que a avaliação seja na ultima data do dataframe pegamos esses valor com a max(), e depois definimos a segunda condição como os ratings => (Igual ou Maior) que 4,7. |
| unique()            | [pandas.unique](https://pandas.pydata.org/docs/reference/api/pandas.unique.html)  | A função unique(), retorna os valores unicos de cada coluna, então utilizamos para retorna apenas a quantidade de filmes e ter a quantidade de filmes que passaram na nossa condição do loc().  |

## 1.5.	Dos filmes encontrados na questão anterior, quais são os 10 filmes com as piores notas ?
| **Função Utilizda** | **Link Documentação** | **Explicação de uso na atividade**|
| -----               | -----                 | ------ |
| min()               | [pandas.DataFrame.min](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.min.html)  | A função min retorna os menores valores de um DataFrame ou DataSeries, utilizamos ele para retornar os filmes com os melhores valores de avaliação. |
| merge()             | [pandas.DataFrame.merge](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.merge.html)  | O merge de Dois Dataframes, faz um JOIN dos mesmos utilizando uma tabela em comum entre os dois, e definimos o tipo da junção que é LEFT ou seja pega os valores do primeiro DF com o do Segundo, Right Pegar os dados em comum do Segundo com o Primeiro, ou Inner que junta os dois dataframes, para o nosso problema precisamos dos 10 filmes que consta no df1, junto com as menores notas contidas no df2.

## 1.6.	Quais os id's dos 5 customers que mais avaliaram filmes e quantas avaliações cada um fez?
| **Função Utilizda** | **Link Documentação** | **Explicação de uso na atividade**|
| -----               | -----                 | ------ |
| value_counts()      | [pandas.Series.value_counts](https://pandas.pydata.org/docs/reference/api/pandas.Series.value_counts.html)  | Utilizamos o Value_counts para contar a quantidade que cada Customers ID votou na tabela de Rating. |
| head()              | [pandas.DataFrame.head](https://pandas.pydata.org/docs/reference/api/pandas.DataFrame.head.html)  | Utilizado para retorna os valores do topo de um data frame, utilizamos o valor head(5), para retornar as 5 linhas do topo do dataframe.

# <p align='center'>🗃 Clustering (agrupamento) usando K-means</p>
  
A ideia do algoritmo K-Means (também chamado de K-Médias) é fornecer uma classificação de informações de acordo com os próprios dados. Esta classificação é baseada em análise e comparações entre os valores numéricos dos dados. Desta maneira, o algoritmo automaticamente vai fornecer uma classificação automática sem a necessidade de nenhuma supervisão humana, ou seja, sem nenhuma pré-classificação existente. Por causa desta característica, o K-Means é considerado como um algoritmo de mineração de dados não supervisionado.

Para entender como o algoritmo funciona, vamos imaginar que temos uma tabela com linhas e colunas que contêm os dados a serem classificados. Nesta tabela, cada coluna é chamada de dimensão e cada linha contém informações para cada dimensão, que também são chamadas de ocorrências ou pontos. Geralmente, trabalha-se com dados contínuos neste algoritmo, mas nada impede que dados discretos sejam utilizados, deste que eles sejam mapeados para valores numéricos correspondentes.
o algoritmo vai analisar todos os dados desta tabela e criar classificações. Isto é, o algoritmo vai indicar uma classe (cluster) e vai dizer quais linhas pertencem a esta classe. O usuário deve fornecer ao algoritmo a quantidade de classes que ele deseja. Este número de classes que deve ser passada para o algoritmo é chamado de k e é daí que vem a primeira letra do algoritmo: K-Means.

Para gerar as classes e classificar as ocorrências, o algoritmo faz uma comparação entre cada valor de cada linha por meio da distância. Geralmente utiliza-se a [distância euclidiana](#euclidiana) para calcular o quão ‘longe’ uma ocorrência está da outra. A maneira de calcular esta distância vai depender da quantidade de atributos da tabela fornecida. Após o cálculo das distâncias o algoritmo calcula [centroides](#centroide) para cada uma das classes. Conforme o algoritmo vai iterando, o valor de cada centroide é refinado pela média dos valores de cada atributo de cada ocorrência que pertence a este centroide. Com isso, o algoritmo gera k centroides e coloca as ocorrências da tabela de acordo com sua distância dos centroides.

<p align='center'>
  <img src='https://raw.githubusercontent.com/JenniferDominique/machine-learning/main/img/Kmeans%20Iteration.gif' width=450>
</p>

Para ler e entender mais sobre o assunto acesse o [link](https://www.devmedia.com.br/data-mining-na-pratica-algoritmo-k-means/4584), acesse também o seguinte [site](https://aprenderdatascience.com/k-means-clustering-agrupamento-k-means/) para se aprofundar mais no assunto.

Veja os notebooks com exemplos de uso do algorítmo:

* ### Vendas BMW

[<img title='Open in GitHub' width=150 src='https://raw.githubusercontent.com/JenniferDominique/machine-learning/main/img/Button-Open_in_GitHub.png'>](https://github.com/JenniferDominique/machine-learning/blob/main/clustering/vendas_BMW.ipynb)
[<img title="Open in Colab" width=150 src="https://raw.githubusercontent.com/JenniferDominique/machine-learning/main/img/Button-Open_in_Colab.png">](https://colab.research.google.com/drive/199ooIDvkottBvOqTlSt8zlNqG5lL4o3X?usp=sharing)

* ### Carros

[<img title='Open in GitHub' width=150 src='https://raw.githubusercontent.com/JenniferDominique/machine-learning/main/img/Button-Open_in_GitHub.png'>](https://github.com/JenniferDominique/machine-learning/blob/main/clustering/cars.ipynb)
[<img title="Open in Colab" width=150 src="https://raw.githubusercontent.com/JenniferDominique/machine-learning/main/img/Button-Open_in_Colab.png">](https://colab.research.google.com/drive/1mXFBASbqyP1Wi-OjtKMqBCL964fQaN65?usp=sharing)


---

<div id='euclidiana'/>

>### 📖 Distância euclidiana
>A medida da distância euclidiana é baseada na distância entre dois vetores representados no espaço 2-dimensional. 
>Ela calcula a diferença entre dois pontos projetados em um plano. Seu cálculo é baseado no teorema de pitágoras.
>
>Acesse o [link](http://www.augustobaffa.pro.br/wiki/Dist%C3%A2ncia_Euclidiana) para mais informações.

<div id='centroide'/>
         
>### 📖 Centroide
>É o ponto em que as coordenadas são as médias das coordenadas dos pontos que formam uma figura geométrica; baricentro, centro geométrico.
>
>Para ler mais acesse o [link](https://educalingo.com/pt/dic-pt/centroide).

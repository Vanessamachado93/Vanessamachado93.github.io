---
title: Pandas - Curso de Python
tags: [Python, Estudos, Tecnologia]
style: border
color: primary
description: 
O Pandas é uma biblioteca Python usada para análise e manipulação de dados. Ele oferece estruturas de dados flexíveis, como Series e DataFrame, e possui recursos para leitura, escrita, limpeza e exploração de conjuntos de dados. Com o Pandas, você pode filtrar, classificar, agrupar e combinar dados de forma eficiente. É uma ferramenta essencial para cientistas de dados, analistas e desenvolvedores que trabalham com análise de dados em Python.
---

# Visualização no pandas
[Documentação do Pandas](https://pandas.pydata.org/docs/index.html)
  
## Análise de csv de uma rede de loja e suas 

Métodos para analisar nossas tabelas (dataframes), usando plot de gráfico padrões do pandas, mas no projeto de DataScience veremos outras mais bonitas e também muito práticas.

  OBS: O pandas usa o matplotlib (que vimos na seção de "módulos e bibliotecas") para plotar gráficos.<br>
  Se quiser personalizar mais do que o padrão do pandas, importe o matplotlib e use os métodos do matplotlib.
  
- Preparando as bases de dados.
- Lembrando que a base de dados usadas estava na mesma pasta do arquivo pandas.


![](https://i.imgur.com/24ZolwM.png)

 ```
import pandas as pd

#importando os arquivos

vendas_df = pd.read_csv(r'Contoso - Vendas - 2017.csv', sep=';')

produtos_df = pd.read_csv(r'Contoso - Cadastro Produtos.csv', sep=';')

lojas_df = pd.read_csv(r'Contoso - Lojas.csv', sep=';')

clientes_df = pd.read_csv(r'Contoso - Clientes.csv', sep=';')

  

#limpando apenas as colunas que queremos

clientes_df = clientes_df[['ID Cliente', 'E-mail']]

produtos_df = produtos_df[['ID Produto', 'Nome do Produto']]

lojas_df = lojas_df[['ID Loja', 'Nome da Loja']]

  

#mesclando e renomeando os dataframes

vendas_df = vendas_df.merge(produtos_df, on='ID Produto')

vendas_df = vendas_df.merge(lojas_df, on='ID Loja')

vendas_df = vendas_df.merge(clientes_df, on='ID Cliente').rename(columns={'E-mail': 'E-mail do Cliente'})

display(vendas_df)
 ```
 ![](https://i.imgur.com/S4L17E7.png)



<!-- ![Tabela](https://i.imgur.com/K4mUMSY.png) -->

### Qual cliente que comprou mais vezes?

- Usamos o método .value_counts() para contar quantas vezes cada valor do Dataframe aparece
- Usamos o método .plot() para exibir um gráfico

 ```
frequencia_clientes = vendas_df['E-mail do Cliente'].value_counts()

display(frequencia_clientes)

frequencia_clientes[:5].plot(figsize=(15,5))
 ```
![](https://i.imgur.com/X2GLOtU.png)

### Qual a Loja que mais vendeu?

- Usaremos o .groupby para agrupar o nosso dataframe, de acordo com o que queremos (somando as quantidades de vendas, por exemplo)

 ```
vendas_lojas = vendas_df.groupby('Nome da Loja').sum()

vendas_lojas = vendas_lojas[['Quantidade Vendida']]

display(vendas_lojas)

 ```
 ![](https://i.imgur.com/RaWprSu.png)
 ```
 #pegando o maior valor e se índice

maior_valor = vendas_lojas['Quantidade Vendida'].max()

melhor_valor = vendas_lojas['Quantidade Vendida'].idxmax()

print(melhor_valor, maior_valor)

Loja Contoso Catalog Valor em R$ 1029117

 ```

![](https://i.imgur.com/z9vtGmm.png)
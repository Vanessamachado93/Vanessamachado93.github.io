---
title: Métodos Úteis em dicionários - Curso de Python
tags: [Python, Estudos, Tecnologia]
style: border
color: primary
description: Dicionário é uma estrutura de dados poderosa e flexível usada para armazenar pares de chave-valor.
---

[Link do Colab Notebook com arquivo completo](https://colab.research.google.com/github/Vanessamachado93/Python-Impressionador-Hashtag/blob/main/Dicionario_05.ipynb)

<a href="https://imgur.com/ZgHmTFp"><img src="https://i.imgur.com/ZgHmTFp.png" title="source: imgur.com" /></a>

A principal utilidade dos dicionários em Python é permitir a recuperação rápida de um valor (valor associado a uma chave) com base em uma chave única. Aqui estão algumas das principais finalidades e benefícios dos dicionários em Python:

### Recuperação eficiente de valores:<br> 
Em vez de percorrer todos os elementos da estrutura de dados para encontrar um valor, os dicionários utilizam uma função de hash para mapear chaves aos seus valores, tornando a recuperação dos valores muito rápida, mesmo para grandes quantidades de dados.

### Associação de informações: <br>
Os dicionários permitem associar informações relacionadas por meio das chaves e valores. Por exemplo, você pode usar um dicionário para associar o nome de uma pessoa ao seu número de telefone, nome de usuário a senha, etc.

### Armazenamento de configurações: <br>
Os dicionários são úteis para armazenar configurações de aplicativos ou opções de preferência em Python, pois permitem que você acesse essas configurações facilmente através das chaves correspondentes.

### Contagem de ocorrências: <br> 
Ao usar dicionários em Python, você pode contar a frequência de ocorrência de elementos em uma lista ou sequência, usando os elementos como chaves e a contagem como valores.

### Chaves não duplicadas:<br>

As chaves em um dicionário são únicas, o que significa que você pode usar um dicionário para garantir que não haja duplicação de elementos-chave.

### Flexibilidade: <br>
 Os dicionários podem armazenar qualquer tipo de dado em suas chaves e valores, tornando-os bastante versáteis em termos de estrutura de dados.



```Python
 # Criando um dicionário de contatos
contatos = {
    'João': '111-1111',
    'Maria': '222-2222',
    'Pedro': '333-3333'
}

# Acessando um valor através de uma chave
print(contatos['João'])  # Saída: '111-1111'

# Adicionando um novo contato
contatos['Ana'] = '444-4444'

# Verificando se uma chave existe no dicionário
if 'Maria' in contatos:
    print("Maria está na lista de contatos.")

# Iterando pelos pares chave-valor
for nome, telefone in contatos.items():
    print(f"{nome}: {telefone}")

# Saída:
# João: 111-1111
# Maria: 222-2222
# Pedro: 333-3333
# Ana: 444-4444
```
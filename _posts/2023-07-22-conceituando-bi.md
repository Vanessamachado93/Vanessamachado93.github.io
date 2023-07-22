---
title: Conceituando Business Intelligence - Curso da FIAP/SP
tags: [PowerBI, Estudos]
style: border
color: primary
description: Business Intelligence como um termo guarda-chuva para descrever um conjunto de conceitos e métodos para melhoar a tomada das decisões de negócio, usando sistemas de suporte sabeados em fatos.
---

# Conceituando Business Intelligence
### Sistemas com o objetivo de fornecer aos gerentes importantes relatótios periódivos estruturados.


A IBM define Business Intelligence (BI) em um dos seus redbooks como a coleta e a análise das grandes quantidades de dados para obter informações que orientem decisões de negócio estratégicas e táticas, para melhorar o desempenho de
uma empresa no mercado.

Segundo a IBM, os dados podem estar relacionados a todas as facetas do negócio, como transações e distribuição demografia dos clientes, informações financeiras da empresa, processos de fabricação, gerenciamento de inventário, tendências da indústria, transações de fornecedores e perfis dos concorrentes. Os dados de Business Intelligence são coletados de fontes internas, como sistemas de transação, processos de fabricação, registros dos clientes, bem como de fontes
externas, como consultoria e estudos da indústria, a mídia impressa e internet.

## O Conjunto que forma o BI

 O BI é um termo abrangente formado por um conjunto de itens que, juntos, permitem o acesso e a análise das informações para melhorar e otimizar decisões e desempenho.
Vamos entender BI através dos principais itens que o compõem.

<a href="https://imgur.com/zIVXh9W"><img src="https://i.imgur.com/zIVXh9W.png" title="source: imgur.com" /></a>

## Dados do BI 

### Fontes OLTP 
 Processamento das transações on-line (OLTP) descreve a forma como os
dados são processados por um sistema informatizado. Sistemas OLTP armazenam seus dados de forma normalizada e, geralmente, processam enormes quantidades de operações CRUD realizadas pelo usuário final. Não foram criados para o BI, nesse contexto, são importantes fontes dos dados que serão utilizados pelo BI. Podemos citar como exemplo de BI uma solução para apoio a tomada de
decisões que segmenta o mercado, define perfis dos clientes, analisa resultados de campanhas, analisa rentabilidade e risco das iniciativas do negócio. Sendo assim, podemos citar como fontes de tal solução as bases de pacotes ERP, CRM, CMS,
SCM, planilhas, arquivos, sistemas departamentais e desenvolvidos sobre medida.

 ### Fontes Externas

Dados externos são dados que não podem ser encontrados nos sistemas
OLTP, mas são necessários e importantes para melhorar a qualidade das informações geradas pelo BI. Exemplos, pesquisas sobre o mercado, informações sobre ações na bolsa,
informações vindas do cadastro positivo etc. Todos seriam relevantes e
complementares ao exemplo de solução de BI descrito em Fontes OLTP.

### Staging Area (SA)

A Staging Area é uma área de trabalho que recebe os dados das Fontes
Internas e Externas. Os Modelos de dados contidos em uma SA não precisam ser modelados seguindo uma técnica específica. Os dados são armazenados muito próximo ao seu formato original, pois não serão utilizados para consulta e análises,
mas sim como área de cópia, limpeza e transformações feitas pelo ETL.

###  Operational Data Store (ODS)

Os bancos de dados operacionais são bancos de dados normalizados, desenvolvidos em algumas soluções de BI, para atender necessidades analíticas sobre processos específicos em uma empresa. Um Operacional Data Store possibilita o armazenamento dos dados atuais, ou
quase atuais, para suporte as decisões operacionais do dia a dia, através de consultas que retornam uma visão corporativa dos dados em nível detalhado. É orientado ao assunto, é integrado, porém é volátil, ou seja, permite atualizações. Seus dados
provêm das fontes citadas acima


### Data Warehouse (DW)

Inmon, considerado o pai do Data Warehouse, define DW como um conjunto
de dados de apoio às decisões gerenciais, integrado, não volátil, variável em relação ao tempo e baseado em assuntos.

• Integrado – Os dados são coletados a partir de uma variedade de fontes e fundidos em um todo coerente. <br>
• Não volátil – Nenhum dado pode ser alterado ou excluído no DW. Qualquer consulta a um dado relativo a um período de tempo sempre produzirá o mesmo resultado; podemos complementar que nenhum dado será excluído enquanto não se tornar obsoleto para o negócio. Em soluções de BI específicas para alguns tipos de negócio, isso pode ocorrer.<br>
• Variável em relação ao tempo – Todos os dados no data warehouse são identificados com um período de tempo particular. O DW é focado na manutenção do histórico.<br>
• Orientado ao assunto – Possui dados que fornecem informações sobre um assunto específico em vez de sobre as operações em curso de uma empresa. Segundo Kimball, “Ao processo de preparar os dados de um sistema de informação operacional de forma a se ter uma fonte de informações que possam dar suporte à tomada de decisões deu-se o nome de Data Warehousing”.

### Data Marts (DM)

São subconjuntos dos dados corporativos, geralmente focados em assuntos especiais e de valor para um departamento da corporação, unidade corporativa ou conjunto de usuários. Um data mart é definido pelo escopo funcional que atende e não pelo seu tamanho. Geralmente considerado como subconjunto de um Data Warehouse.<br>
Podemos dizer que Data Mart evoluiu a partir dos conceitos do Data Warehousing. 
Como a construção de um Data Warehouse pode levar muito tempo, uma vez que lida com informações para toda a corporação, um Data Mart pode ser considerado como um pequeno DW construído para satisfazer as necessidades de um departamento unidade ou conjunto de usuários.<br>
Esse assunto é abordado na construção de um DW, pelas metodologias Top-Dow (Inmon) e Bottom-Up (Kimball). Kimball defende que um DW seja construído a partir do desenvolvimento de DMs, ou seja, construa um Data Mart departamental e integre-o aos demais, quando estiver pronto.
Inmon defende a construção do DW de uma única vez, gerando Data Marts posteriormente. Face ao tempo de construção muito menor e o retorno de investimento mais rápido, a proposta de Kimball é a mais aceita no mercado atualmente.

### Processos do BI
 Agora que conhecemos o papel das Fontes de Dados, da SA, do ODS, do DW e do DM em uma típica solução BI, precisamos entender como as coisas acontecem. Quais são as típicas necessidades que uma solução de BI atende? Como as informações saem das fontes e chegam ao DW e ao DM? Como essas estruturas são mantidas e administradas?<br>
Enfim, como dados brutos se transformam em informações relevantes, para a
tomada de decisões?<br>
A imagem abaixo apresenta, em alto nível, como os processos acontecem.

<a href="https://imgur.com/Zri8ewg"><img src="https://i.imgur.com/Zri8ewg.png" title="source: imgur.com" /></a>

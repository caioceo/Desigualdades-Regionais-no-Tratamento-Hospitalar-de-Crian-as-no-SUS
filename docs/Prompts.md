## Registro dos principais prompts utilizados para otimização do processo ETL.

# Extração de dados

Prompt: “Vou enviar uma tabela em formato de imagem e preciso que você faça a soma de linhas, formando assim, novas faixas etárias. Elas têm de 0 a 9 anos, 10 a 19 anos e 20 a 59 anos 60 anos ou mais.”

Resultado: A inteligência artificial apenas fez a soma e escreveu a tabela, porém, não foi capaz de gerar o arquivo .xlsx ou .csv, que seria necessário para os próximos processos.

Com isso, recorri ao Grok e apresentei a necessidade de transformar a tabela em formato de texto em um formato de ficheiro. Também o orientei a utilizar python para isso.

Prompt: Preciso de um código python que transforme essa tabela de formato texto para o formato .csv.
Resultado: Código funcional em python & faixa_etaria_X_atributos.csv

Após isso, repeti o processo para formar a base responsável pela distribuição regional

# Dicionário de Dados

Explicamos ao ChatGPT o que queríamos dizer com o termo dicionário de dados e deixamos claro quais os tipos de dados e seus exemplos.

Prompt: “Chat, vou precisar que você faça um dicionário de dados, uma tabela copiável para o formato .md, que informe os seguintes atributos: Atributo, Tipo de dado, Descrição; Primeiramente preciso que confira se o conteúdo abaixo está correto: Atributo referente às colunas. Tipos de dado: Qualitativo ordinal (existe hierarquia entre os dados, ex: inicio/meio/fim) Qualitativo nominal (não existe hierarquia entre os dados, ex: estados/municípios) Qualitativo binário (quando existir duas variáveis, com pesos iguais, ex: homem/mulher e sim/nao) Quantitativa discreta (contagem de números inteiros onde existe zero absoluto, ex: contagens) Quantitativa contínua (pode assumir qualquer valor dentro de um intervalo, sem limites definidos, ex: peso, altura, temperatura) Descrição: Pequeno texto que fale o que o atributo representa.”

Manualmente ajustamos o número de óbitos que foi incoerente e implantamos a taxa de internação nas demais bases.

Resultado: Código funcional em python & distribuição_regional _X_publico_alvo


# Análise Exploratória de Dados

Anexando a tabela unificada e compartilhando a pergunta orientada a dados ao Perplexity AI, obtivemos uma análise estatística e exploratória de dados, permitindo interpretação visual por gráficos didáticos que ilustram bem a situação em discussão. Compartilhamos ideias e possíveis relações dos atributos com a LLM e também tivemos que corrigir o código diversas vezes.

Prompt :“Faça um código python que gere gráficos e análises estatísticas úteis para o trabalho.

Contextualização:

Como a eficácia da assistência hospitalar prestada durante a internação pública de crianças de 0 a 9 anos varia entre as regiões do Brasil, considerando indicadores de morbidade hospitalar como número de internações, óbitos, tempo de permanência e valores gastos por internação?

Hipóteses a serem investigadas

Regiões com menor investimento médio por internação apresentam maior taxa de mortalidade hospitalar infantil.

O tempo médio de permanência hospitalar pode ser maior em regiões com menor estrutura de saúde, refletindo ineficiência no tratamento.

Há maior número de internações por causas evitáveis em regiões com menor cobertura de atenção primária à saúde.

Objetivo

Analisar a desigualdade regional nos indicadores de saúde hospitalar para o público infantil (0 a 9 anos), com base nos dados da Tabela de Morbidade Hospitalar do SUS (DataSUS), visando identificar disparidades na qualidade e eficácia do atendimento hospitalar entre as diferentes regiões do Brasil.”


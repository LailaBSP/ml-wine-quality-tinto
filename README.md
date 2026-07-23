# Projeto Fundamentos da Inteligência Artificial – Análise Exploratória e Classificação da Qualidade de Vinhos

O objetivo do projeto é analisar um conjunto de dados de vinhos tintos e brancos, explorando suas características físico-químicas e a relação dessas variáveis com a qualidade do vinho. Para isso, são realizadas etapas de pré-processamento dos dados, incluindo remoção de duplicatas, tratamento de outliers, padronização das variáveis e criação de faixas de qualidade ("ruim", "médio" e "bom"). Ao final, os dados são preparados para o treinamento de modelos de aprendizado de máquina capazes de classificar a qualidade dos vinhos com base em suas características.

Integrantes:
- Laila Beatriz de Souza Pereira
- Lavínia Almeida Cerqueira dos Santos
- Carolina Aragão Céu Melo

Fonte dos dados:

UCI Machine Learning Repository — Wine Quality Dataset
Link: https://archive.ics.uci.edu/dataset/186/wine+quality

Os dados são carregados diretamente da fonte pública dentro do próprio notebook, sem necessidade de download manual ou upload de arquivos locais.

Tipo da tarefa:

Classificação multiclasse supervisionada, pois o objetivo é prever a faixa de qualidade do vinho (ruim, médio ou bom) a partir de suas características.

Organização dos arquivos:
- README.md — este arquivo
- Projeto_FIA_Qualidade_de_vinhos.ipynb — notebook principal com todo o desenvolvimento: carregamento dos dados, análise exploratória, pré-processamento, modelagem e avaliação
  
Instruções para abrir o notebook no Colab:
1. Acesse o arquivo .ipynb neste repositório.
2. Clique no botão "Open in Colab" (ou copie o link do notebook e abra diretamente em colab.research.google.com).
3. Execute as células em ordem, de cima para baixo (ou use Ambiente de execução → Executar tudo).
4. Os dados são carregados automaticamente de fonte pública, não sendo necessário nenhum download prévio ou upload de arquivos.

Modelos Utilizados e Resultados:

Para prever a faixa de qualidade do vinho (ruim, médio, bom) com base em suas características físico-químicas, foram treinados e avaliados os seguintes modelos:

  Modelos Treinados

- Baseline: DummyClassifier (estratégia "most frequent"), usado como referência mínima de comparação.
- SGDClassifier (com class_weight='balanced'), modelo linear treinado sobre os dados padronizados.
- RandomForestClassifier (com class_weight='balanced'), modelo de ensemble baseado em árvores de decisão.

Ambos os modelos treinados usaram balanceamento de classe (class_weight='balanced') para lidar com o desbalanceamento identificado entre as faixas de qualidade, ao invés de reamostragem dos dados.

Principais Resultados

| Modelo                              | Acurácia | Precisão (Weighted) | Revocação (Weighted) | F1-Score (Weighted) |
|--------------------------------------|----------|----------------------|------------------------|------------------------|
| Baseline (Dummy - Most Frequent)     | 0,4370   | 0,1910               | 0,4370                 | 0,2658                 |
| SGDClassifier                        | 0,5338   | 0,5658               | 0,5338                 | 0,5098                 |
| RandomForestClassifier               | 0,6259   | 0,6301               | 0,6259                 | 0,6254                 |

- Melhor Modelo: O RandomForestClassifier apresentou o melhor desempenho geral, superando tanto o baseline quanto o SGDClassifier em todas as métricas avaliadas.
- O baseline (Dummy) confirma que os modelos treinados agregam valor real: o RandomForest teve um ganho de quase 19 pontos percentuais de acurácia em relação a apenas prever sempre a classe mais frequente.
- O SGDClassifier, por ser um modelo linear, teve desempenho intermediário — indicando que a relação entre as características físico-químicas e a qualidade do vinho não é puramente linear.

Divisão das contribuições:
Todas as três integrantes contribuiram e ajudaram no desenvolvimentos das partes uma das outras, mas as divisões bases são as seguintes:
- Lavínia Almeida Cerqueira dos Santos foi responsável pela parte inicial do projeto, incluindo dados e exploração.
- Laila Beatriz de Souza Pereira foi responsável pelo pré-processamento e separação dos dados e organização básica do readme.
- Carolina Aragão Céu Melo foi responsável pela modelagem e avaliação e discursão. 

Link do vídeo:

https://youtu.be/lvMMCBTVoY8?is=Wv9bIXFrjgy27qdF

Declaração do uso de inteligência artificial:
- Ferramentas usadas: Claude e chatgpt

- Finalidade: Foi usado para facilitar o entendimento da lógica de programação em algumas etapas e explicações lógicas da atividade.

- Parte do trabalho que foi utilizada: Auxílio na estruturação de sintaxe e refatoração de código Python.
Sugestão de boas práticas para plotagem de gráficos e organização visual na análise exploratória.
Geração dos textos explicativos e da documentação do projeto, visando otimizar o tempo de produção do material final.

- Forma de verificação do conteúdo produzido: Apesar do uso de IA para a redação dos textos e suporte técnico, todo o desenvolvimento passou por uma verificação técnica rigorosa por parte dos autores, entre elas:

Validação dos Dados: Todos os dados carregados, pré-processados e transformados foram conferidos manualmente para garantir que não houvesse vazamento de dados (data leakage) ou distorções causadas por automações.
Entendimento Preditivo: As métricas geradas pelos modelos (como F1-Score, Matriz de Confusão e Relatório de Classificação) foram analisadas criticamente em função do problema de negócio, assegurando que o comportamento dos algoritmos fizesse sentido do ponto de vista estatístico e químico.
Garantia de Autoria: O fluxo lógico, a tomada de decisão sobre quais algoritmos utilizar e a interpretação dos resultados finais foram conduzidos integralmente pelo grupo, garantindo domínio completo sobre a solução apresentada.

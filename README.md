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

Para prever a qualidade do vinho tinto com base em suas características físico-químicas, foram treinados e avaliados diversos algoritmos de Machine Learning, divididos entre modelos baseline e ensembles:

  Modelos Treinados

- Baseline: Regressão Logística (Logistic Regression) e Árvore de Decisão (Decision Tree).
- Ensembles Avançados: Random Forest, Gradient Boosting e XGBoost.
- Otimização: Uso de GridSearchCV / RandomizedSearchCV combinado com validação cruzada para o ajuste de hiperparâmetros.


Principais Resultados

- Melhor Modelo: Os algoritmos baseados em Ensemble (especialmente Random Forest e XGBoost) apresentaram o melhor desempenho geral, superando os modelos baseline em acurácia e F1-Score.
- Métricas Principais:
  - Aumento significativo no F1-Score e na AUC-ROC após o balanceamento dos dados e sintonia de hiperparâmetros.
  - Alta capacidade de discriminação entre vinhos de qualidade superior e comum/inferior.
- Variáveis mais Importantes (Feature Importance):
  1. Teor Alcoólico (Alcohol): Principal preditor positivo de qualidade.
  2. Sulfatos (Sulfates): Forte correlação positiva com melhores avaliações.
  3. Acidez Volátil (Volatile Acidity): Principal indicador negativo (quanto maior a acidez volátil, menor a nota atribuída).


Divisão das contribuições:
Todas as três integrantes contribuiram e ajudaram no desenvolvimentos das partes uma das outras, mas as divisões bases são as seguintes:
- Lavínia Almeida Cerqueira dos Santos foi responsável pela parte inicial do projeto, incluindo dados e exploração.
- Laila Beatriz de Souza Pereira foi responsável pelo pré-processamento e separação dos dados e organização básica do readme.
- Carolina Aragão Céu Melo foi responsável pela modelagem e avaliação e discursão. 

Link do vídeo:


Declaração do uso de inteligência artificial:
- Ferramentas usadas: Claude e chatgpt

- Finalidade: Foi usado para facilitar o entendimento da lógica de programação em algumas etapas e explicações lógicas da atividade.

- Parte do trabalho que foi utilizada: Auxílio na estruturação de sintaxe e refatoração de código Python.
Sugestão de boas práticas para plotagem de gráficos e organização visual na análise exploratória.
Geração dos textos explicativos e da documentação do projeto, visando otimizar o tempo de produção do material final.

- Forma de verificação do conteúdo produzido: Apesar do uso de IA para a redação dos textos e suporte técnico, todo o desenvolvimento passou por uma verificação técnica rigorosa por parte dos autores, entre elas:

Validação dos Dados: Todos os dados carregados, pré-processados e transformados foram conferidos manualmente para garantir que não houvesse vazamento de dados (data leakage) ou distorções causadas por automações.
Entendimento Preditivo: As métricas geradas pelos modelos (como F1-Score, Matriz de Confusão e Feature Importance) foram analisadas criticamente em função do problema de negócio, assegurando que o comportamento dos algoritmos fizesse sentido do ponto de vista estatístico e químico.
Garantia de Autoria: O fluxo lógico, a tomada de decisão sobre quais algoritmos utilizar e a interpretação dos resultados finais foram conduzidos integralmente pelo grupo, garantindo domínio completo sobre a solução apresentada.

Trabalho avaliativo da disciplina de Machine learning, criado por Iago Cavalcante, Gustavo Kuster e Lucas Machado Lavinas com tema: Previsao de necessidade de reposicao de estoque com machine learning.

Projeto de Machine Learning: Previsão de Reposição de Estoque em Sistema ERP

Este projeto tem como objetivo aplicar técnicas de Machine Learning para prever se determinado item de estoque precisa ou não ser reposto.

O problema será tratado como uma tarefa de classificação binária, em que:

- 1 = o produto precisa de reposição;
- 0 = o produto não precisa de reposição.

A base de dados simula informações típicas de um sistema ERP, como estoque atual, estoque mínimo, consumo médio mensal, prazo de reposição, categoria do produto, fornecedor e valor unitário.

Serão treinados e comparados dois modelos:

- Regressão Logística;
- Random Forest.


titulo do projeto: Previsão de Necessidade de Reposição de Estoque com Machine Learning


O presente projeto tem como objetivo aplicar técnicas de Machine Learning para prever a necessidade de reposição de produtos em um ambiente semelhante ao de um sistema ERP. A proposta foi escolhida por sua relação direta com processos administrativos, logísticos e gerenciais, especialmente aqueles ligados ao controle de estoque, almoxarifado, compras e planejamento de materiais.

A escolha desse tema permite aproximar o conteúdo técnico da disciplina de uma situação prática já conhecida no ambiente organizacional: a tomada de decisão sobre quando comprar, repor ou manter determinado item em estoque. Dessa forma, o projeto busca demonstrar como modelos preditivos podem apoiar a gestão de materiais, reduzindo riscos de falta de produtos, excesso de estoque e compras emergenciais.

2. Descrição do Problema
Em organizações que utilizam sistemas ERP, o controle de estoque é uma atividade essencial para garantir o funcionamento contínuo dos setores administrativos, operacionais e produtivos. Quando determinado item atinge níveis baixos de estoque, a ausência de reposição adequada pode gerar atrasos, paralisações ou necessidade de aquisições emergenciais. Por outro lado, compras feitas sem critério podem gerar excesso de materiais armazenados, desperdício financeiro e ocupação desnecessária de espaço físico.

Diante desse contexto, o problema definido para este projeto consiste em prever se determinado produto precisa ou não ser reposto, considerando variáveis como estoque atual, estoque mínimo, consumo médio mensal, prazo de reposição, categoria do produto, fornecedor e valor unitário.

Assim, o problema foi tratado como uma tarefa de classificação binária, na qual o modelo deverá indicar uma entre duas possibilidades:

1: o produto precisa ser reposto;
0: o produto não precisa ser reposto.
A aplicação de Machine Learning nesse contexto permite automatizar uma análise que, em muitos sistemas de gestão, ainda depende exclusivamente de regras fixas ou da avaliação manual do responsável pelo estoque. A proposta, portanto, é utilizar dados históricos ou simulados para treinar modelos capazes de identificar padrões associados à necessidade de reposição.

3. Objetivo do Projeto
O objetivo geral deste projeto é desenvolver e avaliar modelos de Machine Learning capazes de prever a necessidade de reposição de itens de estoque em um sistema tipo ERP.

Como objetivos específicos, definem-se:

organizar uma base de dados relacionada ao controle de estoque;
realizar o pré-processamento dos dados;
transformar variáveis categóricas em formato compatível com algoritmos de Machine Learning;
dividir os dados em conjuntos de treino e teste;
treinar pelo menos dois modelos de classificação;
comparar o desempenho dos modelos por meio de métricas apropriadas;
apresentar os resultados obtidos em tabelas e gráficos;
indicar possíveis melhorias para versões futuras do projeto.
4. Descrição dos Dados
A base de dados utilizada no projeto representa informações típicas de um controle de estoque em sistema ERP. O conjunto de dados pode ser construído pelo próprio grupo, de forma simulada, ou adaptado a partir de bases públicas disponíveis em plataformas como Kaggle, UCI Repository ou Google Dataset Search.

Para este projeto, recomenda-se a criação de uma base simulada em formato CSV, contendo aproximadamente entre 300 e 1.000 registros. Essa quantidade é suficiente para fins didáticos e permite executar todas as etapas exigidas no trabalho sem tornar o projeto excessivamente complexo.

A base poderá conter as seguintes variáveis:

Variável	Tipo	Descrição
produto	Categórica	Nome ou identificação do item
categoria	Categórica	Grupo ao qual o produto pertence
estoque_atual	Numérica	Quantidade disponível em estoque
estoque_minimo	Numérica	Quantidade mínima desejada para o item
consumo_medio_mensal	Numérica	Média de consumo mensal do produto
prazo_reposicao_dias	Numérica	Tempo médio para reposição pelo fornecedor
fornecedor	Categórica	Identificação do fornecedor principal
valor_unitario	Numérica	Valor médio unitário do produto
precisa_repor	Binária	Variável-alvo: 1 para repor, 0 para não repor
A variável mais importante do projeto é precisa_repor, pois ela representa aquilo que o modelo deverá aprender a prever. As demais variáveis serão utilizadas como atributos de entrada para auxiliar o algoritmo na identificação de padrões.

5. Metodologia Utilizada
A metodologia do projeto foi organizada em etapas sequenciais, contemplando desde a definição do problema até a comparação dos modelos treinados. Inicialmente, foi realizada a definição do problema de negócio, relacionando a necessidade de reposição de estoque com o uso de Machine Learning.

Em seguida, foi elaborada ou selecionada a base de dados. Após a obtenção dos dados, foram executadas etapas de pré-processamento, incluindo verificação de valores ausentes, tratamento de inconsistências, codificação de variáveis categóricas e separação entre variáveis independentes e variável-alvo.

Após o pré-processamento, os dados foram divididos em conjunto de treino e conjunto de teste. O conjunto de treino foi utilizado para ajustar os modelos, enquanto o conjunto de teste foi reservado para avaliar o desempenho final dos algoritmos. Essa separação é importante para verificar se o modelo consegue generalizar o aprendizado para dados que não foram utilizados durante o treinamento.

Foram selecionados dois algoritmos de Machine Learning para comparação:

Regressão Logística;
Random Forest.
A escolha desses modelos se justifica pela diferença entre suas abordagens. A Regressão Logística é um modelo simples, interpretável e adequado para problemas de classificação binária. Já o Random Forest é um modelo baseado em árvores de decisão, capaz de capturar relações mais complexas entre as variáveis.

6. Pré-processamento dos Dados
O pré-processamento é uma etapa essencial em projetos de Machine Learning, pois os algoritmos dependem de dados organizados e compatíveis com seus métodos de cálculo. No presente projeto, essa etapa envolveu a preparação da base de dados para que ela pudesse ser utilizada pelos modelos de classificação.

Primeiramente, foi realizada a leitura do arquivo CSV por meio da biblioteca pandas. Em seguida, foram verificadas possíveis inconsistências, como valores ausentes, dados duplicados ou registros incompatíveis. Caso fossem encontrados valores nulos, o grupo poderia optar pela remoção das linhas incompletas ou pelo preenchimento com média, mediana ou moda, dependendo do tipo da variável.

As variáveis categóricas, como categoria e fornecedor, precisaram ser transformadas em variáveis numéricas. Isso é necessário porque os algoritmos de Machine Learning utilizados não trabalham diretamente com textos. Para essa conversão, foi utilizado o processo de codificação conhecido como One-Hot Encoding, que cria novas colunas binárias para representar cada categoria.

A variável produto pode ser removida da modelagem caso funcione apenas como identificador, pois nomes de produtos não costumam contribuir diretamente para a previsão. Por outro lado, variáveis como estoque atual, estoque mínimo, consumo médio mensal e prazo de reposição são relevantes porque possuem relação direta com a necessidade de reposição.

Após a preparação dos dados, foi realizada a separação entre:

X: conjunto de variáveis explicativas;
y: variável-alvo, representada por precisa_repor.
7. Modelos Testados
Para atender ao objetivo do projeto, foram selecionados dois modelos de classificação: Regressão Logística e Random Forest.

7.1 Regressão Logística
A Regressão Logística é um algoritmo de classificação utilizado para prever a probabilidade de ocorrência de determinado evento. Neste projeto, ela foi aplicada para prever a probabilidade de um produto precisar ou não de reposição.

Esse modelo foi escolhido por ser simples, rápido e adequado para problemas binários. Além disso, sua interpretação é mais direta, o que facilita a explicação dos resultados em uma apresentação acadêmica.

No contexto do projeto, a Regressão Logística analisa variáveis como estoque atual, estoque mínimo, consumo médio e prazo de reposição para estimar se o item pertence à classe “precisa repor” ou “não precisa repor”.

7.2 Random Forest
O Random Forest é um algoritmo baseado em múltiplas árvores de decisão. Ele combina o resultado de várias árvores para produzir uma classificação final mais robusta. Esse modelo é geralmente eficiente em bases tabulares e pode apresentar bom desempenho mesmo quando existem relações não lineares entre as variáveis.

No presente projeto, o Random Forest foi utilizado para comparar seu desempenho com o da Regressão Logística. A expectativa é que esse modelo tenha melhor capacidade de identificar padrões mais complexos, por exemplo, situações em que o produto ainda possui estoque disponível, mas precisa ser reposto devido ao alto consumo médio e ao longo prazo de entrega do fornecedor.

8. Métricas de Avaliação
Como o projeto trata de um problema de classificação binária, foram utilizadas métricas adequadas para avaliar o desempenho dos modelos. As principais métricas consideradas foram:

8.1 Acurácia
A acurácia mede o percentual total de previsões corretas realizadas pelo modelo. Ela indica, de forma geral, quantas classificações foram acertadas em relação ao total de registros avaliados.

Apesar de ser uma métrica simples, a acurácia deve ser interpretada com cuidado, especialmente quando há desequilíbrio entre as classes. Por exemplo, se a maior parte dos produtos não precisa de reposição, um modelo pode apresentar alta acurácia apenas por prever a classe majoritária.

8.2 Precisão
A precisão mede, entre todos os produtos classificados como “precisa repor”, quantos realmente precisavam de reposição. Essa métrica é importante porque evita que o modelo recomende compras desnecessárias.

Em um contexto de ERP, baixa precisão poderia gerar excesso de compras, aumento de estoque parado e uso inadequado de recursos financeiros.

8.3 Recall
O recall mede, entre todos os produtos que realmente precisavam de reposição, quantos foram corretamente identificados pelo modelo. Essa métrica é especialmente relevante para evitar falta de produtos.

No controle de estoque, um baixo recall pode representar risco operacional, pois o sistema deixaria de alertar sobre itens que deveriam ser repostos.

8.4 F1-Score
O F1-Score é uma métrica que combina precisão e recall. Ela é útil quando se deseja equilíbrio entre evitar compras desnecessárias e evitar falta de produtos.

No presente projeto, o F1-Score foi utilizado como uma das principais métricas para comparar os modelos, pois o problema de reposição de estoque exige equilíbrio entre eficiência financeira e continuidade operacional.

8.5 Matriz de Confusão
A matriz de confusão permite visualizar os acertos e erros do modelo. Ela mostra quantos produtos foram corretamente classificados como “precisa repor” ou “não precisa repor”, além de indicar os falsos positivos e falsos negativos.

No contexto deste projeto:

Verdadeiro positivo: o produto precisava ser reposto e o modelo indicou reposição;
Verdadeiro negativo: o produto não precisava ser reposto e o modelo não indicou reposição;
Falso positivo: o modelo indicou reposição, mas o produto não precisava ser reposto;
Falso negativo: o produto precisava ser reposto, mas o modelo não indicou reposição.
Os falsos negativos são particularmente relevantes, pois podem gerar falta de produtos no estoque.

9. Resultados e Discussão
Após o treinamento dos modelos, os resultados foram comparados utilizando o conjunto de teste. A comparação permitiu verificar qual algoritmo apresentou melhor desempenho na previsão da necessidade de reposição.

A tabela abaixo apresenta um modelo de estrutura para exposição dos resultados:

Modelo	Acurácia	Precisão	Recall	F1-Score
Regressão Logística	[preencher]	[preencher]	[preencher]	[preencher]
Random Forest	[preencher]	[preencher]	[preencher]	[preencher]
A partir dos resultados obtidos, será possível discutir qual modelo apresentou melhor desempenho geral. Caso o Random Forest apresente valores superiores, isso poderá ser explicado pela sua capacidade de trabalhar melhor com relações complexas entre as variáveis. Por exemplo, a necessidade de reposição pode não depender apenas do estoque atual, mas da combinação entre estoque, consumo médio e prazo de entrega.

Caso a Regressão Logística apresente desempenho semelhante, isso indicará que o problema pode ser resolvido satisfatoriamente com um modelo mais simples e interpretável. Nesse caso, a escolha do modelo poderá considerar não apenas a métrica final, mas também a facilidade de explicação e implementação em um ambiente corporativo.

Além da tabela de métricas, recomenda-se apresentar pelo menos um gráfico comparativo, como um gráfico de barras com os valores de acurácia, precisão, recall e F1-Score de cada modelo.

10. Conclusões e Possíveis Melhorias
O projeto demonstrou a aplicação de técnicas de Machine Learning em um problema típico de gestão de estoque, comum em sistemas ERP. A proposta permitiu compreender como dados administrativos podem ser utilizados para apoiar decisões operacionais, como a reposição de produtos.

A partir da comparação entre Regressão Logística e Random Forest, foi possível avaliar qual modelo apresentou melhor desempenho para a classificação dos produtos. O modelo com maior F1-Score pode ser considerado o mais equilibrado, pois essa métrica considera simultaneamente precisão e recall.

De modo geral, o uso de Machine Learning nesse contexto pode contribuir para melhorar a gestão de estoque, reduzir compras emergenciais, evitar falta de produtos e apoiar o planejamento de materiais. Embora o projeto tenha caráter acadêmico e utilize uma base simplificada, ele representa uma aplicação prática de ciência de dados em processos administrativos.

Como possíveis melhorias futuras, podem ser indicadas:

utilização de uma base real extraída de um sistema ERP;
aumento da quantidade de registros analisados;
inclusão de variáveis como sazonalidade, histórico de compras e tempo real de entrega;
comparação com outros modelos, como SVM, KNN ou XGBoost;
uso de validação cruzada e Grid Search para ajuste mais refinado dos hiperparâmetros;
criação de um painel visual para acompanhamento dos itens com maior risco de ruptura;
integração do modelo a um sistema de alerta de reposição.
11. Link do Repositório
O projeto deverá ser disponibilizado em um repositório público, preferencialmente no GitHub ou em um notebook do Google Colab. O repositório deverá conter os arquivos necessários para reprodução dos resultados.

Sugestão de estrutura do repositório:

projeto-ml-estoque/
│
├── dados/
│   └── estoque.csv
│
├── notebooks/
│   └── projeto_ml_estoque.ipynb
│
├── imagens/
│   └── graficos_resultados.png
│
├── README.md
└── apresentacao.pdf
O arquivo README.md deverá apresentar:

título do projeto;
integrantes do grupo;
descrição do problema;
descrição da base de dados;
etapas de pré-processamento;
modelos utilizados;
métricas de avaliação;
principais resultados;
instruções para executar o projeto;
link para o notebook ou código-fonte.
Exemplo de texto para o README:

Este repositório apresenta um projeto de Machine Learning aplicado à previsão de necessidade de reposição de estoque em um sistema tipo ERP. O objetivo é classificar produtos em duas categorias: itens que precisam de reposição e itens que não precisam de reposição. Para isso, foram utilizados dados relacionados a estoque atual, estoque mínimo, consumo médio mensal, prazo de reposição, fornecedor e valor unitário. Foram treinados e comparados os modelos Regressão Logística e Random Forest, utilizando métricas como acurácia, precisão, recall e F1-Score.

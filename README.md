# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Neste documento, descrevemos os procedimentos básicos necessários para demonstrarmos a utilização do SageMaker Canvas com informações simples de estoque tendo como objetivo final a criação de previsões de estoque com base em Machine Learning(ML). Analisando as previsões geradas, podemos obter insights de modo a melhorar a performance do negócio.

## 🚀 Passo a Passo

### 1. Amazon SageMaker

-  O SageMaker Canvas é um recurso do universo Amazon SageMaker sendo necessário criar um domínio para utilizá-lo. Antes de prosseguir com a criação do domínio, certifique que a região configurada no AWS (localizada no canto superior direito) é a mais adequada conforme a sua localização geográfica.
-  No meu caso como estou no Brasil, alterei a região para América do Sul (São Paulo). Com esta alteração, teremos uma melhor performance na criação do domínio e execuções das demais atividades.
-  Utilize a opção quicksetup para criar o seu domínio.
-  Após a criação do domínio, poderemos acessar a feature Canvas

### 1. Selecionar Dataset

-   Navegue até a pasta `datasets` deste repositório. Esta pasta contém os datasets que você poderá escolher para treinar e testar seu modelo de ML. Sinta-se à vontade para gerar/enriquecer seus próprios datasets, quanto mais você se engajar, mais relevante esse projeto será em seu portfólio.
-   Escolha o dataset que você usará para treinar seu modelo de previsão de estoque.
-   Faça o upload do dataset no SageMaker Canvas.

### 2. Construir/Treinar

-   No SageMaker Canvas, importe o dataset que você selecionou.
-   Configure as variáveis de entrada e saída de acordo com os dados.
-   Inicie o treinamento do modelo. Isso pode levar algum tempo, dependendo do tamanho do dataset.

### 3. Analisar

-   Após o treinamento, examine as métricas de performance do modelo.
-   Verifique as principais características que influenciam as previsões.
-   Faça ajustes no modelo se necessário e re-treine até obter um desempenho satisfatório.

### 4. Prever

-   Use o modelo treinado para fazer previsões de estoque.
-   Exporte os resultados e analise as previsões geradas.
-   Documente suas conclusões e qualquer insight obtido a partir das previsões.

## 🤔 Dúvidas?

Esperamos que esta experiência tenha sido enriquecedora e que você tenha aprendido mais sobre Machine Learning aplicado a problemas reais. Se tiver alguma dúvida, não hesite em abrir uma issue neste repositório ou entrar em contato com a equipe da DIO.

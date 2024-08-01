# 📊 Previsão de Estoque Inteligente na AWS com [SageMaker Canvas](https://aws.amazon.com/pt/sagemaker/canvas/)

Neste documento, descrevemos os procedimentos básicos necessários para demonstrarmos a utilização do SageMaker Canvas com informações simples de estoque tendo como objetivo final a criação de previsões de estoque com base em Machine Learning(ML). Analisando as previsões geradas, podemos obter insights de modo a melhorar a performance do negócio.

## 🚀 Passo a Passo

### 1. Amazon SageMaker

-  O SageMaker Canvas é um recurso do universo Amazon SageMaker sendo necessário criar um domínio para utilizá-lo. Antes de prosseguir com a criação do domínio, certifique que a região configurada no AWS (localizada no canto superior direito) é a mais adequada conforme a sua localização geográfica.
-  No meu caso como estou no Brasil, alterei a região para América do Sul (São Paulo). Com esta alteração, teremos uma melhor performance na criação do domínio e execuções das demais atividades.
-  Utilize a opção quicksetup para criar o seu domínio.
-  Após a criação do domínio, poderemos acessar a feature Canvas.
-  Caso não localize a feature Canvas, verifique o idioma e mude para English. A feature Canvas estará na sessão Applications and IDEs. A Amazon utiliza tradução literal e neste caso, aparecerá como TELA, se o idioma estiver como Português. A Amazon deveria incluir a palavra Canvas em um catálogo comercial e implementá-lo de modo a não realizar traduções literais evitando alguns problemas para os usuários de seus serviços.

### 2. Construir/Treinar

-   No SageMaker Canvas, importaremos o dataset escolhido que contém indicador de preço promocional e a quantidade atual no estoque.
-   Após a importação do arquivo e criação do dataset, iniciaremos a construção do modelo.
-   Utilizaremos o tipo Análise preditiva, sendo mais indicado para atingirmos o objetivo final de previsões de reposição do estoque.
-   Configurando as variáveis de entrada e saída de acordo com os dados:
    -  Utilizaremos a coluna QUANTIDADE_ESTOQUE como coluna target, pois o modelo que estamos construindo irá prever valores através desta coluna;
    -  A ferramenta recomenda algumas configurações após a definição da coluna target, identificando a coluna time stamp DATA_EVENTO;
    -  Necessário informarmos a coluna que identifica exclusivamente os itens do nosso conjunto de dados;
    -  Optamos por marcar a opção de avaliar conforme os feriados do Brasil;
    -  De modo a refinar a qualidade dos dados e melhorar a performance do modelo, a ferramenta poderá sugerir ajustes para os dados. Em nosso caso, acatamos as sugestões de inserir preço médio e quantidade igual a zero para os valores faltantes da nossa massa de dados.
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

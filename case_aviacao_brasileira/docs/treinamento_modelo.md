## Treinamento de Modelo de Machine Learning

1-  Configuração do Ambiente
Bibliotecas Importadas:<br />
Manipulação de dados: pandas, numpy.<br />
Visualização de dados: seaborn, matplotlib.pyplot, scikitplot.<br />
Machine Learning (Pré-processamento e métricas): scikit-learn, imblearn, xgboost, shap, hyperopt.<br />
Outras utilidades: pickle, os, re, datetime, pytz.<br />

2 - Preparação dos Dados<br />
Leitura de Dados: O script carrega um conjunto de dados de um arquivo CSV para um DataFrame do pandas.<br />
Seleção das colunas que vão participar do treinamento.<br />

3 - Pré-processamento de Dados<br />
Codificação de Características: Utilização de codificação one-hot para transformar características categóricas.<br />

4 - Modelagem<br />
Modelo Utilizado: XGBoost (Extreme Gradient Boosting).<br />
Ajuste de Hiperparâmetros:<br />
Implementação de uma função para ajuste de hiperparâmetros (hipertunnig) usando validação cruzada (Cross-validation). Vale destacar que o SMOTE foi aplicado dentro de cada segmentação de dados da etapa da validação cruzada. <br />
Técnicas de otimização: hyperopt e skopt.<br />


!!! info "SMOTE (Synthetic Minority Over-sampling Technique)"
    === "Desequilíbrio de Classes"

        No mundo da ciência de dados e aprendizado de máquina, o desequilíbrio de classes em conjuntos de dados é um desafio comum, especialmente em cenários de classificação. O SMOTE (Synthetic Minority Over-sampling Technique) emergiu como uma técnica inovadora para abordar esse problema, ajudando a melhorar a precisão e eficácia dos modelos preditivos.<br />
        
        O desequilíbrio de classes ocorre quando as observações em diferentes classes não estão igualmente representadas. Por exemplo, em um conjunto de dados de detecção de fraude, as transações fraudulentas são muito menos comuns do que as transações legítimas. Esse desequilíbrio pode levar a modelos que favorecem a classe majoritária, resultando em uma identificação inadequada da classe minoritária.<br />

    === "O Que é?"

        SMOTE é uma técnica de processamento de dados usada para equilibrar conjuntos de dados desbalanceados através do aumento do número de exemplos na classe minoritária. Diferentemente do simples oversampling, que apenas replica exemplos existentes, o SMOTE cria exemplos sintéticos.<br />

    === "Como Funciona?"

        O processo do SMOTE envolve a seleção aleatória de um ponto da classe minoritária e a identificação de seus vizinhos mais próximos no conjunto de dados. Em seguida, ele gera novos exemplos sintéticos que são combinações lineares desses pontos e seus vizinhos. Isso ajuda a introduzir mais variedade dentro da classe minoritária, evitando o overfitting comum no oversampling tradicional.<br />

    === "Aplicações"
        SMOTE é particularmente útil em áreas como detecção de fraude, diagnóstico médico, e reconhecimento de padrões, onde a classe de interesse é significativamente menos representada.<br />

    === "Benefícios e Limitações"

        Benefícios: O SMOTE melhora a representação da classe minoritária, contribuindo para modelos mais equilibrados e precisos.<br />
        
        Limitações: Pode gerar exemplos sintéticos que não representam bem a realidade se os dados originais já estiverem muito desequilibrados ou se tiverem muitos outliers.

5 - Avaliação do Modelo<br />
Métricas de Avaliação:<br />
Acurácia, F1-Score, Matriz de Confusão, ROC-AUC, Recall, Precisão, Log Loss, Average Precision Score. Curvas ROC e Precision-Recall.<br />

6 - Salvamento e Carregamento de Modelos<br />
Funções para salvar e carregar modelos usando a biblioteca pickle.<br />
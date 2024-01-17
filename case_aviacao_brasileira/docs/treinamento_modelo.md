## Treinamento de modelo de machine learning

1-  Configuração do ambiente
bibliotecas importadas:<br />
Manipulação de dados: pandas, numpy.<br />
Visualização de dados: seaborn, matplotlib.pyplot, scikitplot.<br />
Machine Learning (Pré-processamento e métricas): scikit-learn, imblearn, xgboost, shap, hyperopt.<br />
Outras utilidades: pickle, os, re, datetime, pytz.<br />

2 - Preparação dos Dados<br />
Leitura de Dados: O script carrega um conjunto de dados de um arquivo CSV para um DataFrame do pandas.<br />
Seleção das colunas que vão participar do treinamento.<br />

3 - Pré-processamento de Dados<br />
Codificação de Características: Utilização de codificação one-hot para transformar características categóricas.<br />

4 - Treinamento<br />
Modelo Utilizado: XGBoost (Extreme Gradient Boosting).<br />
!!! info "Para mais informações sobre o funcionamento XGBoost acesse:"
    - [Understanding XGBoost - A Comprehensive Guide (YouTube Video)- Parte 1](https://www.youtube.com/watch?v=OtD8wVaFm6E)<br />
    - [XGBoost in Python from Start to Finish (YouTube Video) - Parte 2](https://www.youtube.com/watch?v=8b1JEDvenQU)<br />
    - [XGBoost Explained (Kaggle) (YouTube Video) - Parte 3](https://www.youtube.com/watch?v=ZVFeW798-2I)<br />
    - [XGBoost Machine Learning Algorithm Explained (YouTube Video) - Parte 3](https://www.youtube.com/watch?v=oRrKeUCEbq8)<br />
    - [What is XGBoost? - NVIDIA Glossary](https://www.nvidia.com/en-us/glossary/xgboost/#:~:text=What%20is%20XGBoost%3F,%2C%20classification%2C%20and%20ranking%20problems.)<br />
    - [XGBoost - GeeksforGeeks](https://www.geeksforgeeks.org/xgboost/)<br />
    - [An End-to-End Guide to Understand the Math behind XGBoost - Analytics Vidhya](https://www.analyticsvidhya.com/blog/2018/09/an-end-to-end-guide-to-understand-the-math-behind-xgboost/)<br />
    - [XGBoost Documentation](https://xgboost.readthedocs.io/en/stable/tutorials/model.html)<br />


Ajuste de Hiperparâmetros:<br />
Implementação de uma função para ajuste de hiperparâmetros (hipertunnig) usando validação cruzada (Cross-validation). Vale destacar que o SMOTE foi aplicado dentro de cada segmentação de dados da etapa da validação cruzada. <br />
Técnicas de otimização: hyperopt e skopt.<br />
Treinamento do modelo com melhores parâmetros.<br />


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
!!!warning
    É importante destacar que nem todas as métricas empregadas nesta análise são as mais apropriadas para contextos onde a variável dependente é desbalanceada. Estas métricas foram selecionadas principalmente com o objetivo de aprendizado, e cada uma delas merece uma exploração mais detalhada e até postagens separadas.<br />
Métricas de Avaliação:<br />
- Acurácia <br />
- F1-Score <br />
- Matriz de Confusão <br />
- ROC-AUC <br />
- Recall <br />
- Precisão <br />
- Log Loss <br />
- Average Precision Score <br />
- Curva ROC <br />
- Curva Precision-Recall<br />

!!! info "Outras métricas para valiação de modelos de classificação"
    :ballot_box_with_check: &nbsp; **Kappa de Cohen (Cohen's Kappa)**;<br />
    :ballot_box_with_check: &nbsp; **F-Score Balanceado**;<br />
    :ballot_box_with_check: &nbsp; **Matthews Correlation Coefficient (MCC)**;<br />
    :ballot_box_with_check: &nbsp; **Taxa de Falsos Positivos (False Positive Rate)**;<br />
    :ballot_box_with_check: &nbsp; **Taxa de Falsos Negativos (False Negative Rate)**;<br />

    
6 - Salvamento e Carregamento de Modelos<br />
Funções para salvar e carregar modelos usando a biblioteca pickle.<br />
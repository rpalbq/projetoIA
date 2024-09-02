# Descrição da Base de Dados Dry Bean

O Dry Bean Dataset é um conjunto de dados que contém informações sobre diferentes tipos de feijão seco. O objetivo é prever a classe do feijão com base em várias características físicas.

## Estrutura dos Dados
- **Número de Colunas:** 16
- **Número de Linhas:** 13.611
- **Colunas de Atributos:** Características físicas como área, perímetro, compacidade, etc.

### Atributos:
- **Área:** Área total ocupada pelo grão na imagem.
- **Perímetro:** Soma das distâncias dos contornos do grão.
- **Comprimento do Eixo Maior:** Comprimento do eixo mais longo do grão.
- **Comprimento do Eixo Menor:** Comprimento do eixo mais curto.
- **Excentricidade:** Mede a excentricidade da forma do grão.
- **Área Convexa:** Área do menor polígono convexo que engloba o grão.
- **Diâmetro Equivalente:** Diâmetro do círculo com a mesma área do grão.
- **Extensão:** Proporção da área do grão em relação à caixa delimitadora.
- **Solidez:** Razão entre a área do grão e a área do seu contorno convexo.
- **Arredondamento:** Mede o quão circular é o grão.
- **Razão de Aspecto:** Razão entre os comprimentos dos eixos maior e menor.
- **Compacidade:** Razão entre o perímetro ao quadrado e a área.
- **Fator de Forma 1:** Primeira métrica de forma do grão.
- **Fator de Forma 2:** Segunda métrica de forma.
- **Fator de Forma 3:** Terceira métrica de forma.
- **Fator de Forma 4:** Quarta métrica de forma.

### Coluna de Classe:
- **Tipo de Feijão (7 classes possíveis):**
  - Barbunya
  - Bombay
  - Cali
  - Dermosan
  - Horoz
  - Sira
  - Sevrekli

## Análise das Classes:

### Resultado: Distribuição das Classes:
- **Class_1:** 2500
- **Class_2:** 2200
- **Class_3:** 1800
- **Class_4:** 1700
- **Class_5:** 1500
- **Class_6:** 1400
- **Class_7:** 1511

**Conclusão:** Base relativamente equilibrada, todas as classes têm uma quantidade de dados boa para a realização da modelagem.

## Dados Ausentes:

**Conclusão:** Não foram encontrados dados ausentes no conjunto de dados.

## Verificação de Duplicados:

**Conclusão:** Não foram encontradas linhas duplicadas no conjunto de dados.

## Análise Comparativa das Técnicas de Machine Learning: Escolha da Melhor Técnica

Após treinar e avaliar cinco diferentes modelos de Machine Learning utilizando o código fornecido, os resultados indicaram que o **Support Vector Machine (SVM)** foi o modelo mais eficaz para a tarefa de classificação em questão.

### Desempenho do SVM:
- **Acurácia:** O SVM alcançou a maior acurácia no conjunto de teste, com um valor de 93.29%.
- **F1-Score:** O SVM também obteve o maior F1-Score, 93.31%. Este valor reflete o equilíbrio entre precisão e recall, sendo particularmente importante em problemas onde as classes podem ser desbalanceadas.

O SVM se destacou devido à sua capacidade de maximizar a margem de separação entre as diferentes classes, o que é crucial em problemas de classificação com fronteiras complexas. Sua robustez contra o sobreajuste e a eficiência em lidar com dados de alta dimensionalidade o tornaram a melhor escolha para este problema específico.

### Comparação com Outros Modelos:
- **Regressão Logística:**
  - Test Accuracy: 92.29%
  - Test F1-Score: 92.33%

- **K-Nearest Neighbors (KNN):**
  - Test Accuracy: 92.16%
  - Test F1-Score: 92.18%

- **Random Forest:**
  - Test Accuracy: 92.26%
  - Test F1-Score: 92.27%

- **Rede Neural (MLP):**
  - Test Accuracy: 93.27%
  - Test F1-Score: 93.28%

## Conclusão

Com base nos resultados obtidos, o modelo SVM foi o que apresentou a melhor combinação de acurácia e F1-Score no conjunto de teste. Isso faz dele a técnica mais adequada para o problema, garantindo previsões precisas e um bom equilíbrio entre precisão e recall. Embora outros modelos, como a MLP, tenham chegado perto, o SVM se destaca por sua simplicidade, robustez e eficiência, o que justifica sua escolha como a melhor técnica para este caso.

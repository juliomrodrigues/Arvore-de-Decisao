# Classificador por Arvore de Decisão

#### Usando algoritmo de árvore de decisão em uma base de dados real para classificar registros(Base de Dados - Censo de 1994 - EUA).
#### Objetivo: Prever se um americano possui renda anual <= ou > 50 mil dólares por ano.

### Resultados - Validação Cruzada - StratifiedKFold
**Precisão** | **Pré-Processamentos** | **Desvio Padrão**
| :------: | :------: | :------: |
0.8138 | LabelEncoder | 0.0050
**0.8185** | **OneHotEncoder** | **0.0044**
0.8137 | LabelEncoder + StandardScaler | 0.0047
0.8185 | OneHotEncoder + StandardScaler | 0.0046
0.8185 | LabelEnconder + OneHotEncoder + StandardScaler | 0.0046

### Matriz de Confusão(Média de todas as 10 execuções):
### Matriz de Confusão (Média):
x | **0** | **1**
| :------: | :------: | :------: |
0 | **2171.3** | 300.7
1 | 290 | **494.1**

A Matriz na tabela acima é formada pela média de todas as matrizes geradas ao longo de 10 execuções usando pré-processamentos OneHotEncoder.

A diagonal principal (em negrito) destaca os registros classificados corretamente.

### Bibliotecas usadas:
- Pandas
- Sklearn
- Numpy

### Técnicas de Pré-Processamento e Tratamento dos dados usada:
- LabelEnconder;
- OneHotEncoder;
- StandardScaler;

### Ferramentas Usadas:
- Anaconda
- Spyder

### Linguagem:
- Python

#### Fonte da Base de Dados: 
Dua, D. and Graff, C. (2019). UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

#### Como usar:
Basta fazer o download do código fonte e da base de dados. Para executar o código por partes(células) e testar diferentes possibilidades de pré-processamento, recomendo uma IDE como Spyder ou o Jupyter. (Támbem é necessário ter o Python instalado no seu computador)

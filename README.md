# Classificador por Arvore de Decisão

Treinando um modelo de árvore de decisão e aplicando em uma base de dados para classificar registros(Censo de 1994 - EUA).

O objetivo é prever se uma pessoa possui renda anual <= ou > 50 mil dólares por ano.

Percentual Mínimo -> Base Line Classifier = 0.7559 (ZeroR).

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

### Fonte da Base de Dados: 
- Dua, D. and Graff, C. (2019). UCI Machine Learning Repository [http://archive.ics.uci.edu/ml]. Irvine, CA: University of California, School of Information and Computer Science.

### Como usar:
1. Faça o download do classificador já treinado dispoível neste mesmo repositório [aqui](https://github.com/juliomrodrigues/Arvore-de-Decisao/blob/main/classificador_arvore_decisao.sav).
2. Abra o arquivo.py que deseja usar o classificador ou então crie um novo.
3. Execute o código abaixo para fazer a importação:
~~~~python
import pickle
classificador = pickle.load(open('classificador_arvore_decisao.sav', 'rb'))
~~~~~
4. Pronto, agora o classficador está pronto para ser usado.

#### Outros Classificadores:
- [Naive Bayes](https://github.com/juliomrodrigues/Classificador-Naive-Bayes)
- [Random Forest](https://github.com/juliomrodrigues/Random-Forest-Classificador)
- [Regras](https://github.com/juliomrodrigues/Classificador-Regras)
- [KNN](https://github.com/juliomrodrigues/Classificador-KNN)
- [Regressão Logística](https://github.com/juliomrodrigues/Regressao-Logistica-Classificador)
- [SVM](https://github.com/juliomrodrigues/Classificador-SVM)
- [Rede Neural](https://github.com/juliomrodrigues/Classificador-Rede-Neural)

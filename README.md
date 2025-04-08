# 🛳️ Titanic Dataset: Análise e Limpeza de Dados

Análise exploratória e limpeza do famoso dataset do Titanic, com foco na preparação dos dados para análises futuras ou modelagem preditiva.

---

## 📦 Bibliotecas Utilizadas

- `numpy`: operações matemáticas e vetoriais
- `pandas`: manipulação e análise de dados tabulares
- `matplotlib.pyplot`: visualização de dados

---

## 📥 Obtenção dos Dados

Os dados foram baixados diretamente do Google Drive via `gdown`:

```python
!gdown 1qT5OdmoWy1tkIAbvXRx-gjVKA_GUNfO0
```

---

## 📊 Primeira Visão dos Dados

Após carregar o CSV (`titanic_train.csv`), o dataset foi visualizado com `df.head()` e `df.info()` para entender sua estrutura.

---

## 🧹 Limpeza de Dados

### 🔍 Análise de valores nulos

Foram identificadas colunas com dados ausentes, como:

- `Age`: 177 valores nulos
- `Cabin`: 687 valores nulos
- `Embarked`: 2 valores nulos

### 🛠️ Tratamentos aplicados:

- **Coluna `PassengerId`**: removida por não ser útil para análise.
- **Coluna `Age`**: valores nulos preenchidos com a mediana, agrupada por `Pclass` e `Sex`.
- **Coluna `Cabin`**: removida devido à alta quantidade de valores ausentes.
- **Coluna `Embarked`**: linhas com valores nulos removidas (apenas 2 registros).

---

## 📈 Visualizações

### 📌 Idade por classe e sexo
Gráfico de barras com a mediana da idade agrupada por `Pclass` e `Sex`.

### 🔥 Heatmap de Correlação
Análise de correlação entre variáveis numéricas:

- Conversão de `Sex` em valores numéricos (`male` → 0, `female` → 1)
- Colunas não numéricas irrelevantes removidas
- Matriz de correlação visualizada com `imshow()` e anotação dos valores

### 📦 Boxplots

- **Idade (`Age`)**: distribuição da idade dos passageiros
- **Preço do ticket (`Fare`)**: análise da dispersão dos preços

---

## ✅ Resultado Final

Após a limpeza:

- Nenhum valor nulo restante
- Dataset pronto para análises mais aprofundadas ou modelagem preditiva

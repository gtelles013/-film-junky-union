#  IMDB Sentiment Analysis — Classificação de Resenhas de Filmes

##  Visão Geral

Este projeto desenvolve um modelo de **Processamento de Linguagem Natural (NLP)** para classificar automaticamente resenhas de filmes como **positivas** ou **negativas**.

O objetivo é simular uma solução real para a *Film Junky Union*, permitindo a moderação e análise automatizada de conteúdo em larga escala.

---

##  Problema de Negócio

Plataformas com grande volume de conteúdo enfrentam dificuldades para:

* Identificar rapidamente feedback negativo
* Priorizar melhorias com base na opinião dos usuários
* Moderar conteúdo de forma eficiente

 Este projeto resolve esse problema com um classificador de sentimento baseado em Machine Learning.

---

##  Dataset

* Fonte: IMDB Movie Reviews
* Total de registros: ~50.000 resenhas
* Classes:

  * `0` → Negativo
  * `1` → Positivo
* Divisão já definida:

  * Treino (`train`)
  * Teste (`test`)

---

##  Abordagem

###  Pré-processamento

* Normalização de texto (lowercase)
* Remoção de pontuação
* Remoção de stopwords
* Vetorização com **TF-IDF**

###  Modelos Treinados

Foram testados múltiplos algoritmos:

* Regressão Logística
* Gradient Boosting
* (Outros modelos podem ser incluídos conforme evolução)

---

## Avaliação

**Métrica principal:** F1-score

> Ideal para cenários com possível desequilíbrio de classes

| Modelo              | F1-score (Teste) |
| ------------------- | ---------------- |
| Regressão Logística | 0.XX             |
| Gradient Boosting   | 0.XX             |

 **Meta do projeto:** F1 ≥ 0.85

---

##  Testes com Dados Reais

Além da avaliação padrão, os modelos foram testados com **resenhas escritas manualmente**, simulando uso em produção.

Isso permitiu observar:

* Diferenças de generalização
* Sensibilidade a linguagem informal
* Robustez dos modelos

---

##  Principais Insights

* Modelos lineares (como Regressão Logística) performam muito bem em NLP com TF-IDF
* Pré-processamento impacta diretamente na performance
* Pequenas variações no texto podem alterar significativamente a predição
* Há diferenças claras entre performance em teste e uso real

---

##  Stack Tecnológica

* Python
* Pandas & NumPy
* Scikit-learn
* Matplotlib / Seaborn
* NLP (TF-IDF)

---

##  Estrutura do Projeto

```
 imdb-sentiment-analysis
 ┣  notebook.ipynb
 ┣  imdb_reviews.tsv
 ┣  README.md
```

---

##  Como Executar o Projeto

```bash
# Clonar repositório
git clone https://github.com/seu-usuario/imdb-sentiment-analysis.git

# Entrar na pasta
cd imdb-sentiment-analysis

# Instalar dependências
pip install -r requirements.txt

# Executar notebook
jupyter notebook
```

---

##  Melhorias Futuras

* Implementação de modelos baseados em Transformer (ex: BERT)
* Otimização de hiperparâmetros
* Pipeline automatizado de NLP
* Deploy como API (FastAPI ou Flask)
* Interface simples para classificação em tempo real

---

##  Autor

Desenvolvido como projeto de portfólio em Ciência de Dados, com foco em **Machine Learning aplicado a NLP**.

---

##  Destaque

Este projeto demonstra:

* Capacidade de trabalhar com dados reais
* Construção completa de pipeline de ML
* Avaliação crítica de modelos
* Aplicação prática de NLP

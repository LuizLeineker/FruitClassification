# 🍎 Inspeção Visual Automática de Frutas

Projeto desenvolvido para a disciplina de Visão Computacional utilizando o pipeline clássico de inspeção visual automática.

---

# 🧮 Introdução

Este trabalho foi desenvolvido com base nos requisitos definidos na disciplina e utiliza o **Cenário A — Inspeção de frutas em uma central de distribuição**.

O objetivo é automatizar o processo de análise da qualidade de frutas por meio de técnicas clássicas de visão computacional, reduzindo dependência da inspeção manual.

Foi utilizado o dataset **Fruit Quality Detection**, disponível no Kaggle.



Fruit Quality Dataset
https://www.kaggle.com/datasets/sriramr/fruits-fresh-and-rotten-for-classification

---

# 🍌 Problema Proposto

Uma central de distribuição recebe diariamente grandes volumes de frutas e realiza separação manual entre produtos aptos para comercialização e produtos deteriorados.

Neste projeto foi desenvolvido um sistema capaz de identificar automaticamente se uma fruta pertence à classe:

* Fresh (fresca)
* Rotten (podre)

Foram considerados defeitos como:

* manchas escuras na casca;
* deformações geométricas;
* variações de coloração;
* sinais visíveis de deterioração.

---

# 📂 Dataset

O dataset original possui seis classes:

* Fresh Apple
* Fresh Banana
* Fresh Orange
* Rotten Apple
* Rotten Banana
* Rotten Orange

Como o objetivo do projeto é avaliar qualidade da fruta e não identificar o tipo da fruta, as classes foram agrupadas em:

* Fresh
* Rotten

As imagens do dataset não permitem distinguir a categoria intermediária destinada para produção de sucos.

---

# ⚙️ Pipeline Implementado

Imagem RGB
↓
Pré-processamento
↓
Segmentação (HSV + Morphology)
↓
Extração de Features
(Forma + Hu + Cor + GLCM)
↓
Construção da Tabela X + Vetor y
↓
Classificação (Random Forest + SVM)
↓
Avaliação (Accuracy, Precision, Recall, F1-score e Matriz de Confusão)

---

# 📁 Estrutura do Projeto

```plaintext
notebooks/
├── 01_segmentacao.ipynb
├── 02_features.ipynb
├── 03_classificacao.ipynb

outputs/
├── figuras
├── matrizes_confusao
├── tabelas_metricas
├── imagens_de_erros

X.csv
y.csv

README.md
requirements.txt
```

---

# ▶️ Instruções de Execução

### 1. Criar e ativar ambiente virtual

```bash
python -m venv venv
```

Windows:

```bash
venv\Scripts\activate
```

Linux/macOS:

```bash
source venv/bin/activate
```

### 2. Instalar dependências

```bash
pip install -r requirements.txt
```

### 3. Executar os notebooks

```bash
jupyter notebook
```

Executar na ordem:

```plaintext
01_segmentacao.ipynb
02_features.ipynb
03_classificacao.ipynb
```

---

# 👥 Integrantes
Felipe Henrique Ribeiro   
Luiz André Hoffmann Leineker

---


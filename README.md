# applied-computational-intelligence

Homework 2 de Inteligência Computacional Aplicada (ICA), Departamento de
Engenharia de Teleinformática da UFC, disciplina ministrada pela Profa. Michela
Mulas.

Modelos de regressão para a solubilidade em água de 1.267 compostos químicos
(Alternativa 1 do enunciado, dataset `solubility` do pacote
`AppliedPredictiveModeling`): análise exploratória com transformação de
Yeo-Johnson, mínimos quadrados ordinários (OLS), regressão ridge e mínimos
quadrados parciais (PLS) implementados do zero e comparados com o
scikit-learn, validação cruzada implementada do zero, rede neural (MLP) e
comparação estatística entre os modelos.

## Conteúdo do repositório

O repositório do trabalho no GitHub está hospedado no endereço
https://github.com/icaro-a-santana/applied-computational-intelligence-hm2

| Caminho | Descrição |
|---|---|
| `homework2.ipynb` | Notebook com as questões 0 a 4 do enunciado e a comparação entre modelos, já executado |
| `paper/main.pdf` | Relatório final, formato de artigo de conferência IEEE |
| `paper/main.tex` | Fonte LaTeX do relatório |
| `paper/tabelas/` | Fragmentos LaTeX gerados pela última seção do notebook |
| `figuras/` | Figuras referenciadas pelo artigo, geradas pelo notebook |
| `dataset/solubility/` | Conjunto de dados (treino e teste, preditores e desfecho) |
| `requirements.txt` | Dependências Python |
| `USO_DE_IA.md` | Apêndice de uso de ferramentas de IA |
| `TI0175_HW2_assignment.pdf` | Enunciado |

Os arquivos `solTrainXtrans.txt` e `solTestXtrans.txt` são as versões já
transformadas que acompanham o pacote do R; o notebook **não** os usa, a
transformação é refeita do zero a partir de `solTrainX.txt` e `solTestX.txt`.

## Como rodar

### Notebook no Google Colab

Clique no botão *Open in Colab* no topo do notebook, ou abra
https://colab.research.google.com/github/icaro-a-santana/applied-computational-intelligence-hm2/blob/main/homework2.ipynb

A primeira célula detecta o Colab e clona este repositório para ter acesso ao
dataset; basta executar as células em ordem (*Runtime > Run all*). O Colab
sempre abre a versão do notebook que está no branch `main` do GitHub; para
salvar alterações feitas lá de volta no repositório use *File > Save a copy in
GitHub*.

### Notebook local

Python 3.10 ou superior:

```
pip install -r requirements.txt
```

Abra `homework2.ipynb` no Jupyter a partir da raiz do repositório e execute as
células em ordem. Para executar tudo pela linha de comando, regravando as
saídas, as figuras e as tabelas do artigo:

```
jupyter nbconvert --to notebook --execute --inplace homework2.ipynb
```

A execução completa leva cerca de 9 minutos num notebook comum (no Colab pode
levar um pouco mais); a maior parte é a busca de hiperparâmetros da rede
neural. Todas as partições aleatórias usam a semente
fixa `SEMENTE = 42`, então os números são reproduzíveis.

### Tabelas e artigo

As tabelas do artigo não são digitadas à mão. A última seção do notebook
escreve os fragmentos em `paper/tabelas/`, que o `main.tex` inclui com
`\input`, e as figuras são salvas em `figuras/` ao longo do notebook. Para
compilar o artigo é preciso uma distribuição LaTeX com a classe `IEEEtran`:

```
cd paper
pdflatex main && bibtex main && pdflatex main && pdflatex main
```

## Autores e contribuições

| Autor | Matrícula | Contribuição |
|---|---|---|
| Ícaro Adriano | 609310 | A preencher |
| Matheus Reis | 571954 | A preencher |
| Alisson Jaime | 555083 | A preencher |
| Vinícius Alexandre Gomes do Nascimento | 568594 | A preencher |

## Uso de IA

Ferramentas de IA foram utilizadas no desenvolvimento deste trabalho. Os
prompts, as respostas e o destino de cada uma estão registrados em
[`USO_DE_IA.md`](USO_DE_IA.md), conforme exigido pelo enunciado.

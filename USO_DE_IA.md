# Apêndice: uso de ferramentas de IA

O enunciado do Homework 2 permite o uso de ferramentas de IA e exige que ele seja
declarado, com os prompts e as respostas registrados em apêndice ou em arquivo
separado do repositório. Este é esse arquivo.

Ferramenta utilizada: **Claude** (Anthropic), versão Opus 5.5, através do
Claude Code.

Cada entrada abaixo registra o que foi pedido, o que a ferramenta devolveu e o
que os autores fizeram com aquilo. As respostas eram extensas e estão
resumidas, com indicação de onde o resultado foi incorporado ao repositório,
que é o registro verificável.

---

## Ícaro Adriano

Sessão de 27/10/2026, Claude Opus 5.5 via Claude Code, com acesso de leitura e
escrita ao repositório local, ao enunciado e ao dataset.

### 1. Adaptação do repositório do Homework 1 para o Homework 2

**Prompt:** "Quero que reserve esse chat para fazer um trabalho de inteligência
computacional aplicada, quero que use como base o repositório [do homework 1],
o atual é o homework 2, esse é o documento de requisitos e orientação. O
dataset que quero que seja usado é o primeiro, o solubility, que já vem no
homework. Quero que você mantenha o padrão do relatório já existente, com a
mesma equipe, etc., apenas que mude o conteúdo dos arquivos para serem
compatíveis com o homework 2. Também quero que o Jupyter seja sincronizado com
o Colab."

**Resposta:** a ferramenta leu o enunciado, o artigo e o notebook do Homework 1
e produziu:

- o notebook `homework2.ipynb`, com a análise exploratória, a transformação de
  Yeo-Johnson, o OLS, o ridge, o PLS (NIPALS) e a validação cruzada
  implementados do zero e comparados com o scikit-learn, a rede neural, os
  testes estatísticos entre modelos e a exportação das tabelas do artigo;
- o artigo `paper/main.tex` no mesmo formato IEEE e com o mesmo bloco de
  autores do Homework 1, e as referências em `paper/refs.bib`;
- a célula inicial do notebook que clona o repositório quando executada no
  Colab, e o botão *Open in Colab* apontando para este repositório;
- a atualização do `README.md` e deste arquivo.

**O que foi feito:** _a preencher pelos autores: o que foi revisado,
conferido, reescrito ou descartado do material gerado._

---

## Matheus Reis

> **A PREENCHER PELO MATHEUS:** transcrever aqui os prompts efetivamente usados
> e um resumo do que a ferramenta devolveu, ou declarar que não usou IA.

---

## Alisson Jaime

> **A PREENCHER PELO ALISSON:** mesma orientação acima.

---

## Vinícius Alexandre Gomes do Nascimento

> **A PREENCHER PELO VINÍCIUS:** mesma orientação acima.

---

## Declaração

_A preencher pelos autores após a revisão do trabalho: quais decisões de
método, interpretações e trechos do texto são dos autores e quais partiram da
ferramenta._ Os resultados numéricos apresentados no artigo são reproduzíveis a
partir do repositório: a execução completa de `homework2.ipynb` regenera todas
as figuras e tabelas a partir do dataset original.

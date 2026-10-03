# Verificação externa das referências (ia-6.1)

O `CLAUDE.md` deste template proíbe inventar referências. As três obras abaixo
foram escolhidas entre as que já constavam na revisão bibliográfica do ia-3.2
(`ex3_2/revisao/matriz-literatura.csv`) e na lista de referências da versão de
qualificação da dissertação (.docx de 21/09/2026). Cada uma foi conferida em
fonte externa ao agente em 03/10/2026, com `curl` sobre a API do Crossref e
sobre a página do repositório/editora. Só entraram no `referencias.bib` depois
de confirmadas.

## 1. `castro2014` — Castro, Aciar e Reategui (2014)

- Fonte consultada: SEDICI (repositório institucional da UNLP),
  <http://sedici.unlp.edu.ar/handle/10915/42368> (metadados Dublin Core da página).
- Conferido:
  - título: "Learning object recommendation for teachers creating lesson plans" — confere;
  - autores: `DC.creator` = "Castro Aneas, Leandro"; "Aciar, Silvana"; "Reategui, Eliseo Berni" — conferem
    (o repositório registra o sobrenome composto "Castro Aneas"; mantive "Castro", como na
    lista de referências da dissertação e na citação em texto "Castro; Aciar; Reategui, 2014");
  - ano: `DCTERMS.issued` = 2014; `DC.date` = 2014-10 — confere;
  - veículo: `DCTERMS.isPartOf` = "XX Congreso Argentino de Ciencias de la Computación (Buenos Aires, 2014)",
    `DC.description` = "XII Workshop de Tecnología Informática Aplicada en Educación" — confere.
- Não há DOI registrado; a entrada usa `url` + `urldate`.
- Resultado: **confirmada**.

## 2. `schulten2020` — Schulten et al. (2020)

- Fontes consultadas:
  - Crossref, <https://api.crossref.org/works/10.1007/978-3-030-52240-7_69> (DOI do capítulo);
  - Crossref, <https://api.crossref.org/works/10.1007/978-3-030-52240-7> (DOI do livro, para os editores);
  - Springer, <https://link.springer.com/chapter/10.1007/978-3-030-52240-7_69> e
    <https://link.springer.com/book/10.1007/978-3-030-52240-7> (volume da série).
- Conferido:
  - título: "Bridging Over from Learning Videos to Learning Resources Through Automatic Keyword Extraction" — confere;
  - autores: Cleo Schulten, Sven Manske, Angela Langner-Thiele, H. Ulrich Hoppe — conferem;
  - ano: 2020 (publicado online em 30/06/2020) — confere;
  - veículo: capítulo de *Artificial Intelligence in Education* (AIED 2020, Part II),
    Lecture Notes in Computer Science, volume 12164, Springer, Cham, p. 382–386 — confere;
  - editores do livro (Crossref do DOI do livro): Ig Ibert Bittencourt, Mutlu Cukurova,
    Kasia Muldner, Rose Luckin, Eva Millán — conferem.
- Resultado: **confirmada**.

## 3. `bulathwela2022` — Bulathwela et al. (2022)

- Fonte consultada: Crossref,
  <https://api.crossref.org/works?query.bibliographic=Power+to+the+Learner+Towards+Human-Intuitive+and+Integrative+Recommendations+with+Open+Educational+Resources>
  → DOI `10.3390/su141811682` (<https://doi.org/10.3390/su141811682>).
- Conferido:
  - título: "Power to the Learner: Towards Human-Intuitive and Integrative Recommendations with Open Educational Resources" — confere;
  - autores: Sahan Bulathwela, María Pérez-Ortiz, Emine Yilmaz, John Shawe-Taylor — conferem;
  - ano/data: 17/09/2022 — confere;
  - veículo: *Sustainability* (MDPI), v. 14, n. 18, artigo 11682, ISSN 2071-1050 — confere.
- Citação direta longa (ambiente `citacao` no capítulo 2): o trecho transcrito é o
  texto literal das duas primeiras frases do **abstract** da obra, tal como devolvido
  pelo campo `abstract` do registro Crossref acima. Não tive acesso ao PDF para
  conferir a paginação interna; o abstract está na primeira página do artigo, por
  isso a citação indica `p. 1`.
- Resultado: **confirmada**.

## Obras da matriz que NÃO foram usadas

Nenhuma obra consultada deixou de confirmar. As demais obras da matriz do ia-3.2
(Wang, 2022; Chen et al., 2024; Chougule et al., 2025 etc.) não foram incluídas
porque o exercício pede apenas três.

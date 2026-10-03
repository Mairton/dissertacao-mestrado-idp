# Contexto da pesquisa — ponto de partida para o Wayfinder

**Programa:** Mestrado Profissional em Administração Pública (IDP). **Orientador:** Prof. Claudiomar Filho.
**Qualificação:** 25/11/2026. **Defesa:** 04/05/2027.
**Título de trabalho:** *Ativos digitais públicos e matriz de referência do ENEM: avaliação técnica de alternativas de classificação automatizada de um acervo educacional audiovisual.*

## Tema e recorte

Acervos audiovisuais mantidos por redes públicas são ativos digitais do Estado cujo valor público depende da capacidade de convertê-los em uso pedagógico. O recorte é o acervo do Preparatório ENEM do Canal Educação (SEDUC-PI): 760 videoaulas ativas em 15 disciplinas, produzidas para a rede estadual do Piauí (224 municípios). O objeto é a articulação automatizada dessas videoaulas às 120 habilidades da matriz de referência do ENEM, para apoiar o planejamento do professor da rede pública sem substituir a decisão pedagógica. A população-alvo do artefato são os docentes do ensino médio da rede estadual; nesta etapa não há coleta com participantes.

## Problema

O professor identifica a habilidade que precisa trabalhar, mas não dispõe de ferramenta que indique, de forma automática e contextualizada, quais videoaulas do acervo público servem a ela. Pergunta de pesquisa: *que alternativas de classificação automatizada permitem a uma rede pública articular um acervo audiovisual já constituído às habilidades da matriz do ENEM, e como se comparam quanto à qualidade da classificação e à viabilidade de execução?* Essa é a pergunta da dissertação; a de aprofundamento, sobre contribuição, está na última seção.

## O que já está decidido

- Método: Design Science Research, com construção e avaliação do artefato; hipóteses como proposições sobre o comportamento do artefato (H1 e H2 no núcleo; H3, utilidade percebida pelos docentes, na proposta de continuidade).
- Artefato: transcrição automática de fala, embeddings BGE-M3 (modelo pré-treinado, só inferência, sem ajuste), similaridade de cosseno entre aula e descritor, ordenamento das habilidades mais próximas; sem histórico de uso (início frio). Saída apresentada ao docente como conjunto ordenado com margem visível, nunca como atribuição única.
- Referência externa de avaliação: a atribuição oficial de habilidade a cada item do ENEM publicada pelo INEP nos microdados (externa, anterior à pesquisa, auditável). É a única referência disponível sem coleta com participantes, e é a salvaguarda declarada para o conflito de interesse (dirijo a organização que opera o Canal Educação).
- Condições comparadas: lexical (TF-IDF, sem IA), vetorial (BGE-M3, Formas A, B e C de representação do alvo) e generativo proprietário. Métricas: concordância na primeira posição e nas cinco primeiras; piso de acaso calculado (3,3% e 16,7%).
- Resultados já obtidos (884 itens, 2020–2024; generativo em 2023, 178 itens): lexical 11,8% / 32,6%; artefato (Forma A) 15,7% / 43,8%; generativo 41,0% / 78,1%; Forma C (alvo construído dos itens, edição retida) 21,5% / 57,8% no agregado. O artefato supera o lexical e fica em menos da metade do generativo, e o texto declara isso sem atenuação. A Forma A permanece como configuração do artefato.
- Limitação declarada: item de prova não é videoaula; a concordância medida valida os métodos, não a classificação das aulas. Os valores são limite superior, não estimativa pontual.
- Revisão de literatura: mapeamento sistemático orientado pelo PRISMA-ScR com desvios declarados, dois blocos com protocolo (técnico 2018–2026; avaliação externa no Brasil 2007–2026) e um eixo narrativo. Estudos que avaliam só por escore interno entram marcados `referencia = inexistente`, não são excluídos.
- Escopo do que não cabe até a defesa: padrão-ouro por professores especialistas e aferição de utilidade percebida ficam na proposta de continuidade, por prazo de apreciação ética.

## O que está em aberto

- Qual é, afinal, a contribuição científica que a dissertação reivindica: o artefato, o desenho de avaliação por referência oficial, ou o achado sobre a representação do descritor (o texto da matriz descreve pior a habilidade do que os itens que o exame lhe atribui).
- Se esse desenho de avaliação já existe na literatura de alinhamento curricular automatizado e de tagging de itens a habilidades, ou se é inédito no uso de atribuição oficial de um órgão como referência.
- Como a quarta condição (modelo generativo aberto, execução local), programada para antes da defesa, entra no argumento.
- A causa da fragilidade em Linguagens e Códigos, para a qual duas explicações já foram testadas e excluídas.
- Qual forma de representação do alvo descreve corretamente uma videoaula; as três formas não convergem e o método mais forte não arbitra entre elas.

## Pergunta de aprofundamento

O que, nesta dissertação, outra pesquisa sobre classificação curricular automatizada teria motivo para citar: o artefato aplicado a um acervo público, o desenho de avaliação por referência oficial do INEP sem julgamento humano, ou o achado de que o texto do descritor da matriz representa a habilidade pior do que os itens que o exame lhe atribui?

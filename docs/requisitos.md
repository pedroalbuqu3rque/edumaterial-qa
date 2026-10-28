# Especificação de Requisitos — Módulo de Busca

**Projeto:** EduMaterial  
**Documento:** `docs/requisitos.md`  
**Versão:** 1.0  
**Status:** Requisitos propostos para estudo de caso  
**Área:** Quality Assurance (QA)

## 1. Objetivo

Definir os requisitos funcionais e os critérios de aceitação do módulo de busca do EduMaterial, estabelecendo comportamentos que possam ser verificados por meio de testes de software.

Este documento faz parte de um projeto de portfólio de QA. Os requisitos descritos são propostas elaboradas para o estudo de caso e não representam funcionalidades confirmadas ou implementadas em uma aplicação real.

## 2. Escopo

O módulo de busca deverá permitir que professores encontrem materiais educacionais por meio de palavras-chave.

A busca deverá considerar três campos:

- Título do material;
- Disciplina;
- Descrição do material.

Também serão considerados os comportamentos para pesquisas sem resultados e para tentativas de pesquisa sem preenchimento do campo.

## 3. Requisitos funcionais

### REQ-001 — Pesquisa por palavra-chave

**Descrição:** O sistema deverá permitir que o usuário pesquise materiais educacionais informando uma palavra-chave.

**Regras de negócio:**
- A pesquisa deverá considerar os campos título, disciplina e descrição.
- Um material deverá ser considerado correspondente quando o termo pesquisado atender à regra de correspondência definida para pelo menos um desses campos.
- A pesquisa deverá apresentar os materiais correspondentes aos critérios utilizados.

**Critérios de aceitação:**
- CA-001.1: Dado que existam materiais com correspondência no título, quando o usuário pesquisar um termo correspondente, então os materiais elegíveis deverão ser apresentados.
- CA-001.2: Dado que existam materiais com correspondência na disciplina, quando o usuário pesquisar um termo correspondente, então os materiais elegíveis deverão ser apresentados.
- CA-001.3: Dado que existam materiais com correspondência na descrição, quando o usuário pesquisar um termo correspondente, então os materiais elegíveis deverão ser apresentados.
- CA-001.4: Quando houver correspondências em mais de um campo, o sistema deverá apresentar os materiais elegíveis sem duplicar o mesmo material nos resultados.

### REQ-002 — Pesquisa sem resultados

**Descrição:** O sistema deverá informar ao usuário quando a pesquisa não retornar materiais correspondentes.

**Regras de negócio:**
- A ausência de resultados deverá ser comunicada por meio de uma mensagem informativa.
- A mensagem deverá orientar o usuário a tentar outros termos de pesquisa.
- A ausência de resultados não deverá ser apresentada como uma falha técnica.

**Critérios de aceitação:**
- CA-002.1: Dado que a pesquisa tenha sido realizada e nenhum material corresponda ao termo informado, quando os resultados forem apresentados, então o sistema deverá exibir uma mensagem indicando que nenhum material foi encontrado.
- CA-002.2: A mensagem deverá sugerir que o usuário altere os termos da pesquisa e tente novamente.
- CA-002.3: A interface deverá permitir que o usuário modifique o termo e realize uma nova pesquisa.

**Mensagem sugerida para o estudo de caso:**

“Nenhum material encontrado. Tente alterar os termos da sua busca.”

### REQ-003 — Pesquisa vazia

**Descrição:** O sistema não deverá iniciar uma pesquisa quando o campo de busca estiver vazio.

**Regras de negócio:**
- Uma pesquisa vazia não deverá substituir o catálogo por uma tela de resultados de pesquisa.
- O catálogo de materiais deverá permanecer visível.
- O comportamento deverá ser consistente quando o campo estiver vazio após a remoção de um termo anteriormente informado.

**Critérios de aceitação:**
- CA-003.1: Dado que o catálogo esteja visível, quando o usuário tentar pesquisar sem informar um termo, então uma pesquisa não deverá ser executada e o catálogo deverá permanecer visível.
- CA-003.2: Dado que o usuário tenha realizado uma pesquisa anteriormente, quando apagar o termo e tentar pesquisar novamente, então o sistema deverá retornar ao estado de catálogo visível, sem apresentar uma pesquisa vazia.

## 4. Requisitos não funcionais e aspectos transversais

Os pontos abaixo são itens propostos para investigação e refinamento, não requisitos formalmente aprovados.

- **Usabilidade:** as mensagens de ausência de resultados deverão ser compreensíveis e orientar o próximo passo.
- **Consistência:** os estados de catálogo e resultados de pesquisa deverão apresentar comportamentos previsíveis.
- **Acessibilidade:** deverá ser investigado se o campo, a ação de pesquisar e as mensagens podem ser utilizados por pessoas que navegam por teclado e tecnologias assistivas.

Critérios específicos de acessibilidade e desempenho serão definidos após o detalhamento do produto.

## 5. Dúvidas em aberto

As seguintes questões precisam ser respondidas antes de considerar a especificação completa:

| ID | Questão | Impacto |
|---|---|---|
| DA-001 | A busca deverá ignorar diferenças entre letras maiúsculas e minúsculas? | Correspondência dos resultados |
| DA-002 | A busca deverá ignorar acentos, como em “geografia” e “geográfia”? | Correspondência dos resultados |
| DA-003 | A correspondência será por palavra completa, por trecho ou por ambos? | Critérios de busca |
| DA-004 | Como os resultados serão ordenados? | Relevância e experiência do usuário |
| DA-005 | Haverá limite de caracteres para o termo pesquisado? | Validação de entrada |
| DA-006 | Espaços antes ou depois do termo serão ignorados? | Tratamento de entrada |
| DA-007 | O catálogo deverá ser atualizado imediatamente após limpar o campo ou somente após uma ação do usuário? | Comportamento da interface |

As respostas deverão ser registradas em uma nova versão do documento quando as decisões forem tomadas.

## 6. Rastreabilidade

Os requisitos serão utilizados como referência para os casos de teste.

| Requisito | Casos de teste previstos |
|---|---|
| REQ-001 | Busca com correspondência no título, disciplina e descrição; correspondências múltiplas |
| REQ-002 | Busca sem resultados; apresentação da mensagem; nova tentativa |
| REQ-003 | Busca vazia; remoção de termo previamente pesquisado |

Cada caso de teste deverá referenciar o requisito correspondente para facilitar a rastreabilidade entre o comportamento esperado e a verificação realizada.

## 7. Status de validação

**Status atual:** especificação inicial proposta.

Os critérios descritos ainda precisam ser refinados e confrontados com a implementação do produto, quando disponível. A existência deste documento não significa que os requisitos tenham sido implementados ou que os testes tenham sido executados.

## 8. Histórico de versões

| Versão | Alteração |
|---|---|
| 1.0 | Criação da especificação inicial do módulo de busca para o estudo de caso. |

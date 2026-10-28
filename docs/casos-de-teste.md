# Casos de Teste — EduMaterial

## 1. Identificação

- **Projeto:** EduMaterial
- **Módulo:** Busca de materiais educacionais
- **Tipo de teste:** Teste funcional manual
- **Documento:** Casos de teste
- **Versão:** 1.0
- **Status:** Planejado — aguardando aplicação funcional para execução

## 2. Objetivo

Documentar os cenários de teste necessários para verificar o comportamento esperado da funcionalidade de busca do EduMaterial, considerando os requisitos definidos no documento `requisitos.md`.

Os casos de teste foram elaborados para orientar futuras execuções manuais e registrar os resultados obtidos quando uma versão funcional da aplicação estiver disponível.

## 3. Pré-condições gerais

Para executar os testes, será necessário:

- Ter acesso a uma versão funcional do EduMaterial.
- Ter acesso ao módulo de busca.
- Dispor de materiais cadastrados no catálogo.
- Conhecer os títulos, as disciplinas e as descrições dos materiais utilizados nos testes.

**Observação:** as pré-condições acima ainda não foram verificadas, pois a aplicação não está disponível para execução dos testes.

## 4. Casos de teste

### CT-001 — Buscar material pelo título

- **Requisito relacionado:** REQ-001
- **Objetivo:** verificar se a busca localiza materiais pelo título.
- **Prioridade:** Alta
- **Tipo:** Positivo

**Pré-condições:**
- O catálogo contém pelo menos um material cadastrado.
- O título do material utilizado no teste é conhecido.

**Dados de teste:**
- Termo de busca: título completo ou trecho conhecido de um material cadastrado.

**Passos:**
1. Acessar o módulo de busca.
2. Localizar o campo de pesquisa.
3. Digitar o título ou trecho do título de um material existente.
4. Acionar a busca, caso seja necessário.
5. Observar os resultados apresentados.

**Resultado esperado:**
O material correspondente ao termo pesquisado aparece nos resultados.

**Resultado obtido:** Não executado.

**Status:** Não executado.

**Evidências:** A registrar durante a execução.

---

### CT-002 — Buscar material pela disciplina

- **Requisito relacionado:** REQ-001
- **Objetivo:** verificar se a busca localiza materiais pela disciplina associada.
- **Prioridade:** Alta
- **Tipo:** Positivo

**Pré-condições:**
- O catálogo contém materiais associados a disciplinas conhecidas.

**Dados de teste:**
- Termo de busca: nome de uma disciplina cadastrada, como Geografia.

**Passos:**
1. Acessar o módulo de busca.
2. Digitar o nome de uma disciplina existente.
3. Acionar a busca, caso seja necessário.
4. Observar os resultados apresentados.

**Resultado esperado:**
Os materiais associados à disciplina pesquisada são apresentados, conforme os critérios definidos para a busca.

**Resultado obtido:** Não executado.

**Status:** Não executado.

**Evidências:** A registrar durante a execução.

---

### CT-003 — Buscar material pela descrição

- **Requisito relacionado:** REQ-001
- **Objetivo:** verificar se a busca considera os termos presentes na descrição dos materiais.
- **Prioridade:** Alta
- **Tipo:** Positivo

**Pré-condições:**
- O catálogo contém materiais com descrições conhecidas.

**Dados de teste:**
- Termo de busca: palavra ou expressão presente na descrição de um material, mas ausente do título.

**Passos:**
1. Acessar o módulo de busca.
2. Digitar um termo conhecido da descrição de um material.
3. Acionar a busca, caso seja necessário.
4. Observar os resultados.

**Resultado esperado:**
O material cuja descrição contém o termo pesquisado é apresentado nos resultados.

**Resultado obtido:** Não executado.

**Status:** Não executado.

**Evidências:** A registrar durante a execução.

---

### CT-004 — Realizar busca sem resultados correspondentes

- **Requisito relacionado:** REQ-002
- **Objetivo:** verificar o comportamento da aplicação quando nenhum material corresponde ao termo pesquisado.
- **Prioridade:** Alta
- **Tipo:** Negativo

**Pré-condições:**
- O módulo de busca está disponível.
- O termo utilizado não corresponde a nenhum material cadastrado.

**Dados de teste:**
- Termo de busca: uma expressão que não exista no catálogo.

**Passos:**
1. Acessar o módulo de busca.
2. Digitar um termo sem correspondências no catálogo.
3. Acionar a busca, caso seja necessário.
4. Observar a mensagem apresentada.

**Resultado esperado:**
A aplicação não apresenta materiais incompatíveis com a busca e exibe a mensagem:

> Nenhum material encontrado. Tente alterar os termos da sua busca.

A interface também deve orientar o usuário a modificar os termos pesquisados, conforme especificado no requisito.

**Resultado obtido:** Não executado.

**Status:** Não executado.

**Evidências:** A registrar durante a execução.

---

### CT-005 — Acessar o catálogo com o campo de busca vazio

- **Requisito relacionado:** REQ-003
- **Objetivo:** verificar se uma busca vazia é impedida e se o catálogo permanece acessível.
- **Prioridade:** Alta
- **Tipo:** Negativo / Validação de entrada

**Pré-condições:**
- O catálogo está disponível.

**Dados de teste:**
- Campo de busca vazio.

**Passos:**
1. Acessar o módulo de busca.
2. Deixar o campo de pesquisa vazio.
3. Tentar acionar a busca, caso exista um botão específico.
4. Observar o comportamento da interface.

**Resultado esperado:**
A aplicação não executa uma pesquisa vazia e mantém o catálogo visível, conforme o requisito definido.

**Resultado obtido:** Não executado.

**Status:** Não executado.

**Evidências:** A registrar durante a execução.

---

### CT-006 — Limpar o termo pesquisado

- **Requisito relacionado:** REQ-003
- **Objetivo:** verificar se o usuário consegue retornar à visualização do catálogo após realizar uma busca.
- **Prioridade:** Média
- **Tipo:** Funcional

**Pré-condições:**
- O catálogo contém materiais cadastrados.
- Uma busca anterior pode ser realizada.

**Dados de teste:**
- Termo de busca: nome de um material existente.

**Passos:**
1. Acessar o módulo de busca.
2. Pesquisar um material existente.
3. Limpar o conteúdo do campo de pesquisa.
4. Observar o catálogo e os resultados apresentados.

**Resultado esperado:**
Após limpar o campo, o comportamento da interface deve seguir a regra definida para retorno ao catálogo.

**Observação:** a regra exata para atualizar os resultados após limpar o campo ainda precisa ser confirmada no documento de requisitos.

**Resultado obtido:** Não executado.

**Status:** Não executado.

**Evidências:** A registrar durante a execução.

---

## 5. Resumo dos casos de teste

| ID | Cenário | Requisito | Prioridade | Status |
|---|---|---|---|---|
| CT-001 | Busca por título | REQ-001 | Alta | Não executado |
| CT-002 | Busca por disciplina | REQ-001 | Alta | Não executado |
| CT-003 | Busca por descrição | REQ-001 | Alta | Não executado |
| CT-004 | Busca sem resultados | REQ-002 | Alta | Não executado |
| CT-005 | Busca com campo vazio | REQ-003 | Alta | Não executado |
| CT-006 | Limpar a busca | REQ-003 | Média | Não executado |

## 6. Critérios para registro da execução

Quando a aplicação estiver disponível, cada caso deverá ser atualizado com:

- **Resultado obtido:** comportamento realmente observado.
- **Status:** aprovado, reprovado, bloqueado ou não executado.
- **Evidências:** capturas de tela, gravações ou outros registros relevantes.
- **Defeitos identificados:** descrição do comportamento divergente do esperado, quando houver.

Um caso será considerado **aprovado** quando o resultado observado corresponder ao resultado esperado. Será considerado **reprovado** quando houver divergência. Será considerado **bloqueado** quando uma condição impedir sua execução.

## 7. Rastreabilidade

Os casos de teste estão relacionados aos seguintes requisitos:

- **REQ-001:** busca por título, disciplina e descrição — CT-001, CT-002 e CT-003.
- **REQ-002:** comportamento quando não há resultados — CT-004.
- **REQ-003:** comportamento da busca vazia e retorno ao catálogo — CT-005 e CT-006.

## 8. Limitações conhecidas

- A aplicação ainda não está disponível para testes funcionais.
- Os dados de teste são exemplos e precisam ser validados em um catálogo real.
- Algumas regras de comportamento ainda dependem da confirmação dos requisitos.
- Nenhum caso de teste deste documento foi executado.

## 9. Histórico de versões

| Versão | Alteração |
|---|---|
| 1.0 | Criação inicial dos casos de teste planejados. |

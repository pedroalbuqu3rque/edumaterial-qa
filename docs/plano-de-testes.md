# Plano de Testes — EduMaterial

**Projeto:** EduMaterial  
**Documento:** `docs/plano-de-testes.md`  
**Versão:** 1.0  
**Status:** Planejamento inicial  
**Responsável:** QA do projeto de portfólio

## 1. Objetivo

Definir a estratégia de testes do módulo de busca do EduMaterial, estabelecendo o escopo, os recursos necessários, os riscos e os critérios para execução e conclusão dos testes.

Este documento faz parte de um estudo de caso independente de Quality Assurance. As atividades descritas representam um planejamento proposto, e não uma execução de testes em uma aplicação funcional.

## 2. Escopo dos testes

### 2.1 Itens incluídos

Serão planejados testes funcionais manuais para verificar:

- Pesquisa de materiais pelo título;
- Pesquisa de materiais pela disciplina;
- Pesquisa de materiais pela descrição;
- Apresentação dos resultados correspondentes;
- Comportamento quando nenhum material é encontrado;
- Exibição de orientação para modificar os termos da busca;
- Comportamento diante de uma pesquisa vazia;
- Retorno ao catálogo após a remoção de um termo pesquisado;
- Ausência de duplicação de materiais quando houver correspondência em mais de um campo.

### 2.2 Itens inicialmente fora do escopo

Nesta primeira etapa, não serão executados testes de:

- Desempenho e carga;
- Segurança e testes de invasão;
- Integração com serviços externos;
- Compatibilidade entre diferentes navegadores;
- Acessibilidade completa;
- Testes automatizados.

Esses itens poderão ser incorporados em etapas futuras, conforme a evolução do projeto e a disponibilidade da aplicação.

## 3. Estratégia de testes

A abordagem inicial será baseada em testes funcionais manuais.

Cada caso de teste deverá conter:

- Identificador único;
- Requisito relacionado;
- Objetivo;
- Pré-condições;
- Dados de teste;
- Passos de execução;
- Resultado esperado;
- Prioridade;
- Resultado observado;
- Status da execução;
- Evidências, quando aplicáveis.

Os resultados esperados serão derivados dos requisitos e critérios de aceitação documentados em `docs/requisitos.md`.

Os resultados observados somente serão preenchidos após a execução efetiva de cada teste.

## 4. Técnicas de teste previstas

### 4.1 Particionamento de equivalência

Agrupar entradas que devem produzir comportamentos semelhantes.

Exemplos:
- Termo com correspondência em um material;
- Termo sem correspondência;
- Campo de busca vazio.

### 4.2 Análise de valores-limite

Será aplicada quando existirem limites definidos, como quantidade mínima ou máxima de caracteres permitidos.

Esses limites ainda precisam ser especificados antes da elaboração dos testes correspondentes.

### 4.3 Testes baseados em requisitos

Cada requisito funcional será associado a um ou mais casos de teste, permitindo verificar se os critérios de aceitação foram atendidos.

## 5. Ambiente de testes

**Situação atual:** ambiente funcional ainda não disponível.

Antes da execução, será necessário identificar:

- Aplicação ou versão a ser testada;
- URL ou forma de acesso;
- Navegador e versão;
- Sistema operacional;
- Massa de dados de teste;
- Condições necessárias para reproduzir os cenários.

Até que essas informações estejam disponíveis, os casos de teste poderão ser elaborados e revisados, mas não serão classificados como executados.

## 6. Dados de teste

Será planejada uma massa de dados controlada, contendo materiais com diferentes títulos, disciplinas e descrições.

Os dados deverão permitir verificar:

- Correspondências exclusivas em cada campo;
- Correspondências em mais de um campo;
- Ausência de correspondências;
- Repetição de termos em materiais diferentes;
- Busca vazia;
- Nova pesquisa após limpar o campo.

Os valores concretos serão definidos na documentação dos casos de teste.

## 7. Priorização

A prioridade inicial será definida considerando o impacto do comportamento no objetivo principal do módulo.

| Prioridade | Critério | Exemplos |
|---|---|---|
| Alta | Impede ou compromete a descoberta de materiais | Busca não retorna materiais que deveriam corresponder |
| Média | Compromete a compreensão ou a qualidade dos resultados | Mensagem de ausência de resultados inadequada |
| Baixa | Comportamento secundário sem impacto relevante no fluxo principal | Ajustes de texto sem perda de compreensão |

A prioridade será reavaliada conforme os riscos e os comportamentos reais da aplicação forem conhecidos.

## 8. Riscos e limitações

### Riscos identificados

- Requisitos incompletos podem gerar interpretações diferentes;
- Ausência de dados de teste adequados pode limitar a cobertura;
- Regras de correspondência ainda não definidas podem causar divergências nos resultados esperados;
- Indisponibilidade da aplicação impede a validação funcional.

### Limitações atuais

Este projeto encontra-se na fase de planejamento. Ainda não há evidências de execução, defeitos confirmados ou resultados de aprovação.

As decisões pendentes registradas em `docs/requisitos.md` deverão ser revisadas antes da execução dos casos que dependam delas.

## 9. Critérios de entrada

A execução dos testes funcionais poderá começar quando:

- A aplicação estiver acessível;
- Os requisitos relevantes estiverem suficientemente definidos;
- O ambiente e a versão testada forem identificados;
- Os dados de teste estiverem preparados;
- Os casos de teste prioritários estiverem documentados;
- Os resultados esperados forem objetivos e verificáveis.

## 10. Critérios de saída

A etapa de testes será considerada concluída para o escopo acordado quando:

- Todos os casos planejados para a rodada tiverem um status registrado;
- Os resultados observados e as evidências estiverem documentados;
- Os defeitos encontrados tiverem sido registrados;
- Os casos bloqueados ou não executados estiverem identificados;
- Os riscos remanescentes e as limitações estiverem descritos;
- Um relatório de execução estiver disponível.

A conclusão dos testes não significa necessariamente ausência de defeitos. Significa que a execução planejada foi documentada e que os riscos conhecidos foram comunicados.

## 11. Entregáveis

- Especificação de requisitos;
- Plano de testes;
- Casos de teste;
- Relatórios de defeitos;
- Evidências de execução;
- Relatório final da rodada de testes.

## 12. Rastreabilidade

| Requisito | Área de teste |
|---|---|
| REQ-001 | Busca por palavra-chave e apresentação de resultados |
| REQ-002 | Ausência de resultados e orientação ao usuário |
| REQ-003 | Busca vazia e manutenção do catálogo visível |

## 13. Histórico de versões

| Versão | Alteração |
|---|---|
| 1.0 | Criação do plano inicial de testes do módulo de busca. |

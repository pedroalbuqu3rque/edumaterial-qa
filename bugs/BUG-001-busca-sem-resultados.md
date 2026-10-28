BUG-001 — Busca sem resultados deixa a página em branco

Tipo: Cenário hipotético de treinamento
Status: Simulado / não validado
Severidade: Média
Prioridade: Alta (classificação inicial)
Caso de teste: CT-004

Descrição:
Ao realizar uma pesquisa por um termo que não corresponde a nenhum material do catálogo, a página fica em branco, sem informar ao usuário que nenhum resultado foi encontrado.

Pré-condições:
- Usuário na página do catálogo.
- Nenhum material corresponde ao termo pesquisado.

Passos para reproduzir:
1. Acessar o catálogo.
2. Digitar Astronomia no campo de busca.
3. Executar a pesquisa.
4. Observar o comportamento da página.

Resultado esperado:
Exibir: “Nenhum material encontrado. Tente alterar os termos da sua busca.”

Resultado observado no cenário hipotético:
A página fica em branco e não apresenta mensagem ou orientação.

Justificativa da severidade:
Média, pois a ausência de feedback pode transmitir a impressão de que a plataforma está inoperante, prejudicando a compreensão do usuário, embora outras funcionalidades possam continuar disponíveis.

Justificativa da prioridade:
Alta, como classificação inicial, caso a equipe confirme que a falha compromete uma funcionalidade central e afeta significativamente os usuários. Reavaliar conforme impacto, frequência e alternativas.

Evidências:
Nenhuma evidência real disponível. Cenário criado para treinamento.

Ambiente:
Não aplicável — não executado em aplicação real.

Caso de teste relacionado

ID: CT-004

Requisito relacionado: REQ-002

Resultado no cenário simulado: Fail

Status da execução real: Não executado

Justificativa: No cenário hipotético, a página fica em branco quando a pesquisa não encontra resultados, contrariando o comportamento esperado de exibir uma mensagem informativa.

# Constituição do workspace

## Propósito

Este workspace coordena a evolução de microserviços e seus artefatos de descoberta, decisão e entrega. Ele não substitui os repositórios dos serviços: cada serviço em `microservices/` preserva sua própria história, regras e ciclo de release.

## Princípios de trabalho

- Use português em perguntas, planos, decisões e resumos, salvo solicitação contrária.
- Comece por entender o contexto e as regras locais (`CLAUDE.md` do serviço) antes de alterar código.
- Registre decisões relevantes em `docs/agentic/decisions.md` e aprendizados reutilizáveis em `docs/agentic/learnings.md`.
- Planeje antes de implementar mudanças não triviais; aguarde aprovação explícita quando houver uma etapa de aprovação.
- Mantenha o escopo solicitado. Não crie contratos, status de domínio, metas de desempenho ou regras de identidade sem evidência ou decisão registrada.
- Trate credenciais, dados pessoais, tokens e dados de produção como confidenciais. Nunca os grave em documentação, tarefas ou commits.

## Fluxo padrão

1. Refinar o pedido e identificar lacunas materiais.
2. Investigar o serviço, dependências e evidências disponíveis.
3. Produzir um plano verificável e obter a aprovação necessária.
4. Implementar mudanças pequenas, coesas e reversíveis.
5. Revisar, testar e registrar o resultado e os riscos restantes.

Consulte `docs/agentic/workflow.md` para o fluxo detalhado e `.claude/agents/` para os papéis.

## Organização

- `.claude/`: configuração, agentes, skills e regras locais.
- `docs/`: conhecimento compartilhado do ecossistema, negócio e operação agentic.
- `work/tasks/`: artefatos temporários por tarefa; não é fonte de verdade de produto.
- `microservices/`: pontos de montagem para checkouts independentes dos serviços.

## Precedência de instruções

Instruções explícitas do usuário prevalecem. Em seguida, aplique este arquivo, as regras de `.claude/rules/` e, por fim, o `CLAUDE.md` do microserviço em escopo. Em caso de conflito entre o workspace e o serviço, siga o arquivo mais específico, exceto por requisitos de segurança.

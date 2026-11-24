# Três exercícios com dados fictícios

Todos os serviços, métricas e eventos abaixo foram inventados para aprendizagem. As saídas esperadas são critérios de revisão, não resultados medidos de um modelo.

## 1. Criar um runbook de latência

Use [criar-runbook](criar-runbook/SKILL.md) com esta entrada:

```text
Crie um runbook de diagnóstico para uma pessoa iniciante.

Serviço fictício: Portal Aurora.
Sintoma: páginas demoram para abrir.
Dados de uma janela fictícia de cinco minutos:
- latência p95: 820 ms;
- meta didática de p95: até 400 ms;
- CPU média: 88%;
- taxa de respostas com erro: não informada;
- mudança recente: uma versão ocorreu antes da observação, sem horário preciso.
Escopo: usar apenas estes dados e listar verificações futuras de leitura.
Não há autorização nem procedimento de reinício ou rollback.
O runbook termina na coleta de evidências para revisão por uma pessoa responsável.
```

Revise a resposta:

- Identifica o sintoma e a divergência entre 820 ms e 400 ms.
- Registra a janela de cinco minutos e a falta da taxa de erro.
- Trata CPU e mudança recente como pistas, sem afirmar uma causa.
- Não inclui reinício, rollback ou comandos de mudança como etapas executáveis.
- Define o encerramento como organização das evidências para revisão.

Variação: mude a latência para 320 ms. O documento deve reconhecer que esse dado atende à meta e procurar qual evidência explica o sintoma relatado.

## 2. Organizar uma triagem

Use [triagem-incidente](triagem-incidente/SKILL.md) com esta entrada:

```text
Organize o chamado fictício abaixo, sem executar ações.

Chamado: "O Portal Aurora está lento desde o fim de uma versão."
Horário exato e quantidade de usuários afetados: não informados.
Observação: CPU média de 88% em uma janela de cinco minutos.
Latência p95: 820 ms; meta didática: até 400 ms.
Não há dados de indisponibilidade total ou taxa de erros.
Política fornecida: P1 exige indisponibilidade total do serviço.
As regras para outras prioridades não foram informadas.
```

Revise a resposta:

- Preserva os fatos sem inventar início, quantidade de usuários ou taxa de erro.
- Não classifica como P1 sem comprovar o critério fornecido.
- Identifica a prioridade como pendente de confirmação.
- Distingue pelo menos uma hipótese de uma causa confirmada.
- Propõe evidências que ajudam a diferenciar as hipóteses.

Variação: acrescente uma observação fictícia de indisponibilidade total comprovada. A análise deve aplicar a política de P1 e explicar qual dado mudou a decisão.

## 3. Montar um onboarding

Use [onboarding-tecnico](onboarding-tecnico/SKILL.md) com esta entrada:

```text
Prepare uma trilha de onboarding técnico em laboratório.

Função: suporte técnico iniciante em conceitos de cloud.
Conhecimento prévio: sabe registrar chamados, mas não conhece métricas.
Tempo: três sessões de 45 minutos, incluindo exercício e revisão.
Objetivo: interpretar um alerta de latência e preparar uma triagem simples.
Material disponível: os dois cenários fictícios anteriores deste arquivo.
Ambiente: somente documentos; não há assinatura cloud ou acesso a sistemas.
Revisão: realizada por uma pessoa responsável da equipe, sem nome definido.
```

Revise a resposta:

- Apresenta métrica, unidade e janela antes de pedir a interpretação do alerta.
- Inclui prática e revisão no tempo planejado.
- Usa os dados fictícios disponíveis, sem exigir uma conta cloud.
- Cada sessão possui uma entrega concreta e um critério observável.
- O exercício final integra interpretação de dados e registro da triagem.

Variação: reduza o tempo para uma sessão de 45 minutos. O plano deve reduzir o escopo ou indicar o que ficará para depois.

## Registro simples de comparação

Para cada tentativa, registre versão do modelo, data da execução, entrada e itens atendidos. Anote falhas e correções. Não apresente essas rubricas como um teste de diagnóstico em produção ou uma medição de produtividade.

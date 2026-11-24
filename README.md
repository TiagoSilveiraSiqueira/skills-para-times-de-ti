![Skills para times de TI: instruções reutilizáveis](assets/banner.svg)

# Skills para times de TI

Instruções reutilizáveis para transformar informações de laboratório em runbooks, triagens de incidentes e materiais de onboarding. O objetivo é ajudar quem está começando e facilitar a revisão por quem supervisiona uma equipe.

**Autor:** Tiago Silveira Siqueira · Supervisor de TI · IA aplicada e cloud

## Comece em 10 minutos

1. Abra [EXEMPLOS.md](EXEMPLOS.md) e escolha um dos três cenários fictícios.
2. Abra o `SKILL.md` correspondente e copie o conteúdo depois do cabeçalho YAML para seu assistente de IA.
3. Cole o cenário e peça o resultado descrito no exemplo.
4. Compare a resposta com os critérios de revisão apresentados no mesmo arquivo.
5. Ajuste uma informação de entrada e observe o que muda. Não execute ações em um ambiente real.

O uso manual permite experimentar as instruções sem instalar extensões, fornecer chaves ou conectar serviços.

## O que você encontra

| Skill | Quando usar | Resultado |
|---|---|---|
| [criar-runbook](criar-runbook/SKILL.md) | Documentar um procedimento de diagnóstico conhecido | Runbook com pré-condições, etapas, evidências e limites |
| [triagem-incidente](triagem-incidente/SKILL.md) | Organizar um chamado e seus sintomas | Resumo, impacto declarado, hipóteses e próximos passos |
| [onboarding-tecnico](onboarding-tecnico/SKILL.md) | Preparar uma trilha inicial para uma função técnica | Plano de aprendizagem com exercícios e critérios observáveis |

## Prompt, skill e agente

- **Prompt:** instrução para uma interação específica.
- **Skill:** conjunto de instruções reutilizáveis que orienta um assistente em uma tarefa recorrente.
- **Agente:** software que pode combinar um modelo com ferramentas e um fluxo de execução.

Este repositório contém skills de documentação e exemplos. Ele não inclui um agente executável nem concede acesso a máquinas, contas ou serviços.

## Instalação no Codex

Copie cada pasta de skill para `~/.codex/skills/`. No Windows, `~` corresponde à pasta do seu usuário. Se você configurou `CODEX_HOME`, use a pasta `skills` dentro desse diretório.

```text
~/.codex/skills/
├── criar-runbook/SKILL.md
├── triagem-incidente/SKILL.md
└── onboarding-tecnico/SKILL.md
```

Inicie uma nova sessão para que a descoberta de skills reflita os arquivos copiados. Peça, por exemplo: `Use $criar-runbook com o cenário fictício abaixo.`

## Instalação no Claude Code

Para disponibilizar as skills em um projeto, copie as três pastas para `.claude/skills/` na raiz desse projeto. Para uso pessoal em vários projetos, use `~/.claude/skills/`.

```text
seu-projeto/.claude/skills/
├── criar-runbook/SKILL.md
├── triagem-incidente/SKILL.md
└── onboarding-tecnico/SKILL.md
```

Peça, por exemplo: `/triagem-incidente` e forneça o cenário. A interface e a descoberta podem variar entre versões; confirme que sua instalação encontrou a skill. O formato foi revisado localmente, mas a integração não foi testada dentro do Claude Code.

## Como avaliar uma resposta

Para trabalhar com fatos reais já públicos, consulte [CASOS-PUBLICOS.md](CASOS-PUBLICOS.md). Os estudos vinculados indicam as fontes e diferenciam a informação disponível no início do incidente do conhecimento da análise posterior.

Uma boa resposta separa fatos de hipóteses, identifica lacunas e permite que outra pessoa revise o raciocínio. Uma resposta longa ou confiante não comprova que o diagnóstico esteja correto.

Os exemplos usam serviços, métricas e equipes inventados. Use apenas material fictício ou previamente autorizado e sem credenciais, dados pessoais ou detalhes internos. As skills produzem documentos; não alteram ambientes, enviam mensagens ou abrem chamados.

## Contribua

Uma contribuição útil traz um cenário fictício, a resposta problemática, o comportamento esperado e uma proposta pequena de melhoria. Não inclua dados da sua empresa, capturas de sistemas internos ou arquivos de configuração reais.

Conteúdo sob [licença MIT](LICENSE). Resultados gerados por modelos precisam de revisão humana antes de serem usados fora do laboratório.

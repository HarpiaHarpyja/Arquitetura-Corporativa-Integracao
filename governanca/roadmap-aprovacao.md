# Roadmap de definição e gates de aprovação

[↑ Índice](../README.md) · [Proposta executiva](proposta-executiva.md)

## Quatro níveis e doze etapas

| Nível | Etapas | Entregáveis | Gate |
|---|---|---|---|
| Negócio | 01 UC; 02 capacidades; 03 domínios; 04 processos/regras | Catálogos e fluxos | **G1** — Aprovação do problema e das responsabilidades |
| Informação | 05 entidades; 06 eventos/estados; 07 modelo lógico; 08 governança | Modelos e fontes oficiais | **G2** — Aprovação de identidade, histórico e autoridade |
| Aplicações | 09 serviços; 10 contratos; 11 interfaces/indicadores | Fluxos funcionais e critérios de consumo | **G3** — Aprovação da arquitetura lógica |
| Tecnologia | 12 definição técnica e implantação | Design técnico, custo, fases e testes | **G4** — Aprovação de orçamento e execução |

**Este repositório documenta até G3 de forma conceitual.** Interfaces e indicadores são referências de validação, não especificações finais; G4 não é iniciado.

## Estratégia híbrida

1. **Horizontal:** revisar UCs, capacidades, domínios e núcleo de entidades para toda a empresa.
2. **Vertical:** detalhar percurso ponta a ponta de UCs prioritários.
3. **Revisão:** consolidar ativos e contratos reutilizáveis antes de novos projetos.
4. **Implantação futura:** por ondas após validação de esforço, risco e orçamento.

| Onda sugerida (não aprovada) | UCs | Resultado esperado |
|---|---|---|
| Fundação | UC-001 + UC-004 | Identidade corporativa e alocação |
| Informação gerencial/financeira | UC-002 + UC-003 | Entrega/recebimento e visão Cliente 360° |
| Engenharia e serviços | UC-005 + UC-006 | Modificações, OS, manutenção |
| Observabilidade | UC-007 | Indicadores e aprofundamento em telemetria |
| Suprimentos | UC-008 | Lotes, consumo e rastreabilidade fornecedor→campo |

**Suprimentos deve participar do modelo conceitual desde o início**, ainda que sua implantação seja posterior.

## Registro de decisões pendentes

| ID | Decisão | Responsável pela validação |
|---|---|---|
| DEC-001 | Fonte oficial da identidade corporativa | Diretoria / Gestão de ativos |
| DEC-002 | Confluence mantém documento manual ou visão dinâmica? | Engenharia / Serviços |
| DEC-003 | Quem confirma recebimento e sob qual evidência? | Logística / Serviços |
| DEC-004 | Gatilhos contratuais de faturamento | Comercial / Financeiro |
| DEC-005 | Política de alocação múltipla e centros de custo | Comercial / Gestão de ativos |
| DEC-006 | Aprovação, vigência e reversão de testes em campo | Engenharia / Qualidade |
| DEC-007 | Estrutura oficial de OS, intervenção e custos | Serviços / Financeiro |
| DEC-008 | Definição de disponibilidade por produto | Operação / Engenharia |
| DEC-009 | Serialização e rastreio de componentes/lotes | Suprimentos / Qualidade / Produção |
| DEC-010 | Matriz de acesso por domínio, cliente e sensibilidade | Gestão / Responsável por dados |

## Saída da revisão executiva

Registrar **aprovado, aprovado com ressalvas ou reprovado**, data, sponsor, responsáveis, itens pendentes e próximo gate. Não marcar o desenho como implantado apenas por constar no repositório.

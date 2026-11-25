# 01 — Catálogo de casos de uso corporativos

[← Visão geral](../README.md) · [Próximo: capacidades →](capacidades.md)

> **Situação:** conjunto inicial proposto e aceito para orientar a arquitetura. Os requisitos específicos permanecem sujeitos à validação com os responsáveis. Os IDs são estáveis.

| ID | Caso de uso | Gatilho/consulta | Resultado verificável |
|---|---|---|---|
| UC-001 | Nascimento de um dispositivo | Registro concluído pela produção | Identidade única; histórico acessível; provisionamento OTA rastreado; sem digitação repetida |
| UC-002 | Expedição, recebimento e faturamento | Movimentação e confirmação de recebimento | Elegibilidade consultável conforme contrato; rastreio do evento de entrega |
| UC-003 | Consulta consolidada por cliente | Gestor seleciona cliente | Navegação cliente→organização→dispositivo→histórico técnico/financeiro |
| UC-004 | Alocação e realocação | Mudança de responsável ou local | Cliente, contrato, unidade e centro de custo com validade temporal |
| UC-005 | Modificações experimentais | Alteração autorizada / executada | Identificar dispositivos experimentais, alterações vigentes, reversões e campanhas |
| UC-006 | Ocorrência e ordem de serviço | Técnico identifica condição em campo | Ocorrência→triagem→OS→intervenção→validação, com rastreabilidade |
| UC-007 | Saúde e diagnóstico operacional | Telemetria recebida / consulta gerencial | Indicadores agregados; drill-down para dados específicos, preservando semântica |
| UC-008 | Suprimentos e rastreabilidade de componentes | Compra, recebimento, inspeção e consumo | Saber fornecedor/lote, utilização em produto e impacto de não conformidade |

## Especificação mínima para cada UC

Cada caso de uso deve conter: **ator, objetivo, gatilho, pré-condições, fluxo normal, exceções, regras, entidades, eventos, capacidades, critério de aceitação e responsável por validação**. Os percursos completos estão em [exemplos](../README.md#navegação-por-problema-real).

## Critérios de aceite transversais

1. Uma alteração legítima em uma fonte oficial não requer recadastramento manual em sistemas consumidores.
2. O histórico permite consultar a situação **em uma data passada** (alocação, configuração e estados relevantes).
3. Falhas parciais de integração deixam pendências observáveis e recuperáveis.
4. O identificador corporativo não é substituído por MAC, número de série, ID do Jira ou ID do OTA.
5. Inclusão de produto ou domínio novo não exige alterar os dados brutos dos produtos existentes.
6. As regras comerciais de faturamento são **configuráveis por contrato**, não presumidas universais.
7. Visões executivas agregam apenas métricas equivalentes e distinguem não aplicável, desconhecido e zero.
8. Alterações de engenharia, suprimentos, produção e serviço vinculam os registros de origem e responsável.

## Escopo e fronteiras

Casos de uso **não** decidem protocolos, tabelas físicas ou fornecedor de software. O catálogo descreve resultados do negócio. A aprovação final deverá ser obtida com responsáveis de cada domínio.

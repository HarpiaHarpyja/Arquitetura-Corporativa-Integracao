# Princípios, pressupostos e riscos arquiteturais

[↑ Índice](../README.md)

## Princípios

1. **Unificar significado e processos, não forçar um sistema único.**
2. **Uma fonte autorizada por atributo/fato:** registros podem ser consumidos em várias ferramentas, mas não digitados repetidamente.
3. **Identidade corporativa imutável:** manter correspondências com IDs externos.
4. **Histórico preservado:** eventos, alterações, lotes e relações com validade temporal.
5. **Estados por dimensão:** operação, logística, faturamento, comunicação e qualidade independentes.
6. **Núcleo comum + extensões:** diferentes produtos retêm telemetria própria.
7. **Reutilização de capacidades:** serviço responde a vários UCs.
8. **Integrações recuperáveis:** idempotência, reconciliação e rastreio.
9. **Governança proporcional:** responsabilidade e menor privilégio, sem burocracia desnecessária.
10. **Decisões reversíveis:** não fixar tecnologia antes dos requisitos.
11. **Análise em duas direções:** TOP-DOWN e BOTTOM-UP.
12. **Expansão controlada:** novos domínios seguem a mesma metodologia.

## Pressupostos a validar

- Jira atualmente registra fatos de fabricação e/ou serviço.
- Confluence contém documentação de ciclo de vida montada manualmente.
- Servidor OTA mantém seu cadastro próprio.
- BigQuery armazena séries de telemetria de diferentes produtos.
- Clientes podem ter centros de custo e contratos múltiplos.
- Dados de recebimento, condições de NF, suprimentos e estoque estão fragmentados ou ainda não foram mapeados.
- Há componentes físicos substituíveis entre conjuntos Gancho/central.

## Riscos e mitigação

| Risco | Consequência | Mitigação proposta |
|---|---|---|
| Centralizar sem governar | Única fonte de dados errados | Donos, contratos, reconciliação |
| Implantar dashboard antes da identidade | Visões divergentes | Identidade e relações primeiro |
| Repetir cadastro entre sistemas | Conflito e retrabalho | Fluxo de registro único |
| Confundir versão planejada x instalada | Diagnóstico equivocado | Perspectivas independentes |
| Perder histórico de cliente/CC | Rateio e auditoria incorretos | Alocações temporais |
| Ignorar conectividade intermitente | Eventos atrasados e falsos alertas | event_time vs recorded_at |
| Esquema rígido de telemetria | Novo produto exige redesenho | Extensões versionadas |
| Automatizar faturamento sem regra contratual | Erros de NF | Elegibilidade validada |
| Lote de fornecedor sem vínculo ao dispositivo | Falha de rastreio em campo | Consumo e histórico por lote |
| Excesso de escopo | Projeto sem resultado | Implementação posterior em ondas e gates |

## Premissas não aprovadas

As fontes oficiais, as regras de negócio, a existência de dados no sistema atual, a cobertura de estoque, os vínculos de composição e as metas de ROI **não estão validadas**. Documentos são proposta, não inventário auditado.

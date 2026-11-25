# Matriz de rastreabilidade TOP-DOWN

[↑ Índice](../README.md) · [Casos de uso](../01-negocio/casos-de-uso.md)

A matriz permite justificar qualquer serviço, contrato ou futuro componente técnico por uma necessidade corporativa.

| UC | Capacidade principal | Entidades principais | Eventos principais | Serviços | Contratos |
|---|---|---|---|---|---|
| UC-001 | CAP-001, CAP-002, CAP-010 | Dispositivo, Modelo, Registro de fabricação | EVT-001, EVT-002, EVT-014 | SVC-001, SVC-003, SVC-010 | CT-001, CT-002 |
| UC-002 | CAP-007, CAP-009 | Dispositivo, Remessa, Recebimento, Contrato | EVT-003, EVT-004, EVT-010 | SVC-004, SVC-007 | CT-003, CT-004 |
| UC-003 | CAP-003, CAP-008 | Cliente, Unidade, Alocação, Dispositivo | EVT-005, EVT-009 | SVC-002, SVC-008 | CT-005, CT-008 |
| UC-004 | CAP-003, CAP-002 | Cliente, Centro de custo, Contrato, Alocação | EVT-005 | SVC-002 | CT-005 |
| UC-005 | CAP-004, CAP-006 | Configuração, Modificação, Campanha | EVT-006, EVT-008 | SVC-003, SVC-005 | CT-006, CT-007 |
| UC-006 | CAP-006, CAP-005 | Ocorrência, OS, Intervenção, Consumo | EVT-007, EVT-008, EVT-013 | SVC-005, SVC-009 | CT-007, CT-010 |
| UC-007 | CAP-008, CAP-004 | Observação, Indicador, Dispositivo, Alocação | EVT-009 | SVC-006, SVC-008 | CT-008 |
| UC-008 | CAP-005, CAP-010 | Fornecedor, Pedido, Lote, Consumo, Dispositivo | EVT-011, EVT-012, EVT-013 | SVC-009, SVC-001 | CT-009, CT-010 |

## Aplicação

Se uma nova integração for proposta, exigir a cadeia **UC → CAP → ENT/EVT → SVC → CT**. Caso falte vínculo, avaliar se a integração responde a uma necessidade existente ou se um novo caso de uso deve ser registrado.

## Exceções conhecidas

- A matriz é inicial, não substitui um levantamento detalhado de todos os relacionamentos.
- Um mesmo contrato pode servir diversos casos de uso.
- A etapa tecnológica posterior deve acrescentar componentes e testes, sem perder as referências anteriores.

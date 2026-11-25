# 04 — Processos e regras de negócio

[← Domínios](dominios.md) · [↑ Índice](../README.md) · [Entidades →](../02-informacao/modelo-conceitual.md)

Processos são descritos **sem ferramenta ou mecanismo técnico**. Os diagramas representam o fluxo esperado, não uma automação já existente.

## PROC-001 — Fabricação e registro

```mermaid
flowchart TD
 A[Produção finaliza registro e testes] --> B{Liberado por qualidade?}
 B -->|Não| C[Registrar pendência e retrabalho]
 B -->|Sim| D[Confirmar identidade corporativa]
 D --> E[Registrar evento dispositivo fabricado]
 E --> F[Disponibilizar registro para histórico]
 E --> G[Solicitar provisionamento OTA]
 G --> H{Confirmado?}
 H -->|Sim| I[Provisionamento concluído]
 H -->|Não| J[Pendência rastreável e recuperação]
```

Ver [E01](../exemplos/E01-registro-producao.md).

## PROC-002 — Expedição, recebimento e faturamento

```mermaid
flowchart TD
 A[Registrar expedição] --> B[Confirmar recebimento com data e evidência]
 B --> C[Consultar contrato e condição comercial]
 C --> D{Elegível para faturamento?}
 D -->|Sim| E[Disponibilizar para Financeiro]
 D -->|Não| F[Manter pendência justificada]
 E --> G[Financeiro registra emissão de NF]
```

Ver [E02](../exemplos/E02-entrega-faturamento.md).

## PROC-003 — Ocorrências e serviços

```mermaid
flowchart TD
 A[Técnico registra ocorrência vinculada ao ativo] --> B[Triagem e diagnóstico]
 B --> C{Requer ação?}
 C -->|Não| D[Encerrar com justificativa]
 C -->|Sim| E[Abrir/associar ordem de serviço]
 E --> F[Planejar e executar intervenção]
 F --> G[Registrar alteração de configuração e peças, se houver]
 G --> H[Validar efetividade e registrar custos]
 H --> I[Encerrar ou reabrir]
```

Ver [E06](../exemplos/E06-ocorrencias-os.md).

## PROC-004 — Suprimentos até consumo

```mermaid
flowchart TD
 A[Necessidade de material] --> B[Pedido de compra]
 B --> C[Recebimento e identificação de lote]
 C --> D{Conforme?}
 D -->|Não| E[Quarentena / não conformidade]
 D -->|Sim| F[Liberar para estoque]
 F --> G[Separar para produção ou serviço]
 G --> H[Registrar consumo por dispositivo/intervenção]
 H --> I[Rastrear origem e custo]
```

Ver [E08](../exemplos/E08-suprimentos-rastreabilidade.md).

## Catálogo inicial de regras

| Regra | Enunciado |
|---|---|
| RN-001 | Nenhum dispositivo físico pode receber duas identidades corporativas ativas. |
| RN-002 | Números de série, MAC, IDs de Jira e OTA são identificadores externos; não substituem a identidade corporativa. |
| RN-003 | Dispositivo fabricado e provisionamento OTA são situações distintas; falha de OTA gera pendência, não novo dispositivo. |
| RN-004 | Recebimento requer evento datado, origem/responsável e evidência apropriada. |
| RN-005 | Elegibilidade para NF depende de condição contratual definida e validada; entrega não implica cobrança universalmente. |
| RN-006 | Cada alocação possui início, fim opcional e histórico; alterações não apagam alocações anteriores. |
| RN-007 | Configuração experimental exige autorização, objetivo, vigência, referência e possibilidade de identificar os dispositivos afetados. |
| RN-008 | Ocorrência, diagnóstico, OS, intervenção e validação são entidades distintas; permitem relações N:N onde necessário. |
| RN-009 | Estado operacional, logístico, financeiro, de qualidade e de comunicação não são um único status. |
| RN-010 | Sem comunicação não prova defeito: distinguir indisponível, desconhecido e não aplicável. |
| RN-011 | Consumo de componente vincula lote/serial, dispositivo ou OS, quantidade, momento e responsável. |
| RN-012 | Material sob não conformidade não pode ser tratado como liberado. |
| RN-013 | Eventos têm momento real, momento de registro e origem; atraso de conectividade é suportado. |
| RN-014 | Processos entre sistemas precisam indicar sucesso parcial, repetição segura, reconciliação e pendências. |

**Decisões em aberto:** regras fiscais por contrato, autoridade de confirmação de entrega, política de série/lote para componentes e fluxos de aprovação de modificações.

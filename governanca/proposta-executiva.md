# Proposta executiva — decisão para o CEO

[← Índice principal](../README.md)

## Decisão solicitada

**Aprovar a diretriz e a fase de detalhamento da Arquitetura Corporativa de Integração**, orientada a processos e informações comuns, preservando os sistemas especializados enquanto a necessidade de alteração é avaliada.

**Esta aprovação não significa autorizar implantação, aquisição, substituição de ferramentas ou orçamento técnico.** Isso exigirá plano posterior, estimativa e aprovação específica.

## Situação atual e impacto operacional

| Problema observado | Impacto | Resposta arquitetural |
|---|---|---|
| Mesmo item registrado no Jira, Confluence e OTA | Retrabalho, divergência de cadastro, tempo administrativo | Identidade única e processo de registro com integrações rastreáveis |
| Financeiro busca entrega e instalação manualmente | Dependência entre áreas, risco de atraso de NF | Eventos logísticos, contrato e elegibilidade financeira |
| Cliente sem visão integrada do parque | Falta de visibilidade de operação e custo | Consulta corporativa 360° |
| Equipamento sem centro de custo histórico | Dificulta rateio e responsabilização | Alocação temporal por cliente, unidade, contrato e CC |
| Testes em campo com mudanças pouco visíveis | Risco técnico e comparabilidade de resultados | Gestão de configuração individual e campanhas |
| Ocorrências e OS desconectadas do ativo | Perda de causa, ação, custo e efetividade | Fluxo ocorrência→OS→intervenção→validação |
| Telemetria heterogênea | Diagnóstico fragmentado por projeto | Modelo comum de contexto + extensão por produto |
| Rastreabilidade de materiais incompleta | Análise de lote e impacto em campo prejudicada | Suprimentos→qualidade→consumo→dispositivo |

## Objetivos de negócio

- Reduzir registros redundantes e conciliação manual.
- Aumentar rastreabilidade do ativo durante todo o ciclo de vida.
- Melhorar previsibilidade do faturamento ligado ao recebimento.
- Dar visão agregada por cliente, unidade, centro de custo, produto e equipamento.
- Localizar configurações experimentais, lotes e intervenções.
- Permitir inclusão de produtos e áreas sem reconstruir a arquitetura central.

## Resultados a comprovar na aprovação do desenho

1. Simular o registro único de DEV-00284 com falha parcial no OTA.
2. Consultar itens elegíveis para NF por cliente/contrato e data de recebimento.
3. Navegar cliente → CC → equipamento → saúde → observação original.
4. Reconstruir localização, composição e configuração na data de uma ocorrência.
5. Localizar dispositivos afetados por um lote de componente não conforme.
6. Demonstrar inclusão de novo produto com esquema de telemetria diferente.

## Benefícios e métricas de acompanhamento — sem metas inventadas

| Métrica | Linha de base a medir | Possível medida de efeito |
|---|---|---|
| Registros manuais por dispositivo | Número atual | Redução no novo processo |
| Tempo de cadastro e provisionamento | Tempo atual | Tempo de ciclo e retrabalho |
| Tempo para identificar itens elegíveis à NF | Tempo atual | Tempo até lista verificável |
| Percentual de ativos com identidade consistente | Taxa atual | Taxa de conciliação |
| Percentual de modificações com histórico | Taxa atual | Cobertura de configuração |
| Tempo de diagnóstico de ocorrência | Tempo atual | Tempo entre triagem e resolução |
| Rastreabilidade de lote até clientes | Cobertura atual | Percentual rastreável |

## Condições de aprovação

Solicita-se validar: (a) escopo dos 8 UCs, incluindo Suprimentos e excluindo RH; (b) patrocínio executivo e responsáveis por domínio; (c) mandato para levantar processos e fontes; (d) método TOP-DOWN; (e) gates antes de decisões tecnológicas.

[Roadmap e gates](roadmap-aprovacao.md) · [Riscos e princípios](principios-riscos.md).

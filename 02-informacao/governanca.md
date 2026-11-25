# 08 — Governança, fontes oficiais e qualidade

[← Modelo lógico](modelo-logico.md) · [↑ Índice](../README.md) · [Serviços →](../03-integracao/servicos.md)

## Princípio

A fonte oficial de um atributo não é necessariamente onde o usuário o consulta. Atribuir **responsabilidade de negócio**, **custódia técnica**, **autoridade de escrita** e **permissão de leitura** separadamente.

## Matriz de fonte oficial — hipóteses de trabalho

| Informação | Domínio de autoridade | Sistema atual/candidato | Status |
|---|---|---|---|
| Identidade corporativa do ativo | Gestão de ativos | A definir | **Em aberto** |
| Fabricação e testes | Produção | Jira | A validar |
| Procedimento e especificação | Engenharia | Confluence | A validar |
| Versão de firmware aprovada | Engenharia | Repositório/release | A validar |
| Provisionamento OTA | Operação | Servidor OTA | A validar |
| Versão reportada pelo ativo | Operação | Telemetria (GBQ) | A validar |
| Telemetria detalhada | Operação | BigQuery | A validar |
| Alocação e centro de custo | Gestão de ativos / Comercial | A definir | **Em aberto** |
| Evento de recebimento em campo | Logística / Serviços | A definir | **Em aberto** |
| Ocorrência e OS | Serviços | Jira ou sistema específico | A validar |
| Modificação aprovada | Engenharia | Jira / documentação técnica | A validar |
| Modificação executada | Serviços | A definir | **Em aberto** |
| Pedido e recebimento de material | Suprimentos | A definir | **Em aberto** |
| Liberação de material | Qualidade | A definir | **Em aberto** |
| NF e faturamento | Financeiro | Sistema financeiro | A validar |

**Não assumir que Jira, Confluence ou OTA serão necessariamente a fonte definitiva**; a matriz deve ser aprovada pelos responsáveis.

## Regras de qualidade e integridade

- **Identidade:** sem duplicidade, crosswalk dos identificadores externos e rejeição de vínculos ambíguos.
- **Completude:** atributos mínimos por evento/entidade com tratamento de exceções.
- **Pontualidade:** distinguir evento ocorrido, evento recebido e dado processado.
- **Consistência:** divergências são auditáveis, não apagadas silenciosamente.
- **Histórico:** relações e configurações temporalmente válidas.
- **Segurança:** menor privilégio; delimitar acesso por área, papel, cliente e finalidade; dados financeiros e pessoais protegidos.
- **Retenção e LGPD:** política por categoria de dados e exigência legal/contratual, ainda a definir.
- **Linhagem:** indicador → transformações → eventos → fonte original.

## Reconciliar integrações

Integrar com sucesso não é apenas "enviar uma mensagem". Para cada integração definir:
1. Identificador único da operação/evento.
2. Repetição idempotente, sem criar ativos duplicados.
3. Reconhecimento de recebimento e resultado final.
4. Estados pendente, concluído, falho e divergente.
5. Forma de reprocessar pendências e registrar correções.
6. Dono operacional e prazo de atendimento.

**Exemplo:** falha no OTA após fabricação gera "provisionamento pendente"; o ativo permanece existente e o sistema aponta a pendência até confirmação.

## Aprovações necessárias

Matriz RACI por domínio, políticas de acesso, fronteiras de responsabilidade, critérios de qualidade, fonte oficial de cada atributo e condições de exceção.

# 03 — Domínios e responsabilidades

[← Capacidades](capacidades.md) · [↑ Índice](../README.md) · [Processos →](processos-regras.md)

**Domínio** = fronteira de responsabilidade do negócio, independentemente da estrutura departamental e das ferramentas.

| Domínio | Detém autoridade sobre | Colabora com |
|---|---|---|
| Gestão de ativos | Identidade corporativa e vínculos estruturais do dispositivo | Todos |
| Engenharia | Projeto, revisão aprovada, modificações técnicas | Produção, Serviços, Qualidade |
| Produção | Registro do executado, montagem, testes | Engenharia, Suprimentos |
| Suprimentos | Fornecedores, pedidos, lotes recebidos, entrada de material | Produção, Qualidade, Financeiro |
| Qualidade | Liberação, não conformidades e validação | Produção, Suprimentos, Serviços |
| Logística | Expedição, recebimento e movimentação física | Comercial, Serviços |
| Comercial | Cliente, contrato e regra comercial | Financeiro, Logística |
| Serviços | Ocorrências, diagnósticos, intervenção e ação executada | Engenharia, Qualidade |
| Operação | Telemetria observada e condição operacional | Serviços, Engenharia |
| Financeiro | Faturamento, custos, receitas e baixa financeira | Comercial, Logística |

## Autoridade não é necessariamente armazenamento

- O **Jira** pode registrar a fabricação, mas a **identidade corporativa** deve ter uma autoridade lógica própria.
- A **Engenharia** aprova uma configuração; a **Produção** registra a configuração efetivamente fabricada; **Serviços** registra mudanças em campo; **Operação** observa a versão realmente reportada pelo dispositivo.
- **Suprimentos** registra o lote entregue pelo fornecedor; **Qualidade** determina sua liberação; **Produção** registra seu consumo.
- **Comercial** define condição contratual; **Financeiro** controla o documento fiscal. Um evento de entrega não deve emitir NF automaticamente sem atender às regras aprovadas.

## Exceções e conflitos

Definir matriz RACI antes da implementação. Quando dois domínios discordam, preservar ambos os registros originais, abrir divergência e indicar a autoridade do atributo. Nenhum consumidor deve sobrescrever a fonte oficial silenciosamente.

[Veja fontes candidatas e validações pendentes](../02-informacao/governanca.md).

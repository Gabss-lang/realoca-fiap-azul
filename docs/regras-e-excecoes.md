# Regras e exceções - Realoca

A modelagem da Sprint 1 descreve **11 regras**, agrupadas em três funcionalidades.

| Regra | Resumo |
| --- | --- |
| R1 | Registrar motivo da retenção: peso, cubagem ou menor prioridade; combinar motivos quando aplicável |
| R2 | Somar 1 voo perdido às cargas de prioridade Média/Baixa que ficam fora do voo previsto |
| R3 | Pontuar: +10 por voo perdido, +30 se SLA inferior a 12h ou +15 se inferior a 24h; +10 para prioridade Média; desempate pelo SLA |
| R4 | Com 3 voos perdidos, sinalizar carga crítica e destacá-la na fila |
| R5 | Reservar 30% do peso livre do voo às cargas de prioridade Alta |
| R6 | Liberar a reserva não usada 30 minutos antes do fechamento do voo |
| R7 | Validar disponibilidade de peso, cubagem e prazo antes de confirmar |
| R8 | Encaixar pela ordem de pontuação; regra especial de uso da reserva para cargas críticas |
| R9 | Atualizar capacidade do voo de destino após efetivação do remanejamento |
| R10 | Exigir motivo e comentário com pelo menos 20 caracteres; status em aguardo -> pendente -> remanejada |
| R11 | Registrar operador, horário, voos de origem/destino e pontuação; registro não editável |

## Exceções

- **E1 - Peso:** bloquear voo quando a carga excede o peso disponível para represadas.
- **E2 - Cubagem:** bloquear quando o volume da carga excede a cubagem livre.
- **E3 - SLA em risco:** informar impossibilidade temporal e permitir escalonamento ao supervisor.
- **E4 - Justificativa:** impedir conclusão sem motivo e comentário válido.

**Nota de coerência:** SLA é o prazo máximo de *chegada a Recife*, não apenas o fechamento do voo. O modelo deve ter previsão de chegada ao terminal para validar esse prazo de forma completa. Sem essa informação, não se comprova cumprimento de SLA.

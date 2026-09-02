# Testes Exploratórios

## Objetivo

Os testes exploratórios foram realizados com o objetivo de investigar comportamentos não contemplados nos requisitos, utilizando exploração baseada em regras de negócios, observação da aplicação e levantamento de possíveis riscos. 

ID | Área | Charters/Objetivo | Resultado | Bug | Notas 
-|-|-|-|-|-|
TE001 | Novo Agendamento | Verificar se o sistema permite agendamento em horário retroativo. | O sistema permitiu realizar um agendamento em horário retroativo.| B006 | Embora o RF004.4 estabeleça apenas a rejeição de datas passadas, o sistema permite o registro de um horário anterior ao momento atual. O comportamento pode gerar inconsistências nos dados e nos agendamentos. Recomenda-se avaliar a necessidade de validação do horário quando a data selecionada corresponde ao dia atual.
TE002 | Filtro de Agendamento | Verificar se o sistema exibe somente os agendamentos que atendem simultaneamente aos critérios selecionados. | O sistema exibiu somente os agendamentos que atendiam simultaneamente aos critérios selecionados. | - | Comportamento avaliado durante a exploração da funcionalidade de filtros.
TE003 | Reagendamento | Verificar se o sistema permite reagendamento para horário retroativo. | O sistema permitiu realizar o reagendamento para um horário retroativo. | B007 | Permitir o reagendamento para um momento já decorrido pode gerar inconsistências nos dados e no fluxo de atendimento. Recomenda-se avaliar a necessidade de validação do horário quando a data selecionada corresponde ao dia atual.


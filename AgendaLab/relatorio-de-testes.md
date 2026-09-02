# Relatório de Testes 

## 1. Informações Gerais
- Nome do Projeto: AgendaLab
- Versão Avaliada: v1.0.0 
- Ambiente de Testes: https://agendalabqa.vercel.app/
- Tipo de Teste: Teste Manual Funcional
- Período de execução: 18/08/2026 a 31/08/2026
- Responsável: Dalila Xavier


## 2. Objetivo dos Testes
- O objetivo dos testes foi validar as principais funcionalidades do sistema AgendaLab e identificar inconsistências, garantindo que as funcionalidades estejam de acordo com os requisitos definidos na documentação. 


## 3. Escopo dos Testes
**Dentro do Escopo:**

- Autenticação de Usuários.
- Dashboard.
- Catálogo de Serviços.
- Novo agendamento.
- Listagem de Meus Agendamentos.
- Filtros de Agendamentos.
- Cancelamento de Agendamento.
- Reagendamento.
- Navegação e Layout.
- Reset de Dados de Teste.
- Persistência de Dados.
- Validação de Disponibilidade de Horário.
- Acessibilidade e Responsividade.

**Fora do Escopo:**

- Página de Requisitos do Sistema.


## 4. Ambiente de Testes

- Sistema operacional: Windows 10.
- Navegador: Google Chrome - Versão: 151.0.7922.110.
- Ferramentas: DevTools, Local Storage, VS Code, Snipping Tool.
- Resolução: Desktop/Mobile.


## 5. Resumo da Execução: 

| Métrica                 | Resultado |
 ------------------------ | --------: |
Casos de teste definidos  |        86 | 
Casos de teste executados |        83 | 
Passaram                  |        79 | 
Falharam                  |        04 |
Bloqueados                |        03 |
Bugs identificados        |        06 |
Testes exploratórios      |        03 |
Requisitos avaliados      |        13 |

**Resumo por requisito:**

| Requisito | Casos | Passaram | Falharam | Bloqueado |
| --------- | ----: | -------: | -------: | --------: |
| RF001     |    15 |       14 |       01 |        00 |
| RF002     |    05 |       04 |       01 |        00 |
| RF003     |    03 |       03 |       00 |        00 |
| RF004     |    15 |       15 |       00 |        00 |
| RF005     |    06 |       05 |       00 |        01 | 
| RF006     |    10 |       09 |       00 |        01 |
| RF007     |    05 |       04 |       00 |        01 | 
| RF008     |    04 |       04 |       00 |        00 | 
| RF010     |    09 |       09 |       00 |        00 |
| RF011     |    03 |       02 |       01 |        00 |
| RF012     |    04 |       04 |       00 |        00 |
| RF013     |    03 |       03 |       00 |        00 |
| RF014     |    04 |       03 |       01 |        00 |

**Testes exploratórios:**

Charters | Módulos                                                        | Bugs           |
-------- |--------------------------------------------------------------- |--------------- | 
03       | Novo Agendamento <br> Reagendamento <br> Filtro de Agendamento | B005 <br> B006 |


## 6. Resumo dos bugs reportados

ID  | Título                                                            | Severidade | Prioridade |
--- |------------------------------------------------------------------ |------------|------------|
B001 | Página em branco após login com usuário de perfil Lentidão        | Alta       | Alta       |
B002 | Total de agendamento com status CONCLUÍDO não é exibido           | Alta       | Alta       |
B003 | O sistema não é restaurado automaticamente para os dados iniciais | Média      | Baixa      |
B004 | Contraste inferior a 4.5:1 em alguns elementos do Dashboard       | Média      | Média      |
B005 | Agendamento com horário passado                                   | Média      | Média      |
B006 | Reagendamento com horário passado                                 | Média      | Média      |


## 7. Métricas

**Casos executados:**

| Status                 | Quantidade | Percentual |
 ------------------------| --------:  | ---------: |
Passaram                 |         79 |     95,18% |
Falharam                 |         04 |      4,82% |

**Casos bloqueados:**
| Status                 | Quantidade | Percentual |
 ------------------------| --------:  | ---------: |
Bloqueados               |         03 |      3,49% |


## 8. Evidências

- analise-de-requisitos (Markdown).
- plano-de-testes (Markdown).
- cenarios-de-testes/.
- testes-exploratorios/.
- relatorio-de-bugs (Markdown).
- evidencias (.png e .mp4).
- relatorio-de-testes (Markdown).


## 9. Análise e Riscos

Os testes realizados demonstraram que a maioria das funcionalidades avaliadas apresentou comportamento conforme especificado. Entretanto, foram identificados problemas relacionados aos agendamentos com status CONCLUÍDO, impossibilitando a validação de alguns cenários e resultando em casos de teste com status BLOQUEADO. Também foram identificadas falhas nas funcionalidades de reset dos dados de demonstração e no contraste de alguns elementos da interface.
 

## 10. Conclusão

O AgendaLabs apresentou comportamento adequado na maior parte das funcionalidades avaliadas. Entretanto, foram identificados defeitos com alta e média severidade, que demonstram que existem pontos que devem ser corrigidos ou avaliados antes de considerar o sistema plenamente aderente aos requisitos e critérios de qualidade definidos.
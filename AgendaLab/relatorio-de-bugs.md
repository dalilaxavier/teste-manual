# Relatório de Bugs

- Sistema: AgendaLabs
- Navegador: Google Chrome
- Sistema Operacional: Windows 10
- Data: 25/08/2026
- Responsável: Dalila Xavier do Nascimento

## Bug Reportados:

### B001: Página em branco após login com usuário de perfil Lentidão

ID | Requisito Associado | Cenário associado | Caso de Teste | Severidade | Prioridade | Passos para reproduzir | Resultado esperado | Resultado Obtido | Evidência
-|-|-|-|-|-|-|-|-|-|
B001 | 1. RF001.5 <br> 2. RF001.9 | Cenário de Teste 01 (C001): Autenticação com sucesso | CT003 - Login de usuário com perfil com lentidão | Alta | Alta | 1. Informar usuário válido. <br> 2. Informar senha válida. <br> 3. Clicar em "Entrar". <br> 4. Observar o carregamento. <br> 5. Acessar o DevTools. <br> 6. Consultar o localStorage. | O sistema deve apresentar um delay de 2 segundos durante o carregamento. Após carregamento, o usuário deve ser redirecionado para o Dashboard e uma sessão deve ser criada no localStorage. | O sistema apresentou um tempo de carregamento próximo de 2 segundos. Após o carregamento, apresentou uma página em branco e não redirecionou para o Dashboard. No entanto, a sessão foi criada corretamente no localStorage. | [Evidência](evidencias/b001.mp4) <br> [Evidência-02](evidencias/b001-ev02.png)


### B002: Total de agendamentos com status CONCLUÍDO não é exibido

ID | Requisito Associado | Cenário associado | Caso de Teste | Severidade | Prioridade | Passos para reproduzir | Resultado esperado | Resultado Obtido | Evidência
-|-|-|-|-|-|-|-|-|-|
B002 | 1. RF002.2 | Cenário de Teste 01 (C001): Total de status de agendamentos |  CT002 - Total de agendamento com status CONCLUÍDO | Alta | Alta | 1. Identificar a quantidade de agendamentos com status CONCLUÍDO. <br> 2. Verificar o total de agendamentos concluídos exibido no Dashboard. | O sistema deve exibir o total de agendamentos com status CONCLUÍDO. | O sistema não exibiu o total de agendamentos com status CONCLUÍDO. | [Evidência-01](evidencias/b002-ev01.png) <br> [Evidência-02](evidencias/b002-ev02.png)

### B003: O sistema não é restaurado automaticamente para os dados iniciais

ID | Requisito Associado | Cenário associado | Caso de Teste | Severidade | Prioridade | Passos para reproduzir | Resultado esperado | Resultado Obtido | Evidência
-|-|-|-|-|-|-|-|-|-|
B003 | RF011.2 | Cenário de Teste 01 (C001): Reset de dados com sucesso | CT002 - Reset dos dados de demonstração | Média | Baixa | 1. Clicar em "Resetar Dados".<br> 2. Observar o comportamento do sistema. | O sistema deve retornar imediatamente ao estado inicial de demonstração após o reset. | Após o reset, o sistema continuou apresentando os agendamentos realizados. Para que o estado inicial seja exibido, é necessário atualizar a página. | [Evidência-01](evidencias/b003-ev01.mp4)

### B004: Contraste inferior a 4.5:1 em alguns elementos do Dashboard

ID | Requisito Associado | Cenário associado | Caso de Teste | Severidade | Prioridade | Passos para reproduzir | Resultado esperado | Resultado Obtido | Evidência
-|-|-|-|-|-|-|-|-|-|
B004 | RF014.2  | Cenário de Teste 02 (C002): Contraste necessário | CT002 - Contraste entre texto e fundo | Média | Média | 1. Acessar o DevTools do navegador. <br> 2. Acessar a sessão Elements. <br> 3. Selecionar um elemento que contenha texto. <br> 4. Identificar as cores do texto e do fundo. <br> 5. Verificar a proporção de contraste apresentada pelo DevTools. | O contraste entre o texto e o fundo deve ser igual ou superior a 4.5:1. | A maioria dos elementos que contêm texto apresenta contraste superior a 4.5:1. Entretanto, os textos "Agende um Serviço", "Gerencie seus agendamentos" e "Serviços" localizados nos atalhos no Dashboard, apresentam inferior a 4.5:1. | [Evidência-01](evidencias/b004-ev01.png) <br> [Evidência-02](evidencias/b004-ev02.png) <br> [Evidência-03](evidencias/b004-ev03.png)

### B005: Agendamento com horário passado

ID | Requisito Associado | Cenário associado | Caso de Teste | Severidade | Prioridade | Passos para reproduzir | Resultado esperado | Resultado Obtido | Evidência
-|-|-|-|-|-|-|-|-|-|
B005 | - | Teste Exploratório TE001 | - | Média | Média | 1. Informar nome válido. <br> 2. Informar telefone válido. <br> 3. Selecionar um serviço. <br> 4. Selecionar um profissional.  <br> 5. Informar uma data válida. <br> 6. Informar horário passado. <br> 7. Informar uma observação válida.  <br> 8. Clicar em "Confirmar Agendamento". | O sistema não deveria permitir o registro de um agendamento para um horário já decorrido. | O sistema permitiu o registro de um agendamento para um horário já decorrido. | [Evidência-01](evidencias/b005-ev01.mp4) <br> [Evidência-02](evidencias/b005-ev02.mp4)

### B006: Reagendamento com horário passado

ID | Requisito Associado | Cenário associado | Caso de Teste | Severidade | Prioridade | Passos para reproduzir | Resultado esperado | Resultado Obtido | Evidência
-|-|-|-|-|-|-|-|-|-|
B006 | - | Teste Exploratório TE003 | - | Média | Média | 1. Clicar em reagendar. <br> 2. Selecionar um horário. <br> 3. Clicar em "Confirmar Reagendamento". | O sistema não deveria permitir o reagendamento para um horário já decorrido. | O sistema permitiu o reagendamento para um horário já decorrido. | [Evidência-01](evidencias/b006-ev01.mp4) <br> [Evidência-02](evidencias/b006-ev02.mp4)

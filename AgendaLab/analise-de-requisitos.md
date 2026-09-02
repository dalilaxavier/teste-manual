# Análise de Requisitos

## RF001 - Autenticação de Usuários

**Descrição:** O sistema deve controlar o acesso de usuários por meio de credenciais de login, suportando perfis de usuários com comportamentos diferentes. 

**Funcionalidades esperadas:**

- RF001.1 - O sistema deve exibir a tela de login antes do acesso a qualquer funcionalidade protegida.
- RF001.2 - Os campos vazios devem exibir mensagem de erro de campos obrigatórios. 
- RF001.3 - Os campos com credenciais inválidas devem exibir mensagem de erro genérica. 
- RF001.4 - Usuários com status BLOCKED não devem conseguir autenticar-se no sistema. 
- RF001.5 - O sistema deve autenticar usuário válido, criando uma sessão utilizando o localStorage e redirecionar para o Dashboard.
- RF001.6 - O sistema deve manter a sessão do usuário autenticada após o recarregamento da página.
- RF001.7 - Ao realizar logout, o sistema deve remover a sessão do usuário e redirecioná-lo para a tela de login. 
- RF001.8 - O sistema deve impedir o acesso às páginas protegidas quando não existir uma sessão, redirecionando o usuário para a tela de login. 
- RF001.9 - O sistema deve aplicar um delay de 2 segundos nas operações de carregamento para usuários com perfil Lentidão.

**Observações:**

- Não foi informada a mensagem exata que deve ser exibida ao deixar os campos obrigatórios em branco ou ao inserir credenciais inválidas.

---

## RF002 - Dashboard

**Descrição:** O sistema deve exibir um painel inicial contendo um resumo dos agendamentos do usuário autenticado e os atalhos de navegação.

**Funcionalidades esperadas:**

- RF002.1 - O sistema deve exibir o total de agendamentos com o status CONFIRMADO. 
- RF002.2 - O sistema deve exibir o total de agendamentos com o status CONCLUÍDO. 
- RF002.3 - O sistema deve exibir o total de agendamentos com o status CANCELADO. 
- RF002.4 - O sistema deve exibir atalhos para as funcionalidades Serviços, Novo Agendamento e Meus agendamentos.
- RF002.5 - O sistema deve exibir o nome do usuário autenticado.

---

## RF003 - Catálogo de Serviços

**Descrição:** Na página de serviços, o sistema deve exibir todos os serviços disponíveis com as informações pertinentes, permitindo realizar um agendamento.

**Funcionalidades esperadas:** 

- RF003.1 - O sistema deve exibir os seis serviços cadastrados contendo nome, categoria, duração e profissionais vinculados. 
- RF003.2 - O sistema deve organizar os serviços por categorias: Saúde, Educação, Esporte e Bem-estar. 
- RF003.3 - O sistema deve permitir que ao clicar no botão Agendar o usuário seja redirecionado para o formulário com o serviço pré-selecionado.

---

## RF004 - Novo Agendamento

**Descrição:** O formulário de novo agendamento deve permitir criar uma reserva com todas as validações de negócios aplicadas.

**Funcionalidades esperadas:** 

- RF004.1 - Os campos nome, telefone, serviço, profissional, data e horário são obrigatórios.
- RF004.2 - O campo telefone deve aceitar apenas dígitos, parênteses, espaços e hífens.
- RF004.3 - O campo observação é limitado a 200 caracteres. 
- RF004.4 - O sistema não deve aceitar data passada.
- RF004.5 - O sistema deve rejeitar agendamento aos Domingos.
- RF004.6 - O sistema deve exibir apenas horários válidos: 08h, 09h, 10h, 11h, 13h, 14h, 15h, 16h, 17h.
- RF004.7 - O sistema deve rejeitar conflito de horário (mesmo profissional, data e horário confirmado).
- RF004.8 - Ao criar agendamento com status CONFIRMADO, deve ser exibida uma confirmação de sucesso. 

**Observações:**

A documentação não especifica o comportamento do sistema ao:
- Deixar um dos campos obrigatórios vazios. 
- Informar um telefone com caracteres não permitidos.
- Agendar com horário passado.
- Conflito de horário do usuário ao agendar um serviço para o mesmo horário, mas para diferentes profissionais.

A especificação não define a mensagem ou o comportamento apresentado ao tentar agendar em uma data passada, aos domingos ou em um horário que já tenha passado na data selecionada.

---

## RF005 - Listagem de Meus Agendamentos

**Descrição:** O sistema deve permitir que a página de listagem de agendamentos exiba todos os agendamentos do usuário em cards com ações disponíveis conforme o status. 

**Funcionalidades esperadas:** 

- RF005.1 - Os agendamentos do usuário devem ser exibidos em cards.
- RF005.2 - Os cards devem exibir os dados: serviço, profissional, data, horário, status, cliente, telefone e observações.
- RF005.3 - Os agendamentos com status CONFIRMADO devem exibir os botões Cancelar e Reagendar.
- RF005.4 - Os agendamentos com status CANCELADO e CONCLUÍDO não devem exibir o botão Cancelar.
- RF005.5 - Todos os cards devem apresentar o botão Detalhes.

**Observações:**

- A especificação não informa o conteúdo apresentado ao clicar no botão Detalhes. 
- Também não é informado o conteúdo da página quando não existem agendamentos para o usuário.

---

## RF006 - Filtro de Agendamentos

**Descrição:** O sistema permite que o usuário filtre os agendamentos por status, serviço, profissional e intervalo de datas.

**Funcionalidades esperadas:** 

- RF006.1 - O usuário pode filtrar os agendamentos por: status, serviço, profissional, data inicial e final.
- RF006.2 - O filtro de status deve exibir somente os agendamentos com status correspondente. 
- RF006.3 - O filtro de datas deve conter as datas limites (início e fim).
- RF006.4 - Deve ser restaurado a listagem completa ao limpar filtros.

**Observações:**

- A documentação não especifica o que acontece ao selecionar mais de um filtro.
- Não é especificado o que acontece ao definir somente uma data inicial ou final no filtro por data. 
- A especificação não define o comportamento quando a data inicial é posterior à data final.

---

## RF007 - Cancelamento de Agendamento

**Descrição:** O sistema deve permitir que um agendamento com status CONFIRMADO possa ser cancelado com antecedência mínima de 2 horas. 

**Funcionalidades esperadas:** 

- RF007.1 - O usuário deve conseguir cancelar um agendamento confirmado com 2 horas ou mais de antecedência.
- RF007.2 - Cancelamento com menos de 2 horas de antecedência deve ser rejeitado e apresentar mensagem de erro.
- RF007.3 - Agendamento com status CONCLUÍDO não pode ser cancelado.
- RF007.4 - Agendamento com status CANCELADO não pode ser cancelado novamente.

**Observações:**

- O sistema não especifica a mensagem de erro que aparece ao realizar o cancelamento do agendamento com menos de 2 horas de antecedência.

---

## RF008 - Reagendamento

**Descrição:** O sistema deve permitir que um agendamento com status CONFIRMADO possa ser reagendado para nova data e horários válidos.

**Funcionalidades esperadas:** 

- RF008.1 - O sistema deve apresentar o formulário de reagendamento pré-preenchido com os dados atuais.
- RF008.2 - O sistema deve aplicar ao reagendamento as mesmas validações definidas para a funcionalidade Novo Agendamento (RF004).
- RF008.3 - A nova data e horário devem ser confirmados no localStorage.
- RF008.4 - Ao cancelar a operação de reagendamento, o sistema deve retornar à tela sem alterar o agendamento original.

**Observações:**

- A especificação não informa o comportamento do sistema ao reagendar para um horário passado. 

---

## RF009 - Página de Requisitos do Sistema

Fora do Escopo.

---

## RF010 - Navegação e Layout

**Descrição:** O sistema deve possuir um menu de navegação persistente e um layout responsivo.

**Funcionalidades esperadas:** 

- RF010.1 - O menu deve disponibilizar links para todas as páginas principais enquanto o usuário estiver autenticado.
- RF010.2 - O sistema deve exibir página com erro 404 para rotas inexistentes, com link de retorno para o Dashboard.
- RF010.3 - O layout deve ser responsivo e compatível com desktop e mobile.

---

## RF011 - Reset de Dados de Teste

**Descrição:** O sistema deve permitir que o botão de reset limpe o LocalStorage e restaure o estado inicial.

**Funcionalidades esperadas:** 

- RF011.1 - Ao clicar no botão de reset, o sistema deve limpar todos os agendamentos do localStorage.
- RF011.2 - Ao clicar no botão de reset, os dados iniciais de demonstração devem ser restaurados.
- RF011.3 - Deve ser apresentada uma mensagem de sucesso após o reset. 

**Observações:**

- Não é especificado a mensagem de sucesso que aparece ao resetar o sistema. 

---

## RF012 - Persistência de Dados

**Descrição:** O sistema deve permitir que todos os agendamentos persistidos sejam armazenados no localStorage e recuperados ao recarregar a página. 

**Funcionalidades esperadas:** 

- RF012.1 - Alterações realizadas nos agendamentos são persistidas imediatamente no localStorage.
- RF012.2 - Os dados persistidos no localStorage devem ser recuperados corretamente após o recarregamento da página.
- RF012.3 - A serialização e desserialização dos dados em JSON devem garantir a integridade dos dados.

---

## RF013 - Validação de Disponibilidade de Horário

**Descrição:** O sistema deve verificar e indicar visualmente os horários ocupados por um profissional em uma data selecionada.

**Funcionalidades esperadas:** 

- RF013.1 - O sistema deve verificar agendamentos com status CONFIRMADO do profissional na data selecionada.
- RF013.2 - O sistema deve indicar visualmente horários indisponíveis.
- RF013.3 - O sistema não deve permitir agendamento em horários indisponíveis.

---

## RF014 - Acessibilidade e Responsividade

**Descrição:** O sistema deve suportar leitores de tela básicos, possuir contraste adequado e deve ser utilizável via teclado.

**Funcionalidades esperadas:** 

- RF014.1 - O sistema deve ter atributos ARIA nos principais elementos interativos.
- RF014.2 - O sistema deve apresentar um contraste mínimo de 4.5:1 entre texto e fundo.
- RF014.3 - O Layout deve ser funcional a partir de 320px de largura. 
- RF014.4 - A navegação deve ser possível por teclado (Tab e Enter) nos formulários e botões de ação.



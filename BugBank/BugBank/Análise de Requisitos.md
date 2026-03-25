# Análise de Requisitos

### RF01 - Login

**Descrição:** O sistema deve permitir que o usuário realize login ao preencher os campos obrigatórios corretamente.

**Funcionalidades Esperadas:**
- O campo E-mail é obrigatório.
- O campo Senha é obrigatório.
- Tentativa de acesso sem preencher os campos obrigatórios, o sistema deve exibir a mensagem "Usuário e senha precisam ser preenchidos".
- O sistema não deve autorizar o acesso para usuários inválidos.
- Ao preencher os dados corretamente, o sistema deve direcionar o usuário para a página home. 

**Pontos de Atenção:**
- A documentação não define o comportamento do sistema em múltiplas tentativas de login com credenciais inválidas (ex.: bloqueio de usuário, limite de tentativas).
- A documentação não define o comportamento do sistema ao tentar logar com um e-mail inválido.
- A documentação não define se deve ser exibida mensagem de erro ao usuário em caso de credenciais inválidas. 


### RF02 - Cadastro

**Descrição:** O sistema deve permitir o registro de novos usuários

**Funcionalidades Esperadas:**
- O campo Nome, E-mail, Senha, Confirmação de Senha é de preenchimento obrigatório.
- Tentativa de cadastro sem preencher o campo Nome, o sistema deve exibir a mensagem "Nome não pode ser vazio".
- Tentativa de cadastro sem preencher o campo E-mail, o sistema deve exibir a mensagem "Email não pode ser vazio".
- Tentativa de cadastro sem preencher o campo Senha, o sistema deve exibir a mensagem "Senha não pode ser vazio".
- Tentativa de cadastro sem preencher o campo Confirmar Senha, o sistema deve exibir a mensagem "Confirmar senha não pode ser vazio".
- Ao selecionar a opção de "Criar conta com saldo", o sistema deve cadastrar a conta com um saldo de R$ 1.000,00.
- Ao não selecionar a opção de "Criar conta com saldo", o sistema deve cadastrar a conta com um saldo de R$ 0,00.
- Os campos Senha e Confirmar Senha devem ser iguais. 
- Ao realizar o cadastro com sucesso, o sistema deve exibir o número da conta criada. 

**Pontos de Atenção:**
- A documentação não define comportamento do sistema ao tentar cadastrar o mesmo e-mail mais uma vez, regra mínima de senha e nem a mensagem de erro que deve aparecer ao preencher os campos Senha e Confirmar Senha de forma diferente. Além disso, não informa sobre o uso de caracteres especiais (#,$,@) no campo Nome.


### RF03 - Transferência

**Descrição:** O sistema deve permitir que o usuário seja capaz de enviar e receber dinheiro. 

**Funcionalidades Esperadas:**
- O sistema só deve permitir transferência para contas válidas.
- O sistema só deve permitir transferências quando o saldo for igual ou maior que o valor a transferir.
- Tentativa de transferência para conta inválida, o sistema deve exibir a mensagem de erro "Conta inválida ou inexistente".
- O sistema só deve aceitar números no campo Número e Dígito da conta. 
- O campo Descrição é obrigatório.
- O sistema não deve permitir transferências iguais ou menores que 0.
- Transferência realizada com sucesso, o sistema deve exibir a mensagem  "Transferência realizada com sucesso" e debitar o valor da conta. 
- Transferência realizada com sucesso, o sistema deve redirecionar para a tela de Extrato.

**Pontos de Atenção:**
- A documentação não define uma mensagem de erro ao preencher os campos Número da Conta e Dígito com símbolo ou letras. Além disso, não define a mensagem de erro ao tentar realizar transferência com o campo Descrição em branco.
- Na regra de negócio não é definido um limite máximo de valor ou se é possível realizar transferência para conta própria.


### RF04 - Pagamento
- Funcionalidade e documentação em desenvolvimento.


### RF05 - Extrato
**Descrição:** O sistema deve permitir que o usuário visualize seu extrato.

**Funcionalidades Esperadas:**
- O sistema deve exibir o saldo disponível no momento.
- Transações devem exibir: data da transação, tipo (abertura de conta/transferência enviada/transferência recebida).
- Transferências realizadas devem apresentar a cor em vermelho e um sinal de subtração (-).
- Transferências recebidas devem apresentar a cor verde.
- Transações sem comentários devem exibir um hífen (-).

**Pontos de Atenção:**
- A documentação não define se deve ser considerado a hora da transação.
- Existe um conflito de requisitos na documentação, considerando que no requisito Transferência (RF03) deixa claro que os comentários são itens obrigatórios. No entanto, no requisito atual (Extrato - RF05), diz que deve ser apresentado um hífen no extrato para transações sem comentários, o que torna esse ponto confuso. 


### RF06 - Saque
- Funcionalidade e documentação em desenvolvimento.




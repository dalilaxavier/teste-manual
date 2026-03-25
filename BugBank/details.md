## Partição de equivalência

### RF01 - Login

E-mail | Senha | Resultado
-|-|-
Válido | Válido | Login com sucesso
Válido | Vazio | Mensagem de erro
Vazio | Válido | Mensagem de erro
Inválido | Válida | Mensagem de erro
Válido | inválida | Mensagem de erro

Total de caso de teste: 06


### RF02 - Cadastro

Nome | E-mail | Senha | Confirmação Senha | Saldo | Resultado
-|-|-|-|-|
Válido | Válido | Válido | Válido | Marcado | conta criada + SALDO R$ 1000,00 |
Válido | Válido | Válido | Válido | Não marcado | conta criada + SALDO R$ 0,00 |
Vazio | Válido | Válido | Válido |-| Mensagem de erro |
Válido | Vazio | Válido | Válido |-| Mensagem de erro |
Válido | Válido | Vazio | Válido |-| Mensagem de erro |
Válido | Válido | Válido | Vazio |-| Mensagem de erro |
Válido | Válido | Válido | Inválido |-| Mensagem de erro |

CT: 06

### RF03 - Transferência

Técnica de valor limite

Saldo existente | A transferir | Resultado
1000 | 999 | Permite
1000 | 1000 | Permite
1000 | 1001 | Não permite

Técnica de Partição de Equivalência

Conta | Dígito | Saldo | Valor a Transferir | Descrição | Resultado
-|-|-|-|-|-|
Válido | Válido | 1000 | 500 | Não preenchido | Erro de descrição
Válido | Válido | 0 | -1 | Preenchido | Mensagem de erro valor inválido
Válido | Inválido c/ letra | 1000 | 500 | Preenchido | Mensagem de erro "conta inválida ou inexistente"
Inválido c/ letra | válido | 1000 | 500 | Preenchido | Mensagem de erro "conta inválida ou inexistente"
Vazio | válido | 1000 | 500 | Preenchido | Mensagem de erro "conta inválida ou inexistente"
Válido | Vazio | 1000 | 500 | Preenchido | Mensagem de erro "conta inválida ou inexistente"
Inexistente | Inexistente | 1000 | 500 | preenchido | Mensagem de erro "conta inválida ou inexistente


### RF05 - Extrato

Validação de saldo de extrato
Validação de data disponivel
Validação do tipo de conta
Validação de da cor de transferência (cor vermelha e simbolo de subtração)
Validação de cor de recebimento (cor verde)
Validação de comentários / Sem comentários apresenta o hífen





































































**Caso de Teste 01 (CT01) - Validar login com sucesso**

Descrição: Validar que o sistema autentica corretamente o usuário com credenciais válidas e redireciona para a página inicial

Pré-condição:
1. Usuário cadastrado e ativo no sistema
2. Acesso à página de login

Passo a passo:
1. Acessar a página de login
2. Preencher o campo E-mail com a credencial "teste@teste.com"
3. Preencher o campo Senha com a credencial "teste"
4. Clicar em "Acessar"

Resultado Esperado: Sistema deve autenticar o usuário e redirecionar para a página inicial (Home)

Resultado Obtido: Redirecionamento realizado com sucesso

Status: Passou ✅
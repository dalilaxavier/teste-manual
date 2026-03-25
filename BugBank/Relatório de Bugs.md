# Relatório de Bugs

- Sistema: BugBank
- Navegador: Google Chrome
- Sistema Operacional: Windows 10
- Data: 24/02/2026
- Responsável: Dalila Xavier do Nascimento

## Bugs reportados:

### B01: Mensagem divergente da especificação nos campos de Login 

ID | Cenário associado | Caso de Teste | Severidade | Prioridade | Passos para reproduzir | Resultado esperado | Resultado Obtido | Evidência
-|-|-|-|-|-|-|-|-|
B01 | C01 - Validação do fluxo de Login | CT02 - Validar login com o campo Senha vazio <br> CT03 - Validar login com o campo E-mail vazio <br> CT04 - Validar login com o campo E-mail e Senha vazio | Média | Média | 1. Acessar a tela de Login <br> 2. Executar uma das ações abaixo: <br> - Deixar o campo E-mail vazio <br> - Deixar o campo Senha vazio <br> - Deixar o campo E-mail e Senha vazio <br> 3. Clicar em Acessar | O sistema deve apresentar a mensagem de erro "Usuário e senha precisam ser preenchidos" | O sistema apresentou a mensagem "É campo obrigatório" | [Vídeo 01](https://jam.dev/c/5a783dca-77b2-46a0-9979-75901eb004e7) <br> [Vídeo 02](https://jam.dev/c/259b90b7-0cfe-49bf-8a21-087e8d6db52f) <br> [Vídeo 03](https://jam.dev/c/e4e84e57-5f66-4dfa-8327-59c2e678dd4c) |

---

### B02: Mensagem divergente ao cadastrar com o campo E-mail vazio

ID | Cenário associado | Caso de Teste | Severidade | Prioridade | Passos para reproduzir | Resultado esperado | Resultado Obtido | Evidência
-|-|-|-|-|-|-|-|-|
B02 | C02 - Cadastro de usuário no sistema | CT04 - Validar cadastro com e-mail vazio | Média | Média | 1. Acessar a tela de Cadastro <br> 2. Informar um Nome <br> 3. Informar uma senha <br> 4. Confirmar a senha <br> 5. Clicar em Cadastrar | O sistema deve exibir a mensagem de erro "Email não pode ser vazio" | O sistema exibiu a mensagem "É campo obrigatório" | [Vídeo](https://jam.dev/c/4e18d388-75d1-4a37-bcee-1d7265431266) |

---

### B03: Mensagem divergente ao cadastrar com o campo Senha vazio

ID | Cenário associado | Caso de Teste | Severidade | Prioridade | Passos para reproduzir | Resultado esperado | Resultado Obtido | Evidência
-|-|-|-|-|-|-|-|-|
B03 | C02 - Cadastro de usuário no sistema | CT05 - Validar cadastro com senha vazia | Média | Média | 1. Acessar a tela de Cadastro <br> 2. Informar um e-mail <br> 3. Informar um nome <br> 4. Confirmar a senha <br> 5. Clicar em Cadastrar | O sistema deve exibir a mensagem de erro "Senha não pode ser vazio" | O sistema exibiu a mensagem "É campo obrigatório" | [Vídeo](https://jam.dev/c/4c64f3eb-3b3f-4ca9-9c59-60fcbfff2289) |

---

### B04: Mensagem divergente ao cadastrar com o campo Confirmar senha vazio

ID | Cenário associado | Caso de Teste | Severidade | Prioridade | Passos para reproduzir | Resultado esperado | Resultado Obtido | Evidência
-|-|-|-|-|-|-|-|-|
B04 | C02 - Cadastro de usuário no sistema | CT06 - Validar cadastro com Confirmar senha vazio | Média | Média | 1. Acessar a tela de Cadastro <br> 2. Informar um e-mail <br> 3. Informar um nome <br> 4. Informar uma senha <br> 5. Clicar em Cadastrar | O sistema deve exibir a mensagem de erro "Confirmar Senha não pode ser vazio" | O sistema exibiu a mensagem "É campo obrigatório" | [Vídeo](https://jam.dev/c/04c2320f-2168-4836-834f-bd3408bce9ae) |

---

### B05: Sistema não redireciona o usuário para a tela de extrato após transferência realizada com sucesso

ID | Cenário associado | Caso de Teste | Severidade | Prioridade | Passos para reproduzir | Resultado esperado | Resultado Obtido | Evidência
-|-|-|-|-|-|-|-|-|
B05 | C03 - Validação de Transferência no sistema | CT01 - Validar transferência com o valor de transferência menor que o saldo existente <br> CT02 - Validar transferência com o valor igual que o saldo existente <br> | Alta | Alta | 1. Acessar a tela de Transferência <br> 2. Informar uma conta válida <br> 3. Informar um dígito válido <br> 4. Executar uma das seguintes ações: - Informar o valor de transferência menor que o saldo existente <br> - Informar o valor de transferência igual ao saldo existente <br> 5. Informar a descrição <br> 6. Clicar em Transferir Agora | O sistema deve redirecionar o usuário para a tela de extrato | O sistema não redirecionou o usuário para a tela de extrato | [Vídeo 01](https://jam.dev/c/749010a6-25cc-431c-a448-f7dfb771e605) [Vídeo 02](https://jam.dev/c/2fc28e6d-bbfd-4976-937a-292ca188fde9) |

---

### B06: Sistema permite transferência com campo obrigatório Descrição vazio

ID | Cenário associado | Caso de Teste | Severidade | Prioridade | Passos para reproduzir | Resultado esperado | Resultado Obtido | Evidência
-|-|-|-|-|-|-|-|-|
B06 | C03 - Validação de Transferência no sistema | CT05 - Validar transferência com o campo Descrição em branco | Alta | Alta | 1. Acessar a tela de Transferência <br> 2. Informar uma conta válida <br> 3. Informar um dígito válido <br> 4. Informar o valor de transferência <br> 5. Clica em Transferir Agora | O sistema deve impedir a transferência e exibir uma mensagem de erro informando que é necessário informar a descrição | O sistema permitiu a transferência e exibiu a mensagem "Transferencia realizada com sucesso" | [Vídeo](https://jam.dev/c/fca175e4-5140-46ad-97ed-ff49edd931fb) |

---

### B07: Sistema permite transferência com campo Conta vazio

ID | Cenário associado | Caso de Teste | Severidade | Prioridade | Passos para reproduzir | Resultado esperado | Resultado Obtido | Evidência
-|-|-|-|-|-|-|-|-|
B07 | C03 - Validação de Transferência no sistema | CT06 - Validar transferência com o campo Conta vazio | Alta | Alta | 1. Acessar a tela de Transferência <br> 2. Informar um dígito válido <br> 3. Informar o valor de transferência <br> 4. Informar uma descrição <br> 5. Clica em Transferir Agora | O sistema deve impedir a transferência e exibir uma mensagem de erro informando que a conta deve ser informada | O sistema permitiu a transferência e apresentou a mensagem "Transferencia realizada com sucesso" | [Vídeo](https://jam.dev/c/b54acd95-09f5-4fcd-8b6d-671e770eb1aa) |

---

### B08: Sistema permite transferência com campo Dígito vazio

ID | Cenário associado | Caso de Teste | Severidade | Prioridade | Passos para reproduzir | Resultado esperado | Resultado Obtido | Evidência
-|-|-|-|-|-|-|-|-|
B08 | C03 - Validação de Transferência no sistema | CT07 - Validar transferência com o dígito vazio | Alta | Alta | 1. Acessar a tela de Transferência <br> 2. Informar uma conta válida <br> 3. Informar o valor de transferência <br> 4. Informar uma descrição <br> 5. Clicar em Transferir Agora | O sistema deve impedir a transferência e exibir uma mensagem de erro informando que o dígito deve ser informado | O sistema permitiu a transferência e apresentou a mensagem "Transferencia realizada com sucesso" | [Vídeo](https://jam.dev/c/0f856790-744d-43e9-ac3b-973fe8c7a71eb) |

---

### B09: Mensagem apresentada com erro de concordância e ausência de acentuação

ID | Cenário associado | Caso de Teste | Severidade | Prioridade | Passos para reproduzir | Resultado esperado | Resultado Obtido | Evidência
-|-|-|-|-|-|-|-|-|
B09 | C03 - Validação de Transferência no sistema | CT11 - Validar o comportamento ao transferir para a mesma conta  | Baixa | Baixa | 1. Acessar a tela de Transferência <br> 2. Informar o mesmo número de conta <br> 3. Informar o mesmo número de dígito <br> 4. Informar o valor de transferência <br> 5. Informar uma descrição <br> 6. Clicar em Transferir Agora | O sistema deve impedir a conclusão da transferência e apresentar uma mensagem de erro | Mensagem exibida ao transferir para a mesma conta possui erro de concordância e ausência de acentuação | [Vídeo](https://jam.dev/c/623834ac-6d6c-4fef-b872-43fac84272b0) |

---

### B10: Mensagem técnica exibida ao tentar transferir com valor vazio

ID | Cenário associado | Caso de Teste | Severidade | Prioridade | Passos para reproduzir | Resultado esperado | Resultado Obtido | Evidência
-|-|-|-|-|-|-|-|-|
B09 | C03 - Validação de Transferência no sistema | CT12 - Validar transferência com valor vazio | Média | Alta | 1. Acessar a tela de Transferência <br> 2. Informar uma conta válida <br> 3. Informar o dígito <br> 4. Informar uma descrição <br> 5. Clicar em Transferir Agora | O sistema deve impedir a transferência e apresentar uma mensagem de que o valor deve ser informado | O sistema impediu a transferência e apresentou a mensagem "transferValue must be a `number` type, but the final value was: `NaN` (cast from the value `""`)". Mensagem exibida é técnica e não amigável ao usuário final| [Vídeo](https://jam.dev/c/7d8044d9-43f3-4452-a537-b226928ffa88) |
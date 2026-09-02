# RELATÓRIO DE TESTES

## 1. Informações Gerais
- Nome do Projeto: BugBank
- Versão Avaliada: Demo pública
- Ambiente de Testes: https://bugbank.netlify.app/
- Tipo de Teste: Teste Manual Funcional
- Período de execução: 23/02/2026 a 26/02/2026
- Responsável: Dalila Xavier


## 2. Objetivo dos Testes
- O objetivo dos testes foi validar as principais funcionalidades do sistema BugBank, garantindo que as funcionalidades estejam de acordo com os requisitos definidos na documentação. 


## 3. Escopo dos Testes
Funcionalidades Testadas:
- Login.
- Cadastro.
- Transferência.
- Extrato.


## 4. Métricas
**Resultados da Execução:** 
Total de casos de teste | Passaram | Bugs Reportados
-|-|-|
33 | 21 | 12

---

**Defeitos identificados:**
Bugs reportados | Severidade baixa | Severidade Média | Severidade Alta
-|-|-|-|
12 | 06 | 03 | 03


## 5. Resumo dos Módulos
Módulo RF | Casos Testados | Casos aprovados | Casos reprovados | Bugs Associados
-|-|-|-|-|
RF01 - Login | 06 | 03 | 03 | B01, B02, B03
RF02 - Cadastro | 08 | 05 | 03 | B04, B05, B06 
RF03 - Transferência | 12 | 06 | 06 |  B07, B08, B09, B10, B11, B11
RF04 - Extrato | 07 | 07 | 0 | -

## 6. Resumo dos bugs reportados

ID | Título | Severidade 
-|-|-|
B01 | Mensagem de erro divergente da especificação ao logar com senha vazia | Baixa
B02 | Mensagem de erro divergente da especificação ao logar com e-mail vazio | Baixa
B03 | Mensagem de erro divergente da especificação ao logar com e-mail e senha vazio | Baixa
B04 | Mensagem divergente ao cadastrar com o e-mail vazio | Baixa
B05 | Mensagem divergente ao cadastrar com a senha vazia | Baixa
B06 | Mensagem divergente ao cadastrar com o confirmar senha vazio | Baixa
B07 | Sistema não redireciona o usuário para a tela de extrato após transferência realizada com valor menor que o saldo | Média
B08 | Sistema não redireciona o usuário para a tela de extrato após transferência realizada com valor igual ao saldo | Média
B09 | Sistema permite transferência descrição vazia | Alta
B10 | Sistema permite transferência com conta vazia | Alta
B11 | Sistema permite transferência com dígito vazio | Alta
B12 | Mensagem técnica exibida ao transferir com valor vazio | Média


## 7. Evidências
- Plano de Testes (Markdown).
- Casos de Testes (Markdown).
- Relatório de Bugs (Markdown).
- Evidências em vídeos (Jam.dev).


## 8. Conclusão

- A execução dos testes manuais identificou falhas relevantes em funcionalidades críticas do sistema, principalmente no módulo transferência. Dos 33 casos de testes executados e 12 apresentaram falhas. Recomenda-se a correção dos defeitos reportados antes da liberação do sistema para produção, especialmente aqueles classificados com severidade alta.
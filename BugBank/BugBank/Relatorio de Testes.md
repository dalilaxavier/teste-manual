# RELATÓRIO DE TESTES

## 1. Informações Gerais
- Nome do Projeto: BugBank
- Versão Avaliada: Demo pública
- Ambiente de Testes: https://bugbank.netlify.app/
- Tipo de Teste: Teste Manual Funcional
- Período de execução: 23/02/2026 a 11/03/2026
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
Total de casos de teste | Passaram | Falharam | Bugs Reportados
-|-|-|-|
33 | 21 | 12 | 10

---

**Defeitos identificados:**
Bugs reportados | Severidade baixa | Severidade Média | Severidade Alta
-|-|-|-|
10 | 01 | 05 | 04


## 5. Resumo dos Módulos
Módulo RF | Casos Testados | Casos aprovados | Casos reprovados | Bugs Associados
-|-|-|-|-|
RF01 - Login | 06 | 03 | 03 | B01
RF02 - Cadastro | 08 | 05 | 03 | B02, B03, B04
RF03 - Transferência | 12 | 06 | 06 |  B05, B06, B07, B08, B09, B10
RF04 - Extrato | 07 | 07 | 0 | -

## 6. Resumo dos bugs reportados

ID | Título | Severidade 
-|-|-|
B01 | Mensagem divergente da especificação nos campos de Login | Média
B02 | Mensagem divergente ao cadastrar com o campo E-mail vazio | Média
B03 | Mensagem divergente ao cadastrar com o campo Senha vazio | Média
B04 | Mensagem divergente ao cadastrar com o campo Confirmar senha vazio | Média
B05 | Sistema não redireciona o usuário para a tela de extrato após transferência realizada com sucesso | Alta
B06 | Sistema permite transferência com campo obrigatório Descrição vazio | Alta
B07 | Sistema permite transferência com campo Conta vazio | Alta
B08 | Sistema permite transferência com campo Dígito vazio | Alta
B09 | Mensagem apresentada com erro de concordância e ausência de acentuação | Baixa
B10 | Mensagem técnica exibida ao tentar transferir com valor vazio | Média


## 7. Evidências
- Plano de Testes (Markdown).
- Casos de Testes (Markdown).
- Relatório de Bugs (Markdown).
- Evidências em vídeos (Jam.dev).


## 8. Conclusão

- A execução dos testes manuais identificou falhas relevantes em funcionalidades críticas do sistema, principalmente no módulo transferência. Dos 33 casos de testes executados, 12 apresentaram falhas, resultando em 10 defeitos reportados. Recomenda-se a correção dos defeitos reportados antes da liberação do sistema para produção, especialmente aqueles classificados com severidade alta.
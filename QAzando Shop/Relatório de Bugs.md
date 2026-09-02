# Relatório de Bugs

- Nome do projeto: QAzando Shop
- Ambiente: https://automationpratice.com.br/
- Tipo de Teste: Teste exploratório
- Data do documento: 11/06/2026
- Responsável: Dalila Xavier

## 1. Bugs Reportados:

ID | Charter Associado |Descrição|Passo a passo | Resultado esperado | Resultado obtido | Severidade | Gravidade | Evidência 
:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
B01 | 01 |Sistema permite cadastro com o campo Nome inválido |1. Acessar a tela de Cadastro <br> 2.Preencher o campo Nome com caracteres especiais e/ou números <br> 3. Informar um e-mail válido <br> 4. Informar uma senha válida <br> 5. Clicar no botão Cadastrar | O sistema deveria impedir o cadastro com caracteres incompatíveis com nomes de usuários | O sistema permitiu o cadastro com o campo Nome com caracteres especiais e números | Média | Média | [Evidência](Evidências/nome-invalido01.mp4)
B02 | 01 |Sistema permite cadastro com um e-mail já cadastrado |1. Acessar a tela de Cadastro <br> 2.Informar o Nome corretamente <br> 3. Informar um e-mail já cadastrado <br> 4. Informar uma senha válida <br> 5. Clicar no botão Cadastrar | O sistema não deveria permitir o cadastro | O sistema permitiu o cadastro com usuário já cadastrado | Alta | Alta | [Evidência](Evidências/cadastro-email-duplicado.mp4)
B04 | 03 | Ícones das redes sociais não possuem ação ao serem clicados | 1. Acessar a tela de Cadastro <br> 2. Clicar sobre os ícones das redes sociais | O sistema deveria redirecionar o usuário para a rede social selecionada | O sistema permanece na tela de cadastro | Baixa | Baixa | [Evidência](Evidências/icone-sem-acao.mp4)





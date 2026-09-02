# Plano de Testes

## 1. Identificação do projeto

- Nome do Projeto: QAzando Shop
- Ambiente: https://automationpratice.com.br/
- Data do Documento: 10/06/2026
- Responsável: Dalila Xavier


## 2. Objetivo:

- Explorar a funcionalidade Cadastrar do site QAzando por meio de testes exploratórios, com o objetivo de identificar falhas funcionais, incosistências de usabilidade e comportamentos inesperados.


## 3. Estratégias e Técnicas de teste:

- Devido a ausência de documentação, optou-se por realizar testes exploratórios com o auxílio de sessões guiadas por charters, com foco na descoberta de defeitos, avaliação de riscos e análise do comportamento da funcionalidade. <br>

As técnicas utilizadas foram:

- Partição de equivalência, para validar entradas válidas e inválidas
- Análise de valor limite, para verificar o comportamento próximos aos limites
- Teste exploratório guidado por charters, com foco na descoberta de defeitos, riscos e comportamentos inesperados


## 4. Charters:

**Chater 01: Cadastro no sistema**

Missão: Explorar o comportamento do sistema no processo de cadastro utilizando dados válidos e inválidos

Perguntas-guia:

- O sistema permite o cadastro com dados válidos? 
- O sistema impede cadastro com Nome inválido? 
- O sistema impede cadastro com E-mail inválido? 
- É apresentado uma mensagem de erro ao se cadastrar com o campo Nome vazio? 
- É apresentado uma mensagem de erro ao se cadastrar com o campo E-mail vazio? 
- É apresentado uma mensagem de erro ao se cadastrar com o campo Senha vazio? 
- Existe validação de tamanho mínimo para senha? 
- O sistema impede a conclusão do cadastro ao inserir uma senha menor do que a exigida? 
- Após cadastro bem-sucedido o usuário é redirecionado para a página inicial do sistema? 


**Charter 02: Usabilidade**

Missão: Explorar a experiência do usuário durante o processo de cadastro

Perguntas-guia:

- As mensagens de erro são claras? 
- Existe erro de digitação? 
- O botão cadastrar é visível? 
- Após falha no cadastro, os campos ainda permanecem preenchidos? 
- O ícone de ver a senha está disponível? 


**Chater 03: Navegação e Componentes de Interface**

Missão: Explorar a navagação do usuário com objetivo de identificar falhas

Perguntas-guia:

- O usuário consegue acessar todas as informações localizadas no inicio da página? 
- É possível acessar as informações do tópico Shop localizadas no final da página? 
- O usuário consegue se cadastrar para receber Newsletter? 
- É possível acessar as redes sociais clicando nos ícones das redes? 
- O que acontece ao clicar em cadastrar e clicar sobre a seta de retorno? 


## 5. Critério de Entrada:

- Ambiente de teste disponível e estável.
- Definição das estratégias de testes.
- Charters definidos.


## 6. Critério de Saída:

- Todos os charters executados.
- Defeitos identificados e reportados.
- Evidências geradas (prints/vídeos).
- Relatório de Testes Exploratório devidamente finalizado.


## 7. Ferramentas:

- Navegador Google Chrome - Windows 10 - Versão 149.0.7827.54.
- VS Code - Organização das anotações e documentação.
- Xbox Game Bar e Snipping Tool - Captura e Gravação de tela.


## 8. Cronograma:

Atividade | Data |
-|-|
Plano de Testes | 10/06/2026
Charters 01 | 11/06/2026
Charters 02 | 11/06/2026
Charters 03 | 11/06/2026
Charters 04 | 11/06/2026
Relatório de Bugs | 11/06/2026
Relatório de Testes | 11/06/2026

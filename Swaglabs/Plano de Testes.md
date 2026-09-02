# 📝 PLANO DE TESTES 

## 1. Identificação do Projeto

- Nome do Projeto: Swag Labs
- Versão Avaliada: Demo pública
- Ambiente de Testes: https://www.saucedemo.com/
- Data do Documento: 18/03/2026
- Responsável: Dalila Xavier


## 2. Objetivo

- Explorar as funcionalidades do site Swag Labs por meio de testes exploratórios, identificando falhas funcionais, inconsistências de usabilidade e comportamentos distintos entre diferentes perfis de usuário, a fim de avaliar a qualidade da aplicação. 


## 3. Escopo

**Dentro do Escopo:**
- Login
- Catálogo de Produtos
- Menu
- Carrinho
- Checkout

**Fora do Escopo:**
- Teste de API

## 4. Técnicas Utilizadas

- Teste exploratório.
- Baseado nas seguintes heurísticas:
1. Heurística SFDPOT, com foco na validação de funcionalidades, variações de dados de entrada e saída, operações do sistema e comportamento ao longo do tempo.
2. Heurística de Usabilidade de Jakob Nielsen como referência para avaliar a responsividade, navegação, feedback visual. 


## 5. Charters

**Charter 01: Explorar a funcionalidade de Login para identificar falha de validação, segurança e usabilidade**

Perguntas-guia: 

- O sistema permite logar com sucesso com o usuário standard_user, problem_user, error_user e visual_user?
- O sistema apresenta problemas de desempenho ao logar com o usuário performance_glitch_user?
- O sistema impede que o usuário locked_out_user realize o login? 
- O sistema apresenta mensagem de erro ao logar com os dois campos (Username e Password) em branco?
- O sistema apresenta mensagem de erro ao logar com um dos campos em branco?
- O sistema apresenta uma mensagem de erro ao logar com um usuário não aceito?
- O sistema apresenta uma mensagem de erro ao logar com senha incorreta?
- É possível ver a senha ao preencher o campo?

---

**Charter 02: Explorar a funcionalidade da Página inicial e Catálogo de Produtos com foco em identificar falhas na apresentação dos itens**

Perguntas-guia:

- O sistema permite clicar sobre um produto?
- O sistema permite adicionar um produto no carrinho através do catálogo de produtos?
- O sistema permite adicionar mais de um produto no carrinho através da tela de produtos?
- O sistema permite adicionar mais do mesmo produto no carrinho através da tela de produtos?
- Ao clicar sobre o produto, é possível verificar mais detalhes dele?
- Na tela de talhes do produto, é possível retornar para o catálogo de produtos ao clicar na opção Back to products?
- O sistema permite remover um item adicionado ao carrinho ainda na tela de produtos?
- A listagem de produtos é atualizada por ordem, dependendo da seleção realizada na opção de filtro de produtos?
- Os botões das redes sociais funcionam corretamente?
- É possível acessar os termos de serviço do site?
- É possível acessar o termo de privacidade do site?
- Existe um espaço de orientação/ajuda no sistema?
- O sistema apresenta problemas de navegação ao logar com o usuário problem_user, performance_glitch_user, error_user e visual_user?


**Charter 03: Explorar o Menu com foco em identificar falhas**

Perguntas-guia: 

- O sistema permite acessar ao menu ao clicar no símbolo hamburguer?
- O sistema apresenta todos os produtos ao clicar em All Items?
- O sistema apresenta informações sobre o site ao clicar em About?
- O usuário consegue sair do sistema ao clicar em Logout?
- O sistema reinicia ao clicar sobre a opção Reset App State? 
- O menu fecha corretamente ao clicar no botão X? 


**Charter 04: Explorar o Carrinho com foco em identificar falhas nos itens adicionados e de usabilidade**

Perguntas-guia:

- Os produtos são apresentados corretamente?
- O sistema apresenta a quantidade, preço e a descrição dos produtos?
- É possível remover produtos diretamente do carrinho?
- O sistema permite que o usuário retorne a página inicial ao clicar em Continue Shopping?
- Os produtos anteriormente adicionados permanecem no carrinho ao retornar para a página inicial?
- Ao clicar sobre um produto diretamente do carrinho, o sistema redireciona a página do produto?
- Os produtos permanecem no carrinho ao atualizar a página?
- Os produtos permanecem no carrinho ao fazer logout?
- O carrinho é zerado após checkout?
- O contador do carrinho atualiza conforme adicionado novos produtos?
- O sistema apresenta problemas na visualização do carrinho com os usuários problem_user, performance_glitch_user, error_user e visual_user?


**Charter 05: Explorar o módulo checkout com foco em identificar falhas de processamento**

Perguntas-guia:

- O sistema apresenta uma mensagem ao realizar o checkout corretamente?
- O sistema apresenta mensagem de erro ao tentar realizar checkout com os campos vazios?
- O sistema apresenta mensagem de erro ao tentar realizar checkout com algum dos campos vazios?
- Algum dos campos aceita caracteres especiais?
- O módulo de checkout apresenta os detalhes sobre os itens do carrinho?
- Ao clicar no botão Cancel, o sistema retorna para o carrinho/página inicial?
- Ao clicar no botão Cancel, os produtos permanecem no carrinho?
- É possível retornar a página inicial ao finalizar a compra?
- O sistema permite checkout com o carrinho vazio?
- O sistema apresenta problemas no checkout com os usuários problem_user, performance_glitch_user, error_user e visual_user?


**Charter 06: Explorar o comportamento responsivo da aplicação em diferentes tamanhos de tela, com foco na identificação de quebras de layout e problemas de usabilidade**

Perguntas-guia:

- O layout da tela fica desproporcional ao reduzir o tamanho da tela?
- Algum dos botões quebram?
- As funcionalidades funcionam normalmente ao reduzir o tamanho da tela?


## 6. Critério de Entrada

- Ambiente de teste disponível e estável.
- Definição das estratégias de testes.
- Charters definidos.
- Credenciais de teste fornecidas: 

|ACCEPTED USERNAMES |PASSWORD|
|-|-|
|standard_user |secret_sauce|
|locked_out_user|secret_sauce|
|problem_user|secret_sauce|
|performance_glitch_user|secret_sauce|
|error_user|secret_sauce|
|visual_user|secret_sauce|


## 7. Critério de Saída

- Todos os charters executados.
- Defeitos identificados e reportados.
- Evidências geradas (prints/vídeos).
- Relatório de Testes Exploratório devidamente finalizado.


## 8. Ferramentas

- Navegador Google Chrome - Windows 10 - Versão 146.0.7680.80.
- VS Code - Organização das anotações e documentação.
- Xbox Game Bar, Spinning Tool e Jam.dev - Captura e Gravação de tela.


## 9. Cronograma

Atividade | Data
-|-
Plano de Testes | 18/03/2026
Charter 01: Login | 19/03/2026
Charter 02: Catálogo de Produtos | 19/03/2026
Charter 03: Menu | 23/03/2026
Charter 04: Carrinho | 23/03/2026
Charter 05: Checkout | 24/03/2026
Relatório de Testes | 24/03/2026


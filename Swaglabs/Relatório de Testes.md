# Relatório de Testes

### 1. Identificação da sessão 

- Nome do Projeto: Swag Labs
- Versão Avaliada: Demo pública
- Ambiente de Testes: https://www.saucedemo.com/
- Tipo de Teste: Teste Exploratório
- Data do Documento: 24/03/2026
- Responsável: Dalila Xavier

---
### 2. Notas da sessão

Área testada | Considerações |
-|-|
Login | Área completamente funcional. Porém, foi identificado um bug com relação a usabilidade do sistema, onde, ao inserir username ou password incorretamente é apresentado uma mensagem com a caixa de texto com o dimensionamento incorreto.
Catálogo de Produtos | De modo geral, a funcionalidade apresenta comportamento adequado. No entanto, foi identificado um defeito que impede o acesso aos Termos de Serviço e a Política de Privacidade do site. Adicionalmente, ao utilizar o perfil standard_user, foram observados pequenos trechos de código sendo exibidos na interface, impactando a usabilidade. Também foram registradas oportunidades de melhoria relacionadas à experiência do usuário nesta área.
Menu | A funcionalidade apresenta comportamento adequado. No entanto, após clicar em Reset App State, o sistema zerou o carrinho, mas permaneceu com o botão Remove nos produtos anteriormente adicionados.
Carrinho | Área funcional, no entanto, os itens do carrinho permanecem após logout e login com um diferente usuário. Além disso, foram identificadas oportunidades de melhorias de usabilidade.
Checkout | No geral, a área está funcional, no entanto, foram identificados bugs que permitem a conclusão do checkout com carrinho vazio e com caracteres especiais nos campos de preenchimento.
Usabilidade | No geral, o sistema apresenta uma boa usabilidade. No entanto, foi constatado um problema de dimensionamento do layout ao reduzir a tela (responsividade), além de um problema de dimensionamento na caixa de texto de mensagem de erro do módulo de Login.

---

### 3. Defeitos e Sugestões identificadas

Área | Bug identificado | Severidade | Evidência
-|-|-|-|
Login |B01 - Ao deixar o campo Username ou Password em branco, o sistema apresenta um erro de dimensionamento da caixa de texto |Baixa|[Evidência](evidencias/login-senha-incorreta.png)
Catálogo de Produtos |B02 - Área de Termos de Serviços e Política de Privacidade não possui ação |Média|[Evidência](https://jam.dev/c/e053ddbc-942a-4e2f-8ff8-68e40fdc20c0)
Catálogo de Produtos (standard_user) |B03 - Alguns produtos estão apresentando linhas do código, o que impacta diretamente na usabilidade |Média |[Evidência 01](evidencias/navegacao-codigo01.png) <br> [Evidência 02](evidencias/navegacao-codigo02.png)
Menu |B04 - Ao clicar em Reset App State, o sistema zerou o carrinho, no entanto, os produtos anteriormente adicionados permanecem com o botão Remove | Média |[Evidência](evidencias/menu-reset-app-state.mp4)
Carrinho |B05 - Itens do carrinho permanecem após logout e login com um diferente usuário |Alta | [Evidência](evidencias/carrinho-produto-diferente-usuario.mp4)
Checkout |B06 - O sistema permitiu conclusão do checkout com caracteres especiais |Alta|[Evidência](evidencias/checkout-caracteres.mp4)
Checkout |B07 - O sistema permitiu a conclusão do checkout com carrinho vazio |Média|[Evidência](evidencias/checkout-carrinho-vazio.mp4)
Login |B08 - A caixa de texto da mensagem de erro de login apresenta problema de dimensionamento na versão mobile (responsividade) |Baixa|[Evidência](evidencias/usabilidade-mensagem.png)
Catálogo de Produtos |B09 - O layout sofreu um impacto ao reduzir o tamanho da tela na versão mobile |Baixa |[Evidência](evidencias/usabilidade-layout.png)


Área | Sugestão |
-|-|
Login | Inserir o ícone de exibir a senha no campo Password
Catálogo de Produtos | Acrescentar um espaço de ajuda na tela inicial, com o objetivo de orientar o usuário e melhorar a usabilidade do sistema
Carrinho | É interessante que, ao clicar sobre um determinado produto dentro do carrinho, seja possível retornar ao carrinho, sem precisar retornar para a tela inicial de produtos

---

### 4. Resumo da Execução

**Resultado da Execução:**
Área | Bugs Associados
-|-|
Login | B01, B08
Catálogo de Produtos | B02, B03, B09
Menu | B04
Carrinho | B05
Checkout | B06, B07

**Bugs Identificados:**

Bugs Reportados | Severidade Alta | Severidade Média | Severidade Baixa
-|-|-|-|
9 | 2 | 4 | 3

---

### 5. Métricas da Sessão

- Charters executados: 6
- Bugs encontrados: 9
- Sugestões identificadas: 3

---

### 6. Evidências 
- Plano de Testes (Markdown).
- Evidências em vídeos e imagens.

---

### 7. Conclusão

O teste exploratório abordou as principais funcionalidades do sistema conforme planejado nos charters definidos no plano de testes. Durante a execução foram identificados 9 defeitos, incluindo 2 de alta severidade, 4 de severidade média e 3 de severidade baixa, que podem impactar diretamente a experiência do usuário e a consistência do sistema. De forma geral, os fluxos principais estão funcionais, porém recomenda-se priorizar a correção dos defeitos identificados relacionados à  navegação e validação de dados para melhoria da estabilidade e usabilidade da aplicação.

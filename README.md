# TestePlusoft
Script de testes em 2 funcionalidades disponibilizadas, sendo elas Login e Busca

# FuncionalidadeLogin  
  
Automação de Teste Cypress para Funcionalidade de Login
Este repositório contém um conjunto de testes Cypress para testar a funcionalidade de login de uma aplicação web. O conjunto de testes verifica se a página de login carrega corretamente, se o usuário pode preencher o formulário de login e se a aplicação redireciona para a URL correta após um login bem-sucedido (Url que foi considerada fictícia na aplicação)

Índice
Instalação
Conjunto de Testes
Funcionalidade de Login
URL
Campos
Comportamento Esperado
Executando os Testes
Contribuição
Licença
Instalação
Para instalar o Cypress e configurar o ambiente de testes, siga os passos abaixo:

Clone o repositório:
bash
Copiar código
git clone https://github.com/seu-usuario/seu-repositorio.git
Navegue até o diretório do projeto:
bash
Copiar código
cd seu-repositorio
Instale as dependências:
bash
Copiar código
npm install
Conjunto de Testes
Funcionalidade de Login
Este conjunto de testes cobre os seguintes cenários:

URL
Verifica se a página de login é carregada corretamente no servidor local.

javascript
Copiar código
describe('Login Functionality', () => {
  it('URL', () => {
    // Visitar a página de login no servidor local
    cy.visit('/src/login.html');
  });
});
Campos
Verifica se os campos de usuário e senha podem ser preenchidos e se o botão de login pode ser clicado.

javascript
Copiar código
describe('Login Functionality', () => {
  it('Campos', () => {
    // Preencher o campo de usuário
    cy.get('#username').type('usuario_valido');
    
    // Preencher o campo de senha
    cy.get('#password').type('senha_valida');
    
    // Re-query o botão de login e clique nele
    cy.get('#login_button').should('be.visible').click();
  });
});
Comportamento Esperado
Verifica se a URL redireciona corretamente após o login.

javascript
Copiar código
describe('Login Functionality', () => {
  it('Comportamento esperado', () => {
    // Verificar se a URL redireciona corretamente após o login
    cy.url().should('not.equal', 'http://localhost:62258/login/teste-qualquer-url'); // URL fictícia
  });
});
Executando os Testes
Para executar os testes, use o comando abaixo:

bash
Copiar código
npx cypress open
Isso abrirá a interface do Cypress, onde você pode selecionar e executar os testes.
# FuncionalidadeSearch


# Ferramentas
  Cypress

# Observações
  As aplicações foram testadas no localhost.

# Usuários - Regras de Negócio

## Funcionalidade: Cadastro de Usuários
Como administrador do sistema  
Quero cadastrar um Usuário Novo

### Cenários Válidos:

#### Cadastro com dados corretamente preenchidos
    Dado que o usuário está na tela de cadastro
    Quando ele preenche o campo Login
    E quando ele preenche o campo Nome
    E quando ele preenche o campo E-mail
    E quando ele informa o código de uma empresa, e clicar no botão "...", irá abrir um modal de pesquisa para selecionar a empresa a ser vinculada.
    E quando ele informa a empresa, e clicar no botão "...", irá abrir um modal de pesquisa para selecionar a empresa a ser vinculada.
    Então o sistema deve exibir a mensagem "Cadastro realizado com sucesso"
    E o usuário deve ser registrado no sistema, e a senha temporária será encaminhada ao e-mail cadastrado.

#### Botão Redefinir Senha
    Dado que o usuário está na tela de cadastro
    Quando ele clicar no botão "Redefinir Senha"
    Então o sistema irá encaminhar um link de acesso para o e-mail cadastrado.

### Cenários Inválidos: 

#### Cadastro sem Login
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Login
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Login inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem Nome
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Nome
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Nome inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem E-mail
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO seleciona o campo E-mail
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "E-mail inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem Vinculo com Empresa
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO vincula o cadastro a uma Emrpesa
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Vinculo Usuario/Empresa inválido"
    E o cadastro não deve ser realizado

# Usuários - Regras de Negócio

## Funcionalidade: Cadastro de Usuários
Como administrador do sistema  
Quero cadastrar um Usuário Novo

### Cenários Válidos:

#### Cadastro com dados corretamente preenchidos
    Dado que o usuário está na tela de cadastro
    Quando ele preenche o campo Login
    E quando ele preenche o campo Estoque
    E quando ele preenche o campo Senha
    E quando ele preenche o campo Nome
    E quando ele preenche o campo E-mail
    E quando ele vincula pelo menos 1 empresa ao cadastro do usuário
    Então o sistema deve exibir a mensagem "Cadastro realizado com sucesso"
    E o usuário deve ser registrado no sistema

### Cenários Inválidos: 

#### Cadastro sem Login
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Login
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Login inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem Senha
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Senha
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Senha inválida"
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

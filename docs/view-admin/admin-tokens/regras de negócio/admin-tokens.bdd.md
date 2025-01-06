# Regras de Negócio

## Funcionalidade: Cadastro de Tokens
  Como administrador do sistema   
  Quero cadastrar um novo Token a uma empresa

### Cenários Válidos: 

#### Cadastro com dados corretamente preenchidos
    Dado que o usuário está na tela de cadastro
    Quando ele seleciona a empresa
    E quando ele preenche o Descrição com os dados de acesso ao Token
    E quando ele preenche a Data de Criação no formato "##/##/####"
    E quando ele preenche o Token informado pela K
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem "Cadastro realizado com sucesso"
    E o novo acesso da Empresa com Token deve ser registrado no sistema

#### Informação automática de Data de Criação
    Dado que o usuário está na tela de cadastro
    Quando ele for criar um novo registro, a data de cadastro virá preenchida automaticamente, pela data atual do sistema operacional, no formato "##/##/#### ##:##:###"
    

### Cenários Inválidos: 

#### Cadastro sem Descrição
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Descrição
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Descrição inválida"
    E o cadastro não deve ser realizado

#### Cadastro sem Token
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Token
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Token inválido"
    E o cadastro não deve ser realizado

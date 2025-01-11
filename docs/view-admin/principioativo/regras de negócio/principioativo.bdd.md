# Princípio Ativo - Regras de Negócio

## Funcionalidade: Cadastro de Princípio Ativo
  Como administrador do sistema   
  Quero cadastrar um Princípio Ativo Novo

### Cenários Válidos: 

#### Cadastro com dados corretamente preenchidos
    Dado que o usuário está na tela de cadastro
    Quando ele preenche o campo Descrição
    E quando ele preenche o campo Nome Comercial
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem "Cadastro realizado com sucesso"
    E a empresa deve ser registrado no sistema

### Cenários Inválidos: 

#### Cadastro sem Descrição
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Descrição
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Descrição inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem Nome Comercial
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Nome Comercial
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Nome Comercial inválido"
    E o cadastro não deve ser realizado

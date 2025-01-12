# Unidade de Medida - Regras de Negócio

## Funcionalidade: Cadastro de Unidade de Medida
  Como administrador do sistema   
  Quero cadastrar um Unidade de Medida Novo

### Cenários Válidos: 

#### Cadastro com dados corretamente preenchidos
    Dado que o usuário está na tela de cadastro
    Quando ele preenche o campo Descrição
    E quando ele preenche o campo Sigla
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem "Cadastro realizado com sucesso"
    E a Unidade de Medida deve ser registrado no sistema

### Cenários Inválidos: 

#### Cadastro sem Descrição
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo [Descrição]
    E clica no botão: "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Descrição inválida"
    E o cadastro não deve ser realizado

#### Cadastro sem Sigla
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo [Sigla]
    E clica no botão:  "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Sigla inválida"
    E o cadastro não deve ser realizado

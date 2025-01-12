# Marca - Regras de Negócio

## Funcionalidade: Cadastro de Marca
  Como usuário do sistema   
  Quero cadastrar um Marca Novo

### Cenários Válidos: 

#### Cadastro com dados corretamente preenchidos
    Dado que o usuário está na tela de cadastro
    Quando ele preenche o campo [Descrição] 
    E clica no botão: "Salvar"
    Então o sistema deve exibir a mensagem "Cadastro realizado com sucesso"
    E a Marca deve ser registrado no sistema

### Cenários Inválidos: 

#### Cadastro sem Descrição
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo [Descrição]
    E clica no botão: "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Descrição inválida"
    E o cadastro não deve ser realizado


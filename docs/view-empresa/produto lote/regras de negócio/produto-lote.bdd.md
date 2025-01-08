# Produto Lote - Regras de Negócio

## Funcionalidade: Cadastro de Lote Produtos
Como administrador do sistema  
Quero cadastrar um Lote de Produto Novo

### Cenários Válidos:

#### Cadastro com dados corretamente preenchidos
    Dado que o usuário está na tela de cadastro
    Quando ele preenche o campo Descrição
    E quando ele preenche o campo Data Fabricação
    E quando ele preenche o campo Data Validade
    E quando ele preenche a Quantidade
    Então o sistema deve exibir a mensagem "Cadastro realizado com sucesso"
    E o Lote do produto deve ser registrado no sistema

### Cenários Inválidos: 

#### Cadastro sem Descrição
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Descrição
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Descrição inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem Quantidade
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Quantidade
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Quantidade inválida"
    E o cadastro não deve ser realizado

#### Cadastro sem Data Fabricação
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Data Fabricação
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Data Fabricação inválida"
    E o cadastro não deve ser realizado

#### Cadastro sem Data Validade
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Data Validade
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Data Validade inválida"
    E o cadastro não deve ser realizado

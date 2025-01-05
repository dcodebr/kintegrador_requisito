# Clientes - Regras de Negócio

## Funcionalidade: Cadastro de Cliente
  Como administrador do sistema
  Quero cadastrar um cliente novo

### Cenários Válidos: 

#### Cadastro com dados corretamente preenchidos
    Dado que o usuário está na tela de cadastro
    Quando ele preenche o campo nome
    E quando ele preenche o campo CNPJ no formato "##.###.###/####-##"
    E quando ele preenche o endereço
    E quando ele seleciona a cidade
    E quando ele seleciona a UF
    E quando ele preenche o telefone
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem "Cadastro realizado com sucesso"
    E o cliente deve ser registrado no sistema

#### Informação automática de endereço
    Dado que o usuário está na tela de cadastro
    Quando ele informa o CEP no formato "##.###-###"
    E quando ele tabula o campo CEP
    Então o sistema deverá buscar os dados de endereço na base de dados e preencher o campos Endereço, Cidade e UF.

### Cenários Inválidos: 

#### Cadastro sem nome
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo nome
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Nome inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem nome
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo nome
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Nome inválido"
    E o cadastro não deve ser realizado
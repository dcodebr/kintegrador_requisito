# Clientes - Regras de Negócio

## Funcionalidade: Cadastro de Empresas
  Como administrador do sistema   
  Quero cadastrar uma Empresa nova

### Cenários Válidos: 

#### Cadastro com dados corretamente preenchidos
    Dado que o usuário está na tela de cadastro
    Quando ele preenche o campo nome
    E quando ele preenche o campo CNPJ no formato "##.###.###/####-##"
    E quando ele preenche o endereço
    E quando ele seleciona a cidade
    E quando ele seleciona a UF
    E quando ele preenche o telefone
    E quando ele preenche o e-mail
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem "Cadastro realizado com sucesso"
    E a empresa deve ser registrado no sistema

#### Informação automática de Endereço
    Dado que o usuário está na tela de cadastro
    Quando ele informa o CEP no formato "##.###-###"
    E quando ele tabula o campo CEP
    Então o sistema deverá buscar os dados de endereço na base de dados e preencher o campos Endereço, Cidade e UF.

### Cenários Inválidos: 

#### Cadastro sem Nome
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Nome
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Nome inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem CNPJ
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo CNPJ
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "CNPJ inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem Endereço 
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Endereço
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Endereço inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem Número
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Número
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Número inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem Bairro
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Bairro
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Bairro inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem CEP
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo CEP
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "CEP inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem E-mail
    Dado que o usuário está na tela de cadastro
    Quando ele preenche o campo e-mail diferente do padrão "exemplo@contato.com"
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "E-mail inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem Telefone
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Telefone
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Telefone inválido"
    E o cadastro não deve ser realizado

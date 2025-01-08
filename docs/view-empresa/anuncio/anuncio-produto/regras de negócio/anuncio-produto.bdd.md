# Anuncio-Produto - Regras de Negócio

## Funcionalidade: Cadastro de Anuncio-Produtos
  Como administrador do sistema   
  Quero cadastrar um Anuncio-Produto novo

### Cenários Válidos: 

#### Cadastro com dados corretamente preenchidos
    Dado que o usuário está na tela de cadastro
    Quando ele preenche o campo Data Expiração no formato "##/##/##### ##:##:##"
    E quando ele marcar o campo Reserva Saldo
    E quando ele marcar o campo Permite Acessar Informações no Interesse
    E quando ele marcar o campo Remove Anuncio após Data Expiração
    E quando ele informar pelo menos um Produto na tabela de Anuncio-Produto
    E quando ele preencher o campo Codigo do produto
    E quando ele preencher o campo Descrição do Produto
    E quando ele preencher o campo Quantidade do Produto
    E quando ele Selecionar o campo Unidade de Medida
    E quandod ele informar o Valor Unitario do Produto 
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem "Cadastro realizado com sucesso"
    E o anuncio produto deve ser registrado no sistema

#### Informação automática de Valor Total
    Dado que o usuário está na tela de cadastro
    Quando ele informa nos campos de Produtos as informações de quantidade e Valor unitário
    Então o sistema deverá calcular corretamente o Valor Total do Produto do Anuncio..

#### Informação automática de Total Anuncio
    Dado que o usuário está na tela de cadastro
    Quando ele informa os produtos na tabela de Produto de Anuncio
    Então o sistema deverá calcular corretamente o Valor do Produto do Anuncio..

#### Informação automática de Qtde Total
    Dado que o usuário está na tela de cadastro
    Quando ele informa os produtos na tabela de Produto de Anuncio
    Então o sistema deverá calcular corretamente a Quantidade do Produto do Anuncio..

### Cenários Inválidos: 

#### Cadastro sem Quantidade de Produto
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Qtde
    E clica no botão "Incluir"
    Então o sistema deve exibir a mensagem de validação: "Qtde inválida"
    E o cadastro não deve ser realizado

#### Cadastro sem Valor Unitário de Produto
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Valor Unitário
    E clica no botão "Incluir"
    Então o sistema deve exibir a mensagem de validação: "Valor Unitário inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem Unidade de Medida
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO selecionar o campo Unidade de Medida
    E clica no botão "Incluir"
    Então o sistema deve exibir a mensagem de validação: "Unidade de Medida inválida"
    E o cadastro não deve ser realizado



# Produtos - Regras de Negócio

## Funcionalidade: Cadastro de Produtos
Como usuário do sistema  
Quero cadastrar um Produto Novo

### Cenários Válidos:

#### Cadastro com dados corretamente preenchidos
    Dado que o usuário está na tela de cadastro
    Quando ele preenche o campo Descrição
    E quando ele preenche o campo Estoque
    E quando ele seleciona o Princípio Ativo
    E quando ele seleciona a Marca/Laboratório
    E quanddo ele seleciona a Unidade de Medida
    E quando ele marca o campo Controle por lote, deve habilitar a seção Lote e as informações Lote, Data Fabricação, Data Validade, Quantidade preenchida.
    Então o sistema deve exibir a mensagem "Cadastro realizado com sucesso"
    E o produto deve ser registrado no sistema

### Cenários Inválidos: 

#### Cadastro sem Descrição
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Descrição
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Descrição inválido"
    E o cadastro não deve ser realizado

#### Cadastro com Controle por Lote marcado e não informado Lote
    Dado que o usuário está na tela de cadastro
    Quando ele marca o campo [Controle por lote]
    E NÃO informa nenhum [Lote]
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Controle por Lote habilitado mas não informado lote"

#### Cadastro sem Estoque
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO preenche o campo Estoque
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Estoque inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem Princípio Ativo
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO seleciona o campo Princípio Ativo
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Princípio Ativo inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem Marca/Laboratório
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO seleciona o campo Marca/Lanboratório
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Marca/Laboratório inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem Unidade de Medida
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO seleciona o campo Unidade de Medida
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem de validação: "Unidade de Medida inválido"
    E o cadastro não deve ser realizado

#### Cadastro sem Lote informado 
    Dado que o usuário está na tela de cadastro
    Quando ele NÃO informa corretamente os dados do lote
    E clica no botão "Inserir"
    Então o sistema deve exibir a mensagem de validação: "Lote e demais campos precisam ser preenchidos"
    E o cadastro não deve ser realizados
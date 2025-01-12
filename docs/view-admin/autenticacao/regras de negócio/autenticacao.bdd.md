# Autenticação - Regras de Negócio

## Funcionalidade: Tela de Autenticação
  Como usuário do sistema   
  Quero acessar o sistema

### Cenários Válidos: 

#### Dados corretamente preenchidos
    Dado que o usuário está na tela de Autenticação
    Quando ele informa o campo [Usuário] 
    Podendo ser a informação de [Login] ou [E-mail]
    E ele informa o campo [Senha]
    E clica no botão: "Acessar"
    Então o sistema deve permitir o usuário a acessar o sistema

#### Hyperlink - Recuperar Senha
    Dado que o usuário está na tela de Autenticação
    Quando ele clica no link: "Recuperar senha"
    Então o sistema deve abrir uma nova tela, para ser informado o usuário para efetuar a recucperação de senha.
  
### Cenários Inválidos: 

#### Autenticação sem Usuário
    Dado que o usuário está na tela de Autenticação
    Quando ele NÃO preenche o campo [Usuário]
    E clica no botão: "Acessar"
    Então o sistema deve exibir a mensagem de validação: "Usuário e/ou Senha inválida"
    E o sistema não deve ser autenticado

#### Autenticação sem Senha
    Dado que o usuário está na tela de Autenticação
    Quando ele NÃO preenche o campo [Senha]
    E clica no botão: "Acessar"
    Então o sistema deve exibir a mensagem de validação: "Usuário e/ou Senha inválida"
    E o sistema não deve ser autenticado

# Autenticação - Recuperar Senha

## Funcionalidade: Tela de Recuperar Acesso
  Como usuário do sistema   
  Quero acessar o Recuperar o acesso 

### Cenários Válidos: 

#### Dados corretamente preenchidos
    Dado que o usuário está na tela de Autenticação - Recuperar Senha
    Quando ele informa o campo [Usuário] 
    E clica no botão: "Enviar"
    Então o sistema deve enviar um e-mail com as informações necessárias para a recuperação de senha de acesso. Apresentando uma mensagem: "E-mail de Recuperaçao de Senha enviado!"

### Cenário Inválido

#### Campo Usuário inválido
    Dado que o usuário está na tela de Autenticação - Recuperar Senha
    Quando ele NÃO informa o campo [Usuário] 
    E clica no botão: "Enviar"
    Então o sistema deve exibir a mensagem de validação: "Usuário inválido"

# Autenticação - Alterar Senha

## Funcionalidade: Tela de Alterar Senha
  Como usuário do sistema   
  Quero acessar o Alterar Senha

### Cenários Válidos: 

#### Dados corretamente preenchidos
    O usuário irá clicar no link recebido por e-mail, e será redirecionado a tela de "Autenticação Alterar Senha"
    Dado que o usuário está na tela de Autenticação - Alterar Senha
    Quando ele informa o campo [Nova Senha]
    E ele informa o campo [Repetir Senha]
    E quando ele deslocar o cursor para o próximo campo, o sistema deve valdiar os campos: [Nova Senha] e [Repetir Senha] 
    E clica no botão: "Confirmar"
    Então o sistema deve redirecionar para a Tela de Autenticação

### Cenário Inválido

#### Campo Nova Senha e Repetir Senha inválido
    Dado que o usuário está na tela de Autenticação - Alterar Senha
    Quando ele NÃO informa o campo [Nova Senha]
    E qual ele NÃO informa o campo [Repetir Senha] 
    E clica no botão: "Confirmar"
    Então o sistema deve exibir a mensagem de validação: "Usuário e/ou Senha inválidos"
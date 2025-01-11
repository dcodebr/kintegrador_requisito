# Anúncios - Regras de Negócio

## Lançar um Anúncio
  Como usuário do sistema   
  Quero lançar um anúncio

### Cenários Válidos: 

#### Lançamento de anúncio com mínimo de informações
    Dado que o usuário está na tela de anúncio
    Quando o sistema preenche automaticamente o campo Data Cadastro
    E quando ele informa um produto com código, qtde, Un, Valor Un
    E clica em Incluir
    E clica no botão "Salvar"
    Então o sistema deve exibir a mensagem "Cadastro realizado com sucesso"
    E o anúncio deve ser registrado no sistema

#### Informação automática de Total Anuncio
    Dado que o usuário está na tela de anúncio
    Quando ele informa os produtos na seção Produtos
    Então o sistema deverá somar o Valor Total de todos os itens do anúncio e informar no campo Total Anúncio.

### Reserva de Saldo
    Dado que o usuário está na tela de anúncio
    Quando ele marca o check [Reserva Saldo]
    E clica no botão "Salvar"
    Então o sistema deverá baixar o saldo disponível referente a quantidade de cada produto do anúncio no módulo Interesses. [anuncioproduto.qtde] - [anunciointeresseproduto.qtde].

### Permite Acessar Informações do Anunciante
    Dado que o usuário está na tela de anúncio
    Quando ele marca o check [Permite acessar inf. no Interesse]
    E quando clica no botão "Salvar"
    O sistema habilita a visualização dos dados do anunciante na listagem de anúncios no módulo Interesses.

### Anúncio Expirado
    Dado que o usuário está na tela de anúncio
    Quando ele informa Data Expiração
    E quando ele marca o check [Remove anúncio após expiração]
    E clica no botão "Salvar"
    Então o sistema deverá ocultar o anúncio na listagem do módulo Interesses quando [Data de Expiração] é menor que DATA_HORA_ATUAL.

### Habilita check [Remove anúncio após Expiração]
    Dado que o usuário está na tela de anúncio
    Quando ele informa uma data em [Data Expiração]
    O sistema habilita o check [Remove anúncio após Expiração].

### Desabilita check [Remove anúncio após Expiração]
    Dado que o usuário está na tela de anúncio
    Quando ele NÃO informa uma data em [Data Expiração]
    O sistema desabilita o check [Remove anúncio após Expiração].

### Cenários Inválidos: 

#### Data de Cadastro em Branco
    Dado que o usuário está na tela de anúncio
    E não informa uma data em [Data Cadastro]
    E clica no botão "Salvar"
    Então o sistema deverá exibir a mensagem "Data de Cadastro Inválida!"

#### Data de Expiração menor que Data Cadastro
    Dado que o usuário está na tela de anúncio
    E informa uma data em [Data Expiração] menor que a data informada em [Data Cadastro]
    E clica no botão "Salvar"
    Então o sistema deverá exibir a mensagem "Data de Expiração não pode ser menor que Data Cadastro!"

#### Anúncio Expira sem Data de Expiração
    Dado que o usuário está na tela de anúncio
    E marca o check [Remove anúncio após expiração]
    E não há data preenchida em [Data Expiração]
    E o usuário clica no botão "Salvar"
    Então o sistema deverá exibir a mensagem "Anúncio não pode expirar sem Data Expiração".

#### Anúncio sem Itens
    Dado que o usuário está na tela de anúncio
    E NÃO informa nenhum produto na seção "Produtos"
    E clica no botão "Salvar"
    Então o sistema deverá exibir a mensagem "Anúncio sem produtos!".

## Lançar Itens do Anúncio
  Como usuário do sistema   
  Quero incluir um item no anúncio

### Cenários Válidos:

#### Seleção de Produto
    Dado que o usuário está na tela de anúncio
    E seleciona um produto no campo [código]
    E que o código seja referente a um produto existente no cadastro de produtos
    Então o sistema deverá carregar a a descrição do produto e a Ún principal do produto e o Valor Un do produto.

#### Lançamento de Produto com mínimo de Informações
    Dado que o usuário está na tela de anúncio
    E informa um produto na seção de Produtos
    E informa uma quantidade no campo [Qtde]
    E informa uma unidade de medida em [Un]
    E informa um valor em [Valor Un]
    E clica no botão "➕"
    Então o sistema deverá incluir o produto na listagem da seção Produtos.

#### Exclusão de Produtos
    Dado que o usuário está na tela de anúncio
    E seleciona um produto da seção "Produtos"
    E clica no botão "❌"
    E o produto selecionado NÃO esteja vinculado a nenhum Interesse
    O sistema deverá remover o produto da listagem.

### Cenários Inválidos:

#### Seleção de Produto inválido
    Dado que o usuário está na tela de anúncio
    E informa um código no campo [Código]
    E desloca o cursor o próximo campo
    E o código não corresponde a nenhum cadastro de produto no sistema
    Então o sistema deverá exibir a mensagem "Produto não localizado!"

#### Produto sem quantidade informada
    Dado que o usuário está na tela de anúncio
    E NÃO informa uma quantidade válida no campo [Qtde]
    E clica no botão "➕"
    Então o sistema deverá exibir a mensagem "Qtde. inválida!"

#### Produto sem unidade de medida
    Dado que o usuário está na tela de anúncio
    E NÃO informa uma unidade de medida presente no cadastro do produto na caixa de seleção [Un]
    E clica no botão "➕"
    Então o sistema deverá exibir a mensagem "Un inválida!"

#### Produto sem valor unitário
    Dado que o usuário está na tela de anúncio
    E NÃO informa uma valor válido em [Valor Un]
    E clica no botão "➕"
    Então o sistema deverá exibir a mensagem "Valor Un inválido!"

#### Clicar no botão ❌ sem produto selecionado
    Dado que o usuário está na tela de anúncio
    E NÃO seleciona nenhum produto da seção "Produtos"
    E clica no botão "❌"
    O sistema deverá exibir a mensagem "Selecione um Produto para excluir!"

#### Excluir produto vinculado a Interesses
    Dado que o usuário está na tela de anúncio
    E seleciona um produto na seção "Produtos"
    E clica no botão "❌"
    E o produto está vinculado a pelo menos um lançamento no módulo Interesse
    O sistema deverá exibir a mensagem "Produto com movimentação lançada em Interesses".

## Interessados no Anúncio
  Como usuário do sistema   
  Quero visualizar os interessados no anúncio

### Cenários Válidos:

#### Visualizar interessados no anúncio
    Dado que o usuário está na tela de anúncio
    Quando o usuário clicar no botão "Interesses"
    E houver um anúncio selecionado
    E o anúncio estiver salvo
    O sistema deverá exibir o modal "Interessados no Anúncio"

#### Visualizar Interesse do anúncio
    Dado que o usuário está na tela de anúncio
    Quando o usuário clicar no botão "Visualizar" em um item da lista de Interesses
    O sistema deverá apresentar o módulo Interesses com o registro de interesse selecionado.

### Cenários Inválidos:

#### Clicar no botão "Interesses" sem lançamento de anúncio salvo
    Dado que o usuário está na tela de anúncio
    Quando o usuário clicar no botão "Interesses"
    E o anúncio NÃO estiver salvo
    O sistema deverá apresentar a mensagem "Anúncio não salvo!"
# Interesse - Regras de Negócio

## Funcionalidade: Lançamento de Interesse
  Como usuário do sistema   
  Quero lançar um novo Interesse

### Cenários Válidos: 

#### Importar todos itens de Anúncio pela tela de Interesse
    Dado que o usuário está na tela de anúncio
    E clica na aba Anúncio Vinculado
    E clica no botão ⋯ para selecionar um anúncio disponível
    E seleciona um anúncio disponível
    E clica no botão "Imp. Todos"
    O sistema deverá importar todos itens do anúncio selecionado para a listagem de itens da "Principal".

#### Importar itens selecionados de Anúncio pela tela de Interesse
    Dado que o usuário está na tela de anúncio
    E clica na aba Anúncio Vinculado
    E clica no botão ⋯ para selecionar um anúncio disponível
    E seleciona um anúncio disponível
    E marca o check de ao menos um item da listagem de produtos do Anúncio
    O sistema deverá importar os itens  selecionados do anúncio selecionado para a listagem de itens da "Principal".

#### Alterar a Quantidade de um item do interesse
    Dado que o usuário está na tela de anúncio
    E clica na aba Anúncio Vinculado
    E clica no botão ⋯ para selecionar um anúncio disponível
    E seleciona um anúncio disponível
    E clica no botão "Imp. Todos"
    E clica na aba "Principal"
    E seleciona um item da listagem de produtos do interesse
    E digita uma quantidade no campo Qtde
    E a quantidade digitada é menor ou igual a quantidade disponível no saldo do anúncio(qtde <= {anuncioproduto.qtde} - {SUM(anunciointeresseproduto.qtde)})
    E clica no botão ➕
    O sistema deverá atualizar o lançamento do item na listagem de produtos do anúncio.

#### Excluir item da listagem de produtos do anúncio
    Dado que o usuário está na tela de anúncio
    E clica na aba Anúncio Vinculado
    E clica no botão ⋯ para selecionar um anúncio disponível
    E seleciona um anúncio disponível
    E clica no botão "Imp. Todos"
    E clica na aba "Principal"
    E seleciona um item da listagem de produtos do interesse
    E clica no botão ❌
    O sistema deverá remover o item da listagem de produtos do interesse.

#### Salvar o lançamento de um Interesse
    Dado que o usuário está na tela de anúncio
    E clica na aba Anúncio Vinculado
    E clica no botão ⋯ para selecionar um anúncio disponível
    E seleciona um anúncio disponível
    E clica no botão "Imp. Todos"
    E clica no botão "Salvar"
    E caso o valor do campo "Total Interesse" seja maior que 0
    O sistema deverá persistir o interesse do anúncio e notificar o anunciante.

#### Exibir Anúncios Disponíveis para Interesse
    Dado que o usuário está na tela de anúncio
    E clica no botão "Anúncios"
    O sistema deverá exibir o "Modal Pesquisa Por Anúncios".

### Cenários Inválidos:

#### Quantidade item de produto do Interesse maior que saldo disponível
    Dado que o usuário está na tela de anúncio
    E clica na aba Anúncio Vinculado
    E clica no botão ⋯ para selecionar um anúncio disponível
    E seleciona um anúncio disponível
    E clica no botão "Imp. Todos"
    E clica na aba "Principal"
    E seleciona um item da listagem de produtos do interesse
    E digita uma quantidade no campo Qtde
    E a quantidade digitada é maiora quantidade disponível no saldo do anúncio(qtde > {anuncioproduto.qtde} - {SUM(anunciointeresseproduto.qtde)})
    E clica no botão ➕
    O sistema deverá exibir a mensagem "Quantidade maior que saldo disponível no anúncio" e impedir a alteração.

#### Importar mais de uma vez o mesmo item de produto sem lote
    Dado que o usuário está na tela de anúncio
    E clica na aba Anúncio Vinculado
    E clica no botão ⋯ para selecionar um anúncio disponível
    E seleciona um anúncio disponível
    E marca o check de ao menos um item da listagem de produtos do Anúncio
    E o produto NÃO controlar lote ({produto.controlalote} = false)
    E o produto ja estiver incluído na listagem de produtos do interesse na aba principal
    E  sistema deverá exibir a mensagem "Produto já importado no interesse" e impedir a importação do item.

#### Importar mais de uma vez o mesmo item de produto com lote
    Dado que o usuário está na tela de anúncio
    E clica na aba Anúncio Vinculado
    E clica no botão ⋯ para selecionar um anúncio disponível
    E seleciona um anúncio disponível
    E marca o check de ao menos um item da listagem de produtos do Anúncio
    E o produto NÃO controlar lote ({produto.controlalote} = true)
    E o produto ja estiver incluído na listagem de produtos do interesse na aba principal
    E o lote do produto seja o mesmo do item já importado
    E  sistema deverá exibir a mensagem "Produto já importado no interesse" e impedir a importação do item.

#### Lançar Interesse sem Anúncio vinculado
    Dado que o usuário está na tela de anúncio
    E NÃO seleciona nenhum anúncio disponível
    E clica no botão "Salvar"
    O sistema deverá exibir a mensagem "Interesse sem anúncio vinculado" e impedir a operação.

#### Lançar Interesse sem produtos importados
    Dado que o usuário está na tela de anúncio
    E clica no botão ⋯ para selecionar um anúncio disponível
    E seleciona um anúncio disponível
    E NÃO importa nenhum produto de um anúncio
    E clica no botão "Salvar"
    O sistema deverá exibir a mensagem "Interesse sem itens lançados" e impedir a operação.

#### Lançar interesse com Anúncio Indisponível
    Dado que o usuário está na tela de anúncio
    E clica na aba Anúncio Vinculado
    E clica no botão ⋯ para selecionar um anúncio
    E seleciona um anúncio com data de expiração menor que DATA_HORA_ATUAL
    O sistema deverá exibir a mensagem "Anúncio indisponível para interesse".

## Funcionalidade: Pesquisar Anúncios por Produtos
  Como usuário do sistema   
  Quero pesquisar Anúncios por Produtos

### Cenários Válidos:

#### Listar Produtos disponíveis
    Dado que o usuário está na tela de Interesses
    E clica no botão "Anúncios"
    E clica na aba "Por Produtos"
    O sistema deverá listar todos os produtos anunciados com saldo disponível e com da data de expiração do anúncio maior ou igual DATA_HORA_ATUAL
    E habilitar o botão "Anunciante" para cada um dos itens de produtos cujo anúncio permite a visualização dos Dado do anunciante.

## Funcionalidade: Registrar Interesse por Produto Anunciado
  Como usuário do sistema   
  Quero lançar um novo Interesse

### Cenários Válidos:
#### Interessar por Produto
    Dado que o usuário está na tela de Interesses
    E clica no botão "Anúncios"
    E clica na aba "Por Produtos"
    E expande um item da listagem de produtos
    E clica no botão "Interessar" do item
    O sistema deverá fechar o Modal Anúncios
    E lançar um novo registro de interesse
    E vincular o anúncio do produto selecionado na aba Anúncio
    E importar o item selecionado no Modal Anúncios para a listagem de produtos da aba principal.

## Funcionalidade: Pesquisar Produtos Anunciados Por Similares
  Como usuário do sistema   
  Quero lançar um novo Interesse

### Cenários Válidos:
#### Visualizar Produtos anunciados por Similar
    Dado que o usuário está na tela de Interesses
    E clica no botão "Anúncios"
    E clica na aba "Por Produtos"
    E expande um item da listagem de produtos
    E clica no botão "Similares"
    O sistema deverá limpar o filtro dos anúncios
    E adicionar uma pesquisa por Princípio Ativo com o valor do Princípio Ativo do item selecionado
    E recarregar a listagem.

#### Cenários Inválidos:
#### Clicar em Similares em item de produto sem Princípio Ativo vinculado
    Dado que o usuário está na tela de Interesses
    E clica no botão "Anúncios"
    E clica na aba "Por Produtos"
    E expande um item da listagem de produtos
    E clica no botão "Similares"
    E produto de item selecionado não possuir Princípio Ativo vinculado no cadastro
    O sistema deverá limpar o filtro da tela
    E recarregar a listagem padrão com todos os produtos disponíveis.

## Funcionalidade: Pesquisar Anúncios por Anunciante
  Como usuário do sistema   
  Quero lançar um novo Interesse

### Cenários Válidos:
####  Listar Anúncios disponíveis
    Dado que o usuário está na tela de Interesse
    E clica no botão Anúncios
    E clica na aba Por Anunciante
    O sistema deverá exibir todos os anúncios disponíveis, e também seus itens com saldo disponível, com data de expiração maior ou igual DATA_HORA_ATUAL
    E habilitar o botão "Anunciante" para cada anúncio que permite visualizar os Dado do anunciante.

## Funcionalidade: Visualizar Dado do Anunciante
  Como usuário do sistema   
  Quero lançar um novo Interesse

### Cenários Válidos:
#### Visualizar Dado do Anunciante na pesquisa Por Produto
    Dado que o usuário está na tela de Interesses
    E clica no botão "Anúncios"
    E clica na aba "Por Produtos"
    E expande um item da listagem de produtos
    E clica no botão "Anunciante"
    O sistema deverá exibir o modal "Dado do Anunciante".

#### Visualizar Dados do Anunciante na pesquisa Por Anunciante
    Dado que o usuário está na tela de Interesses
    E clica no botão "Anúncios"
    E clica na aba "Por Anunciantes"
    E expande um item da listagem de anúncios
    E clica no botão "Anunciante"
    O sistema deverá exibir o modal "Dados do Anunciante".

## Funcionalidade: Visualizar Anúncio
  Como usuário do sistema   
  Quero visualizar os Dado do anúncio

### Cenários Válidos:
#### Visualizar Anúncio na pesquisa Por Anunciante
    Dado que o usuário está na tela de Interesses
    E clica no botão "Anúncios"
    E clica na aba "Por Anunciantes"
    E expande um item da listagem de anúncios
    E clica no botão "Visualizar"
    O sistema deverá exibir o Modal "Dados do Anúncio"

## Funcionalidade: Importar Itens do Anúncio Visualizado
  Como usuário do sistema   
  Quero importar os itens do Anúncio visualizado

### Cenários Válidos:
#### Importar Todos os itens do Anúncio Visualizado
    Dado que o usuário está na tela de Interesse
    E clica no botão "Anúncios"
    E clica na aba "Por Anunciantes"
    E expande um item da listagem de anúncios disponíveis
    E clica no botão "Visualizar"
    E marca o check ao menos um item da listagem de produtos do anúncio
    E clica no botão "Importar"
    O sistema deverá fechar o Modal "Dados do Anúncio"
    E fecha o Modal "Anúncios"
    E inclui um novo lançamento de Interesse
    E vincula o anúncio selecionado na aba "Anúncio Vinculado"
    E importa todos os produtos selecionado no modal "Dados do Anúncio" para a listagem de produtos da aba principal do Interesse.
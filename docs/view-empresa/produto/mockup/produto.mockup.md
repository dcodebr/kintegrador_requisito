# Produto - Mockup

## View
![](pencil/svg/produto.svg)

## Ações
|Nome|Tipo de Controle|Descrição|
|---|:---:|---|
|**Filtrar**|Botão|Aciona o Modal de Filtro do módulo Produto|
|**Excluir**|Botão|Exclui um registro no módulo Produto|
|**Incluir**|Botão|Inclui um registro no módulo Produto|
|**Salvar**|Botão|Salva um registro do módulo Produto|

## Controles
|Nome|Tipo de Controle|Descrição|Obrigatório|Tamanho Max.|Validação|
|---|:---:|---|:---:|:---:|:---:|
|Código|Identidade|Identifica o registro|AUTO|-|-|
|Controle por lote|Checkbox|Controlar produto por lote|NÃO|-|Se selecionado habilita para a inserção de lotes do produto|
|Descrição|Caixa de Texto|Descrição do Produto|SIM|255|-|
|Estoque|Caixa de Texto|Estoque Total levando em consideração as quantidades dos lotes|SIM|-|-|
|Princípio Ativo|Caixa de Seleção|Princípio Ativo do Produto|SIM|255|-|
|Marca/Laboratório|Caixa de Seleção|Marcas dos Laboratórios do Produto|SIM|-|-|
|Unidade de Medida|Caixa de Seleção|Unidades de Medidas do Produto|SIM|-|-|

# Produto - Lote

## Ações
|Nome|Tipo de Controle|Descrição|
|---|:---:|---|
|**➕**|Botão|Inclui um registro no módulo Produto Lote|
|**❌**|Botão|Salva um registro do módulo Produto Lote|

## Controles
|Nome|Tipo de Controle|Descrição|Obrigatório|Tamanho Max.|Validação|
|---|:---:|---|:---:|:---:|:---:|
|Lote|Caixa de Texto|Informar a descrição do lote a ser incluído|NÃO|64|-|
|Data Fabricação|Caixa de Texto|Data que o produto foi fabricado|SIM|-|Validação de data "##/##/####"|
|Data Validade|Caixa de Texto|Data que o produto possui de valdiade|NÃO|-|Validação de data "##/##/####"|
|Quantidade|Caixa de Texto|Quantidade do produto do lote em questão|SIM|-|Validação se foi preenchido|
|-|Tabela|Lotes de Produtos vinculados ao Produto|SIM|-|<ol><li>Código</li><li>Lote</li><li>Data Fabricação</li><li>Data Validade</li><li>Qtde</li></ol>|

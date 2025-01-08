# Anuncio - Produto - Mockup

## View
![](../../mockup/pencil/svg/anuncio-produto.svg)

## Ações
|Nome|Tipo de Controle|Descrição|
|---|:---:|---|
|**Filtrar**|Botão|Aciona o Modal de Filtro do módulo Anuncio Produtos|
|**Excluir**|Botão|Exclui um registro no módulo Anuncio Produtos|
|**Incluir**|Botão|Inclui um registro no módulo Anuncio Produtos|
|**Salvar**|Botão|Salva um registro do módulo Anuncio Produtos|

## Controles
|Nome|Tipo de Controle|Descrição|Obrig.|Tam. Max.|Validação|
|---|:---:|---|:---:|:---:|:---:|
|Código|Identidade|Identifica o registro|AUTO|-|-|
|Data Cadastro|Caixa de Texto|Data do Cadastro do Anuncio|AUTO|-|-|
|Data Expiração|Caixa de Texto|Data de Expiração do Anuncio|NÃO|-|-|
|Reserva Saldo|Checkbox|Se marcado ocorrerá reserva do estoque|NÃO|-|-|
|Permite Acessar Inf. no Interesse|Checkbox|Se marcado permite ao usuário visualizar Empresa Anunciante no Interesse|NÃO|-|-|
|Remove Anuncio após Expiração|Checkbox|Se marcado, ocorrerá a exclusão do Anuncio assim que exceder a data expiração|NÃO|-|-|
|CodProduto|Caixa de Texto|Apresenta o código do Produto selecionado|SIM|-|-|
|Botão ...|Botão|Botão Pesquisa de Produto|NÃO|-|-|
|Descrição|Caixa de Texto|Apresenta a Descrição do Produto Selecionado|SIM|-|-|
|Qtde|Caixa de Texto|Quantidade a ser disponibilizada no Anuncio|SIM|-|-|
|UnMedida|Caixa de Seleção|Traz todas as unidades de medidas cadastradas no sistema|SIM|-|-|
|Valor Unitário|Caixa de Texto|Valor unitário do produto selecionado|SIM|-|-|
|Valor Total|Caixa de Texto|Valor unitário x qtde disponibilizada|AUTO|-|-|
|Botão + |Botão|Botão para Inclusão do Produto na Tabela de Visualização|SIM|-|-|
|Botão x |Botão|Botão para Exclusão do Produto na Tabela de Visualização|SIM|-|-|
|Tabela Produtos|Tabela|Trará as informações dos Produtos Incluidos no Anuncio|SIM|-|-|
|Qtde Total Produtos|Caixa de Texto|Traz a informação de quantidade total de produtos no Anuncio|AUTO|-|-|
|Total Anuncio|Caixa de Texto|Traz a informação de quantidade x valor unitário de todos os produtos incluidos na tabela de anuncio|AUTO|-|-|
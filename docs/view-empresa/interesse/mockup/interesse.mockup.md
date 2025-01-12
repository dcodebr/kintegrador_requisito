# Interesse - Mockup

## View
![](../../mockup/pencil/svg/interesse-aba-principal.svg)

## Ações 
|Nome|Tipo de Controle|Descrição|
|---|:---:|---|
|**Anúncios**|Botão|Abre o modal de Pesquisa de Anúncios por Produto|
|**Filtrar**|Botão|Abre o modal de filtro de Interesses|
|**Incluir**|Botão|Inclui um novo registro de Interesse|
|**Excluir**|Botão|Exclui o registro atual de Interesse|
|**Salvar**|Botão|Salva o registro atual de Interesse|

## Controles
|Nome|Tipo de Controle|Descrição|Obrig.|Tam. Max.|Validação|
|---|:---:|---|:---:|:---:|:---:|
|Aba Produtos|Aba de Pagina|Identifica a aba Principal|-|-|-|
|Aba Anúncio Vinculado|Aba de Pagina|Identifica a Anúncio Vinculado|-|-|-|
|Total Anunciado|Caixa de Texto|Exibe o total de produtos anunciados da aba Anúncio Vinculado|AUTO|-|Campo Numérico #,####0.0000|
|Total do Interesse|Caixa de Texto|Exibe o total de produtos do Interesse|AUTO|-|Campo Numérico #,####0.0000|

---

# Produtos do Interesse

## Controles
|Nome|Tipo de Controle|Descrição|Obrig.|Tam. Max.|Validação|
|---|:---:|---|:---:|:---:|:---:|
|Código|Caixa de Texto|Código do Produto|SIM|6|Campo Bloqueado|
|Descrição|Aba de Pagina|Descrição do Produto|SIM|255|Campo Bloqueado|
|Qtde|Aba de Pagina|Quantidade selecionada do Item do interesse|SIM|-|Campo Numérico #,####0.0000|
|Un|Aba de Pagina|Identifica a Aba a ser visualizada|-|-|Campo Bloqueado|
|Valor Un|Aba de Pagina|Informa o valor do item do interesse|-|-|<ul><li>Campo Bloqueado</li><li>Campo Numérico #,####0.0000</li></ul>|
|Valor Total|Caixa de Texto|Totaliza o valor do item do interesse|AUTO|-|Campo Numérico #,####0.0000|
|➕|Botão|Atualiza as informações o item do interesse|-|-|-|
|❌|Botão|Exclui um item do interesse|-|-|-|

---

# Aba Anúncio Vinculado

## View
![](../../mockup/pencil/svg/interesse-aba-anuncio-vinculado.svg)

## Controles
|Nome|Tipo de Controle|Descrição|Obrig.|Tam. Max.|Validação|
|---|:---:|---|:---:|:---:|:---:|
|Código|Caixa de Texto|Código do Anúncio|SIM|6|-|
|⋯|Botão|Carregamento da seleção do Anúncio|-|-|-|
|Data Cadastro|Caixa de Texto|Data de cadastro do Anúncio|AUTO|19|Campo de Data/Cadastro DD/MM/YYYY HH:mm:ss|
|Anunciante|Caixa de Texto|Nome/Razão Social do anunciante|AUTO|255|-|

---

# Produtos da Aba Anúncio Vinculado

## Controles
|Nome|Tipo de Controle|Descrição|Obrig.|Tam. Max.|Validação|
|---|:---:|---|:---:|:---:|:---:|
|Imp. Seleção|Botão|Importaos os itens selecionados de produtos do anúncio para a Aba Principal|-|-|-|
|Imp. Todos|Botão|Importa todos os produtos do anúncio para a Aba Principal|-|-|-|
|-|Tabela|Lista todos os produtos do anúncio|-|-|<ol><li>☑</li><li>Código</li><li>Descrição</li><li>Marca</li><li>Princípio Ativo</li><li>Un</li><li>Qtde</li><li>Valor Un</li><li>Valor Total</li></ol>|


---

# Pesquisa de Anúncios

## View
![](../../mockup/pencil/svg/interesse-pesquisa-por-produto.svg)

## Ações 
|Nome|Tipo de Controle|Descrição|
|---|:---:|---|
|**❌**|Botão|Fecha o Modal de Pesquisa Por Anúncios|
|**Filtrar**|Botão|Abre o Modal de Filtro de Anúncios|

## Controles
|Nome|Tipo de Controle|Descrição|Obrig.|Tam. Max.|Validação|
|---|:---:|---|:---:|:---:|:---:|
|Aba Produtos|Aba de Pagina|Aba de Listagem de produtos anunciados|-|-|-|
|Aba Anúncios|Aba de Pagina|Aba de Listagem de anúncios e anunciantes|-|-|-|

---

# Aba Produtos da Pesquisa de Anúncios

## View
![](../../mockup/pencil/svg/interesse-pesquisa-por-produto.svg)

## Ações 
|Nome|Tipo de Controle|Descrição|
|---|:---:|---|
|**Interessar**|Botão|Lança um novo registro de Interesse com o item em questão|
|**Anunciante**|Botão|Abre o Modal Dados do Anunciante|
|**Similares**|Botão|Modifica o Filtro do módulo para buscar itens com o mesmo princípio ativo do item em questão|

## Controles
|Nome|Tipo de Controle|Descrição|Obrig.|Tam. Max.|Validação|
|---|:---:|---|:---:|:---:|:---:|
|-|Tabela|Lista os produtos anunciados|-|-|<ol><li>Nome do Produto</li><li>Marca</li><li>Preço</li><li>Princípio Ativo</li><li>Qtde</li>Un<li></li><li>Interessar</li><li>Anunciante</li><li>Similares</li></ol>|
|Lotes|Tabela|Lista os Lotes de cada produto anunciado|-|-|<ol><li>Lote</li><li>Data Fabricação</li><li>Data Validade</li><li>Qtde</li></ol>|

---

# Aba Anúncios da Pesquisa por Anúncios

## View
![](../../mockup/pencil/svg/interesse-pesquisa-por-anunciante.svg)

## Ações 
|Nome|Tipo de Controle|Descrição|
|---|:---:|---|
|**Visualizar**|Botão|Abre o Modal de Visualização do Anúncio|
|**Anunciante**|Botão|Abre o Modal de Dados do Anunciante|

## Controles
|Nome|Tipo de Controle|Descrição|Obrig.|Tam. Max.|Validação|
|---|:---:|---|:---:|:---:|:---:|
|-|Tabela|Lista os anúncios disponíveis|-|-|<ol><li>Código do Anúncio</li><li>Anunciante</li><li>Valor Total</li><li>Visualizar</li><li>Anunciante</li></ol>|
|Produtos|Tabela|Lista itens de cada anúncio|-|-|<ol><li>Código</li><li>Descrição</li><li>Marca</li><li>Princípio Ativo</li><li>UN</li><li>Qtde</li><li>Valor Un</li><li>Valor Total</li></ol>|

---

# Dados do Anunciante

## View
![](../../mockup/pencil/svg/interesse-pesquisa-dados-anunciante.svg)

## Ações 
|Nome|Tipo de Controle|Descrição|
|---|:---:|---|
|**❌**|Botão|Fecha o Modal Dados do Anunciante|

## Controles
|Nome|Tipo de Controle|Descrição|Obrig.|Tam. Max.|Validação|
|---|:---:|---|:---:|:---:|:---:|
|Empresa|Texto|Exibe o nome/razão social do Anunciante|-|-|-|
|CNPJ|Texto|Exibe o CNPJ do Anunciante|-|-|-|
|Endereço|Texto|Exibe o endereço e número do Anunciante|-|-|-|
|Cidade|Texto|Exibe a cidade do Anuciante|-|-|-|
|UF|Texto|Exibe Unidade Federativa do Anunciante|-|-|-|
|CEP|Texto|Exibe o CEP do Anunciante|-|-|-|
|Telefone|Texto|Exibe o telefone do Anunciante|-|-|-|
|Email|Texto|Exibe o e-mail de contato do Anunciante|-|-|-|
---

# Dados do Anúncio

## View
![](../../mockup/pencil/svg/interesse-pesquisa-por-anunciante-anuncio.svg)

## Ações 
|Nome|Tipo de Controle|Descrição|
|---|:---:|---|
|**❌**|Botão|Fecha o Modal Dados do Anúncio|
|**Anunciante**|Botão|Abre o Modal Dados do Anunciante|

## Controles
|Nome|Tipo de Controle|Descrição|Obrig.|Tam. Max.|Validação|
|---|:---:|---|:---:|:---:|:---:|
|Código|Texto|Exibe o código do Anúncio|-|-|-|
|Data Cadastro|Texto|Exibe a data de Cadastro do Anúncio|-|-|-|
|Data Expiração|Texto|Exibe a Data de Expiração do Anúncio|-|-|-|
|Produtos|Texto|Lista os itens de produtos do Anúncio|-|-|<ol><li>☑</li><li>Código</li><li>Descrição</li><li>Marca</li><li>Princípio Ativo</li><li>Un</li><li>Qtde</li><li>Valor Un</li><li>Valor Total</li></oi>|
|Total Selecionado|Caixa de Texto|Totaliza o valor dos itens selecionados pela caixa de seleção ☑|AUTO|-|Valor numérico #,####0.0000|
|Total Anúncio|Caixa de Texto|Totaliza o valor de todos os itens do Anúncio|AUTO|-|Valor numérico #,####0.0000|
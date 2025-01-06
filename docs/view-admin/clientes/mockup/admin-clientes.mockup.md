# Clientes - Mockup

## View
![](pencil/svg/admin-clientes.svg)

## Ações
|Nome|Tipo de Controle|Descrição|
|---|:---:|---|
|**Filtrar**|Botão|Aciona o Modal de Filtro do módulo Clientes|
|**Excluir**|Botão|Exclui um registro no módulo Clientes|
|**Incluir**|Botão|Inclui um registro no módulo Clientes|
|**Salvar**|Botão|Salva um registro do módulo Clientes|

## Controles
|Nome|Tipo de Controle|Descrição|Obrigatório|Tamanho Max.|Validação|
|---|:---:|:---:|:---:|---|---|
|Código|Identidade|Identifica o registro|AUTO|-|-|
|Nome|Caixa de Texto|Nome/Razão Social do cliente|SIM|255||
|CNPJ|Caixa de Texto|CNPJ do cliente|SIM|14|Validação do CNPJ|
|CEP|Caixa de Texto|CEP do Endereço do cliente|SIM|10|Deve preencher demais campos do endereço|
|Endereço|Caixa de Texto|Endereço do cliente|SIM|255||
|Número|Caixa de Texto|Número do Logradouro do cliente|SIM|50||
|Bairro|Caixa de Texto|Bairro do endereço do cliente|SIM|255||
|Complemento|Caixa de Texto|Complemento do endereço do cliente|NÃO|100||
|Cidade|Caixa de Seleção|Cidade do cliente|SIM|-|Cidade deve pertencer a UF|
|UF|Caixa de Seleção|UF da cidade do cliente|SIM|-|UF deve estar vinculada à cidade|
|Telefone|Caixa de Texto|telefone principal do cliente|SIM|20|-|
|E-mail|Caixa de Texto|E-mail principal do cliente|SIM|100|S|
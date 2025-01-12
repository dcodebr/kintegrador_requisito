# /empresa

## Rotas
- GET /
- GET/{id}
- POST /
- PUT/{id}
- DELETE/{id}

---

## Modelos de Requisição
### GET /:
#### Descrição: 
Lista todos os objetos **[Empresa]** cadastrados no sistema
#### Envio:

```text
    /
```

#### Resposta:
***Body/JSON:***
```json
    [
        {
            "codigo": Number,
            "nome": String,
            "CNPJ": String,
            "CEP": String,
            "Endereco": String,
            "Numero": String,
            "Bairro": String,
            "Complemento": String,
            "Cidade": String,
            "UF": String,
            "Telefone": String,
            "Email": String
        },
        {
            "codigo": Number,
            "nome": String,
            "CNPJ": String,
            "CEP": String,
            "Endereco": String,
            "Numero": String,
            "Bairro": String,
            "Complemento": String,
            "Cidade": String,
            "UF": String,
            "Telefone": String,
            "Email": String
        }
    ]
```

#### Códigos de Respostas HTTP:
* **200 OK:** Requisição bem-sucedida.
* **204 No Content:** Nenhum registro encontrado para os filtros fornecidos.
* **500 Internal Server Error:** Erro interno no servidor.

---

### GET /{id}:
#### Descrição: 
Retorna um objeto de **[Empresa]** baseado no {Id} informado por Router Parameter

#### Parâmetro de Rota: 
(obrigatório) Identificador único do objeto de **[Empresa]** que será atualizada.
```text
    /{id}
```

#### Resposta:
***Body/JSON:***
```json
    [
        {
            "codigo": Number,
            "nome": String,
            "CNPJ": String,
            "CEP": String,
            "Endereco": String,
            "Numero": String,
            "Bairro": String,
            "Complemento": String,
            "Cidade": String,
            "UF": String,
            "Telefone": String,
            "Email": String
        }
    ]
```

#### Códigos de Respostas HTTP:
* **200 OK:** Requisição bem-sucedida.
* **204 No Content:** Nenhum registro encontrado para os filtros fornecidos.
* **500 Internal Server Error:** Erro interno no servidor.

---

### POST /: 
#### Descrição: 
Envia o objeto de **[Empresa]** novo para o banco de dados
#### Envio:

```json
    [
        {
            "nome": String,
            "CNPJ": String,
            "CEP": String,
            "Endereco": String,
            "Numero": String,
            "Bairro": String,
            "Complemento": String,
            "Cidade": String,
            "UF": String,
            "Telefone": String,
            "Email": String
        }
    ]
```

#### Resposta:
Se a solicitação for bem-sucedida, o servidor retorna uma lista de objetos de **[Empresa]** no seguinte formato:  
***Body/JSON:***
```json
    [
        {
            "codigo": Number,
            "nome": String,
            "CNPJ": String,
            "CEP": String,
            "Endereco": String,
            "Numero": String,
            "Bairro": String,
            "Complemento": String,
            "Cidade": String,
            "UF": String,
            "Telefone": String,
            "Email": String
        }
    ]
```

#### Códigos de Respostas HTTP:
* **201 Created:** O recurso foi criado com sucesso.
* **200 OK:** O recurso foi criado com sucesso e uma resposta é retornada (menos comum que 201).
* **400 Bad Request:** A solicitação foi malformada ou contém dados inválidos.
* **401 Unauthorized:** A autenticação é necessária e não foi fornecida ou é inválida.
* **403 Forbidden:** O cliente não tem permissão para criar o recurso.

---

### PUT /{id}:
#### Descrição: 
Atualiza as informações de um objeto de **[Empresa]** existente no banco de dados com base no {id} fornecido por Router Parameter

#### Parâmetro de Rota: 
(obrigatório) Identificador único de objeto de **[Empresa]** que será atualizada.
```text
    /{id}
```

#### Envio:
```json
    [
        {
            "nome": String,
            "CNPJ": String,
            "CEP": String,
            "Endereco": String,
            "Numero": String,
            "Bairro": String,
            "Complemento": String,
            "Cidade": String,
            "UF": String,
            "Telefone": String,
            "Email": String
        }
    ]
```

#### Resposta:
Caso a atualização seja bem-sucedida, o servidor retornará o objeto atualizado no seguinte formato:  
**Body/JSON:**
```json
    [
        {
            "codigo": Number,
            "nome": String,
            "CNPJ": String,
            "CEP": String,
            "Endereco": String,
            "Numero": String,
            "Bairro": String,
            "Complemento": String,
            "Cidade": String,
            "UF": String,
            "Telefone": String,
            "Email": String
        }
    ]
```

#### Códigos de Resposta HTTP:
* **200 OK:** Atualização bem-sucessidade.
* **400 Bad Request:** Requisição inválida ou campos incorretos.
* **404 Not Found:** Registro não encontrada com o ID fornecido.
* **500 Internal Server Error:** Erro interno no servidor

---

### DELETE /{id}:
#### Descrição: 
Remove as informações de um objeto de **[Empresa]** existente no banco de dados com base no {id} fornecido por Router Parameter

#### Parâmetro de Rota: 
(obrigatório) Identificador único do objeto de **[Empresa]** que será excluído.
```text
    /{id}
```

#### Envio:
```json
    [
        {
            "codigo": Number
        }
    ]
```

#### Resposta:
Caso a atualização seja bem-sucedida, o servidor retornará uma mensagem de código:  
**Body/JSON:**
```json
    [
        {
            "mensagem": "Empresa excluída com sucesso."
        }
    ]
```

#### Códigos de Resposta HTTP:
* **200 OK:** O registro foi excluído com sucesso e uma mensagem de confirmação é retornada.
* **204 No Content:** O Registro foi excluído com sucesso, sem corpo de resposta.
* **400 Bad Request:** A solicitação foi malformada ou o parâmetro de rota é inválido.
* **401 Unauthorized:** O cliente não está autenticado para realizar a exclusão.
* **403 Forbidden:** O cliente não tem permissão para excluir o registro.
* **404 Not Found:** Nenhum registro encontrado com o id informado.
* **409 Conflict:** O recurso não pode ser excluído porque está em uso (ex.: relacionamentos pendentes).
* **500 Internal Server Error:** Ocorreu um erro inesperado no servidor.

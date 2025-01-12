# /usuario

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
Lista todos os objetos **[Unidade de Medida]** cadastrados no sistema
#### Envio:

```text
    /
```

#### Resposta:
***Body/JSON:***
```json
    [
        {
            "Codigo": Number,
            "Descricao": String,
            "Sigla": String
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
Retorna um objeto **[Unidade de Medida]** baseado no {Id} informado por Router Parameter

#### Parâmetro de Rota: 
(obrigatório) Identificador único do objeto **[Unidade de Medida]** que será atualizado.
```text
    /{id}
```

#### Resposta:
***Body/JSON:***
```json
    [
        {
            "Codigo": Number,
            "Descricao": String,
            "Sigla": String
        }
    ]
```

#### Códigos de Respostas HTTP:
* **200 OK:** Requisição bem-sucedida.
* **204 No Content:** Nenhum usuário encontrado para os filtros fornecidos.
* **500 Internal Server Error:** Erro interno no servidor.

---

### POST /: 
#### Descrição: 
Envia o objeto **[Unidade de Medida]** novo para o banco de dados
#### Envio:

```json
    [
        {
            "Descricao": String,
            "Sigla": String
        }
    ]
```

#### Resposta:
Se a solicitação for bem-sucedida, o servidor retorna uma lista dos objetos **[Unidade de Medida]** no seguinte formato:  
***Body/JSON:***
```json
    [
        {
            "Codigo": Number,
            "Descricao": String,
            "Sigla": String
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
Atualiza as informações de um objeto **[Unidade de Medida]** existente no banco de dados com base no {id} fornecido por Router Parameter

#### Parâmetro de Rota: 
(obrigatório) Identificador único do objeto **[Unidade de Medida]** que será atualizado.
```text
    /{id}
```

#### Envio:
```json
    [    
        {
            "Descricao": String,
            "Sigla": String
        }
    ]
```

#### Resposta:
Caso a atualização seja bem-sucedida, o servidor retornará o objeto atualizado no seguinte formato:  
**Body/JSON:**
```json
    [
        {
            "Codigo": Number,
            "Descricao": String,
            "Sigla": String
        }
    ]
```

#### Códigos de Resposta HTTP:
* **200 OK:** Atualização bem-sucessidade.
* **400 Bad Request:** Requisição inválida ou campos incorretos.
* **404 Not Found:** Empresa não encontrada com o ID fornecido.
* **500 Internal Server Error:** Erro interno no servidor

---

### DELETE /{id}:
#### Descrição: 
Remove as informações de um objeto **[Unidade de Medida]** existente no banco de dados com base no {id} fornecido por Router Parameter

#### Parâmetro de Rota: 
(obrigatório) Identificador único do objeto **[Unidade de Medida]** que será excluído.
```text
    /{id}
```

#### Envio:
```json
    [
        {
            "Codigo": Number
        }
    ]
```

#### Resposta:
Caso a atualização seja bem-sucedida, o servidor retornará uma mensagem de código:  
**Body/JSON:**
```json
    [
        {
            "mensagem": "Unidade de Medida excluída com sucesso."
        }  
    ]
```

#### Códigos de Resposta HTTP:
* **200 OK:** O regigstro foi excluído com sucesso e uma mensagem de confirmação é retornada.
* **204 No Content:** O Registro foi excluída com sucesso, sem corpo de resposta.
* **400 Bad Request:** A solicitação foi malformada ou o parâmetro de rota é inválido.
* **401 Unauthorized:** O cliente não está autenticado para realizar a exclusão.
* **403 Forbidden:** O cliente não tem permissão para excluir o registro.
* **404 Not Found:** Nenhum registro encontrada com o id informado.
* **409 Conflict:** O recurso não pode ser excluído porque está em uso (ex.: relacionamentos pendentes).
* **500 Internal Server Error:** Ocorreu um erro inesperado no servidor.

# Geral

## Estrutura
1. [Mockup](mockup/admin-tokens.mockup.md)
2. [Regras de Negócio](regras%20de%20negócio/admin-tokens.bdd.md)

## Resumo
A tela de informações de empresas e tokens de acesso é projetada para exibir e gerenciar os dados básicos das empresas (CNPJ e Razão Social), bem como os tokens associados a elas.   
Cada empresa pode ter múltiplos tokens, que são utilizados para autenticação e controle de acesso a determinados serviços ou APIs.  
Essa funcionalidade é essencial para garantir segurança e rastreabilidade no acesso aos recursos do sistema.

## Objetivo
O objetivo dessa tela é fornecer uma interface centralizada para:

* Visualizar informações básicas das empresas cadastradas (CNPJ e Razão Social).  
* Gerenciar tokens de acesso vinculados a cada empresa, incluindo:  
    - **Criação de novos tokens** com dados personalizados (código, descrição, etc.).  
    - **Consulta de informações de tokens**, como data de criação e expiração.  
    - **Controle de ações sobre os tokens**, como copiar, atualizar ou excluir.
* Garantir que os tokens sejam gerados de forma segura (hash) e que possam ser reutilizados ou revogados conforme necessário.

## Mensagens e Erros
* **Ao copiar um token:** "Token copiado para a área de transferência com sucesso."  
* **Ao excluir um token:** "Você tem certeza de que deseja excluir este token? Esta ação não pode ser desfeita."  
* **Validação de campos obrigatórios:** "O campo [Descrição] é obrigatório e deve ser preenchido."  
* **Erro na geração do token:** "Erro ao gerar o token. Tente novamente mais tarde."  


## Permissões
* Apenas administradores ou usuários com permissões específicas podem criar, editar ou excluir tokens.
* Usuários com permissões de leitura podem visualizar as informações, mas não realizar alterações. (Confirmar com Alex, se as Empresas terão acesso a visualização das informações dessa tela)
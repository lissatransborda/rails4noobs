# Criando Resources

Uma *resource* é o conjunto de objetos parecidos, com ela, poderemos criar um *Controller* e fazer CRUD neste *Controller*, assim poderemos criar, remover, editar,etc items do nosso banco de dados.

Para criarmos uma resource é bem simples, abra ``config/routes.tb`` e digite:

```ruby
Rails.application.routes.draw do
  get 'welcome/index'
 
  resources :artigos
 
  root 'welcome#index'
end
```

Agora execute o comando ``rails routes`` para ver as rotas do *resource* que você acabou de criar, de criação, remoção, edição,etc. Você verá algo parecido com isso:

``
       Prefix Verb   URI Pattern                  Controller#Action
welcome_index GET    /welcome/index(.:format)     welcome#index
     artigos GET    /artigos(.:format)          artigos#index
              POST   /artigos(.:format)          artigos#create
  new_artigo GET    /artigos/new(.:format)      artigos#new
 edit_artigo GET    /artigos/:id/edit(.:format) artigos#edit
      artigo GET    /artigos/:id(.:format)      artigos#show
              PATCH  /artigos/:id(.:format)      artigos#update
              PUT    /artigos/:id(.:format)      artigos#update
              DELETE /artigos/:id(.:format)      artigos#destroy
         root GET    /                            welcome#index
``

Pronto! Criamos uma nova *Resource*, dessa maneira que poderemos fazer CRUD dos dados.

## Proximo =>

[Inserindo Dados](../inserindo-dados/README.md)
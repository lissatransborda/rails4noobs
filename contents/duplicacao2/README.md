# Removendo Duplicação de Código Novamente

Agora temos dois formulários na nossa aplicação, o formulário de criação do artigo e o formulário de criação de um novo comentário, agora vamos separar o formulário de criação de um novo comentário á um arquivo externo, pois assim, nossa aplicação ficará mais organizada e com um código mais simples.

Crie o arquivo ``apps/views/comentarios/_form.html.erb`` e escreva:

```ruby
<%= form_with(model: [ @artigo, @artigo.comentarios.build ], local: true) do |form| %>
  <p>
    <%= form.label :comentarista %><br>
    <%= form.text_field :comentarista %>
  </p>
  <p>
    <%= form.label :corpo %><br>
    <%= form.text_area :corpo %>
  </p>
  <p>
    <%= form.submit %>
  </p>
<% end %>
```

Lembrando que este é o mesmo conteúdo do formulário de comentários da view show do artigos.

Agora edite o arquivo ``app/views/comentarios/_comentario.html.erb`` e coloque o conteúdo:

```ruby
<% @artigo.comentarios.each do |comentario| %>
  <p>
    <strong>Comentarista:</strong>
    <%= comentario.comentarista %>
  </p>
 
  <p>
    <strong>Comentario:</strong>
    <%= comentario.corpo %>
  </p>
<% end %>
```

Agora edite o arquivo ``app/views/artigos/show.html.erb`` e substitua o form de comentários por um render.

```ruby
<p>
  <strong>Título:</strong>
  <%= @artigo.titulo %>
</p>
 
<p>
  <strong>Texto:</strong>
  <%= @artigo.texto %>
</p>

<%= render @artigo.comentarios %>

<h2>Adicionar um comentário:</h2>

<%= render 'comentarios/form' %>

<%= link_to "Voltar", artigos_path %>
```

Quando nós temos uma associação como essa, um artigo que tem vários comentários, mas um comentário só pode ter um artigo, e criamos uma view que no caso, está dentro dos comentários e se chama ``_comentario.rb`` na hora de renderizarmos, podemos usar ``@artigo.comentarios``, de maneira mais simples e usual.

Pronto! separamos o formulário de comentários em um arquivo separado e o arquivo que mostra os comentários em um outro arquivo.

## Proximo =>

[Deletando Comentários](contents/deletando-comentarios/README.md)
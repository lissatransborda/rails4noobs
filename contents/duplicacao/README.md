# Removendo Duplicação em Arquivos

Nas etapas anteriores, criamos um formulário de criação e outro de edição, mas os dois são iguais, como podemos tirar essa duplicação no código e deixar apenas um único formulário que será ultilizado pelos dois?

Crie o arquivo ``apps/views/artigos/_form.html.erb`` e coloque o conteúdo do formulário de edição, dessa maneira:

```ruby
<%= form_with(model: @artigo, local: true) do |form| %>
 
  <% if @artigo.errors.any? %>
    <div id="error_explanation">
      <h2>
        <%= pluralize(@artigo.errors.count, "error") %> Probido de ser salvo este artigo pois:
      </h2>
      <ul>
        <% @artigo.errors.full_messages.each do |msg| %>
          <li><%= msg %></li>
        <% end %>
      </ul>
    </div>
  <% end %>
 
  <p>
    <%= form.label :titulo %><br>
    <%= form.text_field :titulo %>
  </p>
 
  <p>
    <%= form.label :texto %><br>
    <%= form.text_area :texto %>
  </p>
 
  <p>
    <%= form.submit %>
  </p>
 
<% end %>
```

Como este formulário é um componente que será re-ultilizado, use o _ antes do nome.

Agora abra os dois arquivos, a view de criação e a view de edição e substitua todo o conteúdo do formulário, por ``<%= render 'form' %>``, dessa maneira:

view da criação:

```ruby
<%= render 'form' %>
 
<%= link_to 'Voltar', artigos_path %>
```

view de edição:

```ruby
<h1>Editar artigo</h1>
 
  <%= render 'form' %>
 
<%= link_to 'Voltar', artigos_path %>
```

Pronto! modficamos e agora, a quantidade de código diminuiu, a repetição também, e a simplicidade aumentou, facilidade de escalar o código.
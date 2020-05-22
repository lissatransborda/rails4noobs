# Estrutura de pastas do Rails

Você viu que dentro do blog (pasta) há muitas pastas e arquivos, mas, o que significam essas pastas e arquivos?

Cada uma dessas pastas e arquivos tem uma função específica, como configurações, interfaces,etc. Para isso, temos esta tabela abaixo que explica a função de cada pasta e arquivo que o Rails cria por padrão:

| Arquivo/Pasta | Função |
|:--------------|-------:|
|app/ |Armazena os controllers, models, views, helpers, mailers, channels, jobs e assets da sua aplicação, a maior parte do trabalho e arquivos da sua aplicação estaram aqui.
|bin/ | Armazena os scripts Rails da sua aplicação, como o server, para iniciar o servidor
|config/ | Configura as rotas, bancos de dados e mais da sua aplicação
|config.ru | Configuração do Rack
|db/ | Armazena o schema do banco de dados e as migrations, no nosso caso, o SQLite estará aqui.
| Gemfile e Gemfile.lock | Determinam as dependências que são necessárias na nossa aplicação Rails
| lib/ | Módulos (bibliotecas) da nossa aplicação
| log/ | Arquivos de log
| packeage.json | Determina quais dependências do Node serão usadas
| public/ | Arquivos compilados e assets compilados
| Rakefile | Localiza e determina as tarefas que podem ser feitas pelo Rake
| README.md | Arquivo que descreve o que aquela aplicação faz ou serve
| storage/ | Active Storage para o Disk Service
| test/ | diretório para testes
| tmp/ | arquivos temporários, como cache
| vendor/ | Armazena todo o código de terceiros
| .gitignore | Arquivos que serão ignorados pelo git
| .ruby-version | Armazena a versão do Ruby usada no projeto

A maioria dessas pastas e arquivos não serão usadas neste 4noobs, a lista cita TODAS por efeitos de conhecimento, você não precisa decorar, pois você irá aos poucos entender melhor a função de algumas pastas e arquivos citados acima.

## Proximo

[Hello World no Rails](../hello-world/README.md)
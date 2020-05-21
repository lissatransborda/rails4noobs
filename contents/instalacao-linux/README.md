# Instalando Ruby on Rails no Linux

Instalar o Ruby on Rails no Linux é bem simples, use o terminal para instalar o Ruby usando o seu gerenciador de pacotes.

Também teremos que instalar além do Ruby, o Node, Yarn e SQLite, o Node e o Yarn envolvem o Javascript que será usado pelo Rails, você não precisa saber de Javascript para programar em Rails, e o SQLite será o banco de dados local que será usado por padrão pelo Rails, mas você pode usar qualquer um depois que aprender Rails, como MySQL e PostgreSQL

## Debian, Ubuntu, Linux Mint e Derivados

para instalar o Ruby e o Ruby Gems faça:

``sudo apt install ruby sqlite3 yarn nodejs``

## Fedora

faça:

``sudo dnf install ruby sqlite3 yarn nodejs``

## Arch

faça:

``sudo pacman -Syu ruby sqlite3 yarn nodejs``

# Gentoo

faça:

``sudo emerge dev-lang/ruby dev-db/sqlite nodejs sys-apps/yarn``

# Rails

Para instalar o Ruby on Rails em seu sistema, use o Gems para isso:

``gem install rails``

E pronto! teste se o rails foi corretamente instalado com:

``rails -v``

Caso apareça a versão instalada do Rails, está tudo funcionando corretamente.

## Proximo =>

[Criar Projeto em Rails](../criar-projeto/README.md)
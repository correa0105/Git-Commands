# CursoGit

Aqui vou deixar alguns comandos utilizados no Bash para trabalhar com Git

## Comandos para ZSH

##### cd : Entrar no diretório especifco

## Configurar SSH

##### ssh-keygen -t ed25519 -C "your_email@example.com" : Gerando uma SSH
##### cat ed25519.pub : Coletar a key gen para configurar no repositório Online
##### eval "$(ssh-agent -s)" : Para iniciar o agente em segundo plano

##### Antes de adicionar a chave ao agente, é necessário configurar o o arquivo config dentro de .ssh/

> touch ~/.ssh/config
> open config

Editar o texto colocando a seguinte configuração

Host *.github.com
  AddKeysToAgent yes
  UseKeychain yes
  IdentityFile ~/.ssh/id_ed25519

##### ssh-add --apple-use-keychain ~/.ssh/id_ed25519 : Para adicionar a chave ao agente

## Comandos Git
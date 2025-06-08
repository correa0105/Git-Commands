# Comandos Git

Aqui vou deixar alguns comandos utilizados no Bash para trabalhar com Git

## Comandos para ZSH

##### cd : Entrar no diretório especifco
##### rm -rf : Para excluir um diretório
##### mkdir : Para crair um diretório
##### mv : Para mover um arquivo

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

##### git init : Inicia o repositório
##### git add : "Prepara" o arquivo para comitar (Staged)
##### git commit -m : Comita os arquivos que estavam no Staged
##### git status : Verifica o status dos arquivos, untracked, tracked e staged
##### git config : Configura o git, como o user.name, user.email, use a flag --list para ver as configurações
##### git remote add origin : Adiciona um repositório remoto
##### git remote -v : Visualiza os repositórios remotos configurados

> Antes de dar push para o repositório remoto, no caso do GitHub, é necessário mudar o master do Git para main, entrando no .git e mudando o HEAD.

##### git push origin main : Envia o commit para origin (repositório remoto) para a branch main

> Se der algum conflito, será necessário realizar um pull

##### git pull origin main : Puxa o repositório da origin para a main

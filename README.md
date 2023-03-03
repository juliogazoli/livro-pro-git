# [Livro Pro Git](https://git-scm.com/book/pt-br/v2)

# Comandos Git

## Configurar usuário
``` sh
git config --global user.name "Fulano de Tal"
```

## Configurar e-mail
``` sh
git config --global user.email fulanodetal@exemplo.br
```

## Configurar editor
``` sh
git config --global core.editor emacs
```

## Listar configurações
``` sh
git config --list
```

## Ajuda
``` sh
git help config
```

## Inicializar repositório
``` sh
git init
```

## Adicionar arquivos ao monitoramento
``` sh
git add
```

## Clonar repositório existente
``` sh
git clone https://github.com/libgit2/libgit2
```

## Verificar Status
``` sh
git status
```

## Status curto
``` sh
git status --short
git status -s
```

## Visualizar alterações (alterado mas ainda não enviado para o stage)
``` sh
git diff
```

## Visualizar alterações (alterado e enviado para o stage, entrarão no próximo commit)
``` sh
git diff --staged
git diff --cached
```

## Visualizar alterações lado a lado
``` sh
git difftool --tool=vimdiff
```

## Fazer Commit (abre o editor)
``` sh
git commit
```

## Fazer Commit (incluir diff no commit)
``` sh
git commit -v
```

## Fazer Commit (incluir mensagem diretamente)
``` sh
git commit -m "mensagem de commit"
```

## Fazer Commit (pular a área de stage)
``` sh
git commit -a -m "mensagem de commit"
```

## Remover arquivo (preparado para remoção - retirado do stage)
``` sh
git rm arquivo
```

## Remover arquivo (já na área de stage)
``` sh
git rm -f arquivo
```

## Remover arquivo (manter o arquivo no seu diretório de trabalho, mas removê-lo da sua área de stage)
``` sh
git rm --cached arquivo
```

## Renomear arquivo
``` sh
git mv arq_origem arq_destino
```

## Log de commits
``` sh
git log
```

## Mostra o log de commits com o diff após cada item
``` sh
git log -p
```

## Mostra o log dos últimos 2 itens
``` sh
git log -2
```

## Log com estatísticas
``` sh
git log --stat
```

## Log formatado, um commit por linha
``` sh
git log --pretty=oneline
```

## Log com formatação customizada
``` sh
git log --pretty=format:"%h - %an, %ar : %s"
```

```
 Opção   Descrição da saída
------ |--------------------
  %H 	 Hash do commit
  %h 	 Hash do commit abreviado
  %T 	 Hash da árvore
  %t 	 Hash da árvore abreviado
  %P 	 Hashes dos pais
  %p 	 Hashes dos pais abreviado
  %an 	 Nome do Autor
  %ae 	 Email do Autor
  %ad 	 Data do Autor (o formato segue a opção --date=option)
  %ar 	 Data do Autor, relativa
  %cn 	 Nome do Committer
  %ce 	 Email do Committer
  %cd 	 Data do Committer
  %cr 	 Data do Committer, relativa
  %s 	 Comentário
  ```


## Log com gráfico de Branch e Merge
``` sh
git log --pretty=format:"%h %s" --graph
```

## Log com limitação de data relativa
``` sh
git log --since=2.weeks
```

## Log com commits adicionando ou removendo o código que corresponde à string
``` sh
git log -Sfunction_name
```

## Retirar arquivo do stage
``` sh
git reset HEAD <file>
git restore --staged <file>
```

## Exibir repositórios remotos
``` sh
git remote
```

## Exibir repositórios remotos com URLs
``` sh
git remote -v
```

## Adicionar repositório remoto
``` sh
git remote add <shortname> <url>

# Exemplo: 
git remote add pb https://github.com/paulboone/ticgit
git fetch pb
```

## Buscando e obtendo de repositórios remotos
``` sh
git fetch [remote-name]
```

## Buscar(fetch) e Mesclar(merge)
``` sh
git pull
```

## Enviar para o servidor remoto
``` sh
git push [remote-name] [branch-name]

# Exemplo:
git push origin master
```

## Inspecionar servidor remoto
``` sh
git remote show [nome-remoto]

# Exemplo:
git remote show origin
```

## Renomear servidor remoto
``` sh
git remote rename nome_antigo nome_novo
```

## Remover servidor remotos
``` sh
git remote remove nome_servidor
git remote rm nome_servidor
```

## Listar Tags
``` sh
git tag
```

## Listar Tag específica
``` sh
git tag -l "v1.8.5*"
```

## Tag anotada (checksum, nome, e-mail e data)
``` sh
git tag -a v1.4 -m "my version 1.4"
```

## Ver dados da Tag com o commit
``` sh
git show v1.4
```

## Tag leve (checksum)
``` sh
git tag v1.4
```

## Criar Tag posteriormente (informar checksum)
``` sh
git tag -a v1.2 9fceb02
```

## Compartilhar Tag específica
``` sh
git push origin v1.5
```

## Compartilhar todas as Tags
``` sh
git push origin --tags
```

## Deixar versão do repositório idêntica a uma tag
``` sh
git checkout -b [branchname] [tagname]

# Exemplo:
git checkout -b version2 v2.0.0
```

## Apelidos (aliases)
``` sh
git config --global alias.co checkout
git config --global alias.br branch
git config --global alias.ci commit
git config --global alias.st status
git config --global alias.unstage 'reset HEAD --'
git config --global alias.last 'log -1 HEAD'
git config --global alias.visual '!gitk'
```

## Branchs

## Criar Branch
``` sh
git branch testing
```

## Visualizar Branch atual
``` sh
git log --oneline --decorate
```

## Alternar entre Branches
``` sh
git checkout testing
```

## Verificar histórico e Branches
``` sh
git log --oneline --decorate --graph --all
```

## Criar novo Branch e mudar para ele
``` sh
git checkout -b chamado53
```

## Merge da Branch dev para master
``` sh
git checkout master
git merge dev
```

## Remover Branch
``` sh
git branch -d chamado53
```

## Ferramenta gráfica para resolver conflitos
``` sh
git mergetool
```

## Listar Branches
``` sh
git branch
```

## Listar Brnaches com o último commit
``` sh
git branch -v
```

## Remover Branch ainda não mesclado
``` sh
git branch -D chamado53
```

## Obter lista de referências remotas
``` sh
git ls-remote [remote]
	# ou
git remote show [remote]
```

## Sincronizar trabalho
``` sh
git fetch origin
```

## Enviar arquivos ao servidor remoto
``` sh
git push <remote> <branch>

# Exemplo:
git push origin master
```

pág. 90

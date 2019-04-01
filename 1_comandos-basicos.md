# Criando um repositório

```
#Cria repositório
$ git init

#Adicionar informações de usuário
$ git config --global user.name "Seu nome"
$ git config --global user.email "seu@email.com"
```
&nbsp;

# Configurar repositório
```
#Editor padrão
$ git config --global core.editor SeuEditor

#Adicionar templete para commit
$ git config --global commit.templete ~/SeuTemplete.txt

#Usar saída colorida
$ git config color.ui true

#Exibir log em apenas uma linha por commit
$ git config format.pretty oneline


#Git é case insensitive Pessoa == PESSOA
$ git config --global core.ignorecase false

```
&nbsp;

# Adicionar repositório
```
#ssh
$ git remote add teste git@github.com:leandro/teste.git

#https
$ git remote add teste https://www.github.com/leoalves100/teste.git
```
&nbsp;

# Adicionar arquivos
```
#Um arquivo
$ git add arquivo.php

#Por extensão
$ git add *.php

#Todos
$ git add .

#Modo interativo
$ git add -i
```
&nbsp;

# Commit
```
$ git commit -m "Sua mensagem"

#Stage Area + Commit
$ git commit -am "Sua mensagem"

```
&nbsp;

# Branch

```
#Cria
$ git branch nome

#Entra
$ git checkout nome

#Cria/Entra
$ git checkout -b nome

#União de ramos
$ git merge RamoSecundário
```
&nbsp;

# Log
```
#Exibe todos os commits
$ git log 

#Número específico
$ git log -n 2

#Resumo conciso
$ git log --oneline

#Linhas dos arquivos alterados
$ git log --stat

#Junção
$ git log -n 2 --oneline --stat
```
&nbsp;

# Diff
```
#Mudanças do arquivo
$ git diff arquivo.php

#Diferença entre o arquivo da Stage e última versão commitada
$ git diff --staged
```
&nbsp;

# Remover arquivos
```
#Remove arquivo e adiciona na Stage
$ git rm arquivo.php

#Renomear 
$ git mv arquivo.php arquivo1.php
```
&nbsp;

# Desfazer mudanças
```
#Desfaz alterações não rastreada e restaura arquivo deletado
$ git checkout -- arquivo.php

#Remover da área de stage e mantém as alterações feitas
#Sem parâmetro remove TUDO da stage
$ git reset -- arquivo.php

#Remover da área de stage e remove as alterações feitas
$ git reset --hard

#Reverter um arquivo commitado
#Passar código do commit anterior ou HEAD como parâmetro
$ git revert --no-edit xxxxx 

```

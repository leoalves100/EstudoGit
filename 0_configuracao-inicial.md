# Softwares necessários

1. git git-core git-man git-gui git-doc
2. ssh openssh-server openssh-client

> Software opcionais, para ajudar no gerenciamento dos repositórios
1. Gitkraken

&nbsp;

# Configurações globais
```
#Usuário
$ git config --global user.name "Seu nome"

#Email
$ git config --global user.email "seuemail@teste.com"
```
&nbsp;

# Outras configurações
```
#Editor padrão
$ git config --global core.editor SeuEditor

#Adicionar templete para commit
$ git config --global commit.templete ~/SeuTemplete.txt

#Usar saída colorida
$ git config color.ui true

#Exibir log em apenas uma linha por commit
$ git config format.pretty oneline
```
&nbsp;

> Git é case insensitive Pessoa == PESSOA


```
$ git config --global core.ignorecase false

```
&nbsp;

> Armazenando senha em cache para conexão **HTTPS**

```
#Armazena em cache
$ git config --global credential.helper cache

#Define tempo para manter senha em cache em seg
$ git config --global credential.helper 'cache --timeout=3600'
```
&nbsp;

# Gerar chave ssh

```
$ ssh-keygen -t rsa -b 4096 -C "seuemail@servidor.com"

Generating public/private rsa key pair.
Enter file in which to save the key (/home/user/.ssh/id_rsa):

#Pressione Enter

Enter passphrase (empty for no passphrase):

#Digite a senha para sua chave ou deixe em branco, pressionando Enter

Enter same passphrase again:

#Digite a senha anterior
```

Copie conteúdo da chave, **id_rsa.pub**, cole em chave ssh no **Github**

Testar comunicação com **servidor**

```
$ ssh -T git@github.com
```

*****

Continuar: [Comandos básicos](1_comandos-basicos.md)

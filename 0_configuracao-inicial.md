# Configuração inicial

## Softwares necessários

1. git git-core git-man git-gui git-doc
1. ssh openssh-server openssh-client

## Configurações globais


Configure nome e email

```
$ git config --global user.name "Leandro Alves"
$ git config --global user.email "meuemail@teste.com"
```

## Configurando editor
Editor padrão para escrever commits

```
$ git config --global core.editor nomeditor
```

## Armazenando senha em cache para conexão **HTTPS**

```
# Armazena em cache
$ git config --global credential.helper cache

# Define tempo para manter senha em cache
# 3600 == 1h
$ git config --global credential.helper 'cache --timeout=3600'
```

## Gerar chave ssh

```
$ ssh-keygen -t rsa -b 4096 -C "meuemail@servidor.com"
Generating public/private rsa key pair.
Enter file in which to save the key (/home/leandro/.ssh/id_rsa):

# Pressione Enter

Enter passphrase (empty for no passphrase):

# Digite a senha para sua chave ou deixe em branco, pressionando Enter

Enter same passphrase again:

# Digite a senha anterior
```

Copie conteúdo da chave, **id_rsa.pub**, cole em chave ssh no **Github**

Testar comunicação com **servidor**

```
# Testar conexão com o servidor

$ ssh -T git@github.com

# Yes, permitir que github seja adicionado a lista de servidores conhecidos
```

*****

Continuar: [Comandos básicos](1_comandos-basicos.md)

# Instalar Linux no Windows 10 com WSL + NodeJS

## 1) Instalar o WSL

https://docs.microsoft.com/pt-br/windows/wsl/install-win10

## 2) Instalar Ubuntu

Iniciar -> Microsoft Store: procurar Ubuntu

Definir um usuário e senha

## 3) Instalar o Windows Terminal

Iniciar -> Microsoft Store: procurar Windows Terminal

Botão drop down -> Configurações -> Inicialização -> Perfil padrão: Ubuntu

## 4) Testar terminal
```bash
cd ~
cd /mnt/c
ls
```

## 5) Instalar NodeJS
```bash
sudo apt update
sudo apt upgrade
sudo apt install -y curl
curl -sL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt install -y nodejs
```

## 6) Instalar extensão Remote WSL no VS Code

Depois abra uma pasta no VS Code pelo terminal Linux
```bash
code .
```

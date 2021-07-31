# Instalar Linux no Windows 10 com WSL + NodeJS + JDK

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

## 5) Instalar extensão Remote WSL no VS Code

Depois abra uma pasta no VS Code pelo terminal Linux
```bash
code .
```

## 6) Instalar NodeJS
```bash
sudo apt update
sudo apt upgrade
sudo apt install -y curl
curl -sL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt install -y nodejs
```

## 7) Instalar JDK
```bash
sudo apt install openjdk-11-jdk
```
Confira a versão e a localidade da instalação
```bash
java -version
sudo update-alternatives --config java
```

Depois edite o arquivo ~/.bashrc
```bash
code ~/.bashrc
```
Inclua no final do arquivo:
```
JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64
export JAVA_HOME
export PATH=$PATH:$JAVA_HOME
```
Abra um novo terminal e confira a variável de ambiente
```
echo $JAVA_HOME
```

## 8) Instalar o Maven
```bash
sudo apt install mvn
```
Confira a instalação
```bash
mvn -v
```

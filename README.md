# AWS CLI - Userdata
  Este repositório contém alguns arquivos e códigos utilizados durante curso de `Especialização AWS`.
## Observações
  É nessário possui um conta na AWS vinculada para executar os comandos do CLI.

### 💻 Principais Tecnologias e Bibliotecas
- AWS CLI

# ⚙ Instalação, configuração e execução

## ⚙ Instalação 
- Utilizando o [link](https://aws.amazon.com/pt/cli/) faça o download do instalador do CLI especifico para o seu sistema operacional

### Windows
- Assim que fazer o download do executável, instale o CLI.
- Executando o comando `aws` no seu terminal.

### Distribuições Linux
- Faça o download do instalador do CLI:
    
    ```bash
    curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"
    ```
- Descompacte o donwload
    ```bash
    # no ubuntu não vem o "unzip" instalado por padrão
    sudo apt-get install unzip 
    unzip awscliv2.zip
    ```
- Instalando o CLI
    ```bash
    sudo ./aws/install
    ```
    
- Executando o comando `aws` no seu terminal.

## ⚙ Configuração 

### Criando usuário IAM
- Criar um usuário IAM com acesso programático (não é necessário permitir acesso a console)
- Definir políticas: podemos definir políticas exclusivas para cada usuário. No modelo de testes vamos atribuir acesso root.
    - Cuidado com as chaves de um usuário administrador, pois com ela se tem acesso a todos os recursos e diretórios da sua conta.
- Após criar o usuário é importante armazenar em um locval seguro as credenciais de acesso
### Configurando seu CLI
- No seu terminal execute o seguinte comando:
  ```bash
  aws configure
  ```
- Preencha os dados de credenciais solicitados de acordo com o arquivo de credenciais de usuário baixados anteriormente
- Informar a região padrão, pode ser uma ou multiplas
    - `us-east-1`
- Informar o formato de saida dos nossos comandos
    - Vide documentação oficial (`JSON`, `text`, `table`), dependendo do comando o formato de saída tem diferença
    - Por padrão usamos `text`
- Testar se está funcionando
  ```bash
  aws s3 ls # listar os buckets na nossa conta
  ```

## ⚙ Execução
- Todos os comandos e parametros disponíveis para CLI estão presentes na documentação oficial `AWS CLI Command Reference`.
# Treinamento_GB
# Instalação e Configuração

## Pré-requisitos

Antes de começar, verifique se você possui as seguintes credenciais da AWS:
- Access Key ID
- Secret Access Key
`Referencia: https://www.youtube.com/watch?v=SteXxricweA`
## Instalação das ferramentas

1. Abra um terminal e execute o seguinte comando para instalar a AWS CLI e pip3:

    `sudo apt-get install awscli pip3`
        
2. Instale as bibliotecas Python boto e boto3 usando o pip3:
 
    `pip3 install boto boto3`

3. Instale o Ansible e o Ansible Core:

    `sudo apt install ansible ansible-core`

## Configuração da AWS CLI

1. Execute o seguinte comando para configurar a AWS CLI:

    `aws configure`

2. Insira as suas credenciais da AWS quando solicitado. Você também pode configurar a região padrão e o formato de saída.
3. Verifique se a configuração está correta executando o seguinte comando:

     `aws sts get-caller-identity`

4. Se você tiver várias contas ou papéis da AWS, poderá usar o seguinte comando para alternar entre eles:

    `aws configure --profile <profile-name>`

## Configuração do Ansible

1. Verifique se o Ansible foi instalado corretamente executando o seguinte comando:

    `ansible --version`

2. Instale a coleção Amazon AWS executando o seguinte comando:

    `ansible-galaxy collection install amazon.aws`

3. Verifique se a coleção foi instalada corretamente executando o seguinte comando:

    `ansible-galaxy collection list`

## Verificação

1. Verifique se o Ansible está configurado corretamente para se comunicar com a AWS executando o seguinte comando:

    `aws ec2 describe-instances`

2. Verifique se você pode se conectar às instâncias da EC2 usando o Ansible executando o seguinte comando:
 
    `ansible -i <path-to-inventory-file> -m ping <ec2-instance-name>`

Isso é tudo! Com essas etapas, você deve ser capaz de instalar e configurar as ferramentas AWS CLI, pip3, boto, boto3, ansible e a coleção Amazon AWS.


# Desafio DevOps

Este projeto tem como objetivo demonstrar a criação de uma infraestrutura escalável e configurável para hospedagem de um site WordPress no Azure utilizando ferramentas de DevOps como Terraform.

## Pré-requisitos

Antes de começar, você precisará ter os seguintes itens instalados:

- Terraform
- Azure CLI
- Git

## Arquitetura

A arquitetura do projeto inclui:

- **Azure**
  - Virtual Machines
  - Virtual Networks
  - Network Security Groups

## Instruções de Instalação

### Azure

1. Clone o repositório:
   ```bash
   git clone https://github.com/dafneduda/DesafioDevOps.git
   cd DesafioDevOps
   ```

2. Inicialize o Terraform:
   ```bash
   terraform init
   ```

3. Crie um plano de execução:
   ```bash
   terraform plan -out=tfplan
   ```

4. Applique o plano:
   ```bash
   terraform apply "tfplan"
   ```

5. Conecte-se à VM:
   Recupere o endereço IP público da sua VM e use o comando SSH para se conectar, substituindo `<path-to-private-key>` pelo caminho da chave privada e `<var.username>` pelo nome de usuário configurado.
   ```bash
   ssh -i <path-to-private-key> <var.username>@<public-ip-address>
   ```

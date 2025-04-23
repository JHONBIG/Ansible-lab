```markdown
# Ansible-lab

Este repositório contém um laboratório de estudos práticos com **Ansible**, com foco em automação de infraestrutura na **AWS**. O objetivo é experimentar e entender como o Ansible interage com serviços cloud, utilizando práticas reais de provisionamento, configuração e deploy.

## 📦 Estrutura do Projeto

```bash
Ansible-lab/
├── hosts               # Inventário (estático ou dinâmico)
├── index.html          # Página de teste para deploy (ex: via NGINX)
├── maquina.config      # Configurações de provisionamento (ex: EC2, AMI, VPC)
├── README.md           # Este documento
```

## ✨ Objetivos do Lab

- Estudar automação de infraestrutura usando Ansible na AWS
- Criar e configurar máquinas EC2 automaticamente
- Fazer deploy de aplicações ou páginas simples em instâncias provisionadas
- Aprender a usar inventário estático e dinâmico (AWS EC2)

## ☁️ Tecnologias Utilizadas

- **Ansible** (2.9+)
- **AWS EC2**
- **Boto3** / **Botocore**
- **Inventário Dinâmico AWS EC2**
- **NGINX** (como exemplo de aplicação web)
- **Python 3.x**
- (Opcional) **Docker** para testes locais

## 📋 Pré-requisitos

- Conta AWS com IAM configurado
- AWS CLI e credenciais válidas (`aws configure`)
- Instalação dos pacotes:
  ```bash
  pip install ansible boto3 botocore
  ```

- Ansible configurado para usar o plugin `aws_ec2` como inventário dinâmico (caso deseje usar inventário automático baseado nas instâncias da AWS)

## 🚀 Como rodar o projeto

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/Ansible-lab.git
   cd Ansible-lab
   ```

2. Configure o arquivo `hosts` (estático) ou use um inventário dinâmico baseado em EC2:
   - Para dinâmico, veja: [Documentação oficial](https://docs.ansible.com/ansible/latest/plugins/inventory/aws_ec2.html)

3. Customize o arquivo `maquina.config` com os parâmetros da instância (AMI, tipo, chave SSH, VPC, etc).

4. Execute os playbooks conforme suas tarefas de estudo (provisionamento, configuração, deploy).

   Exemplo (provisionamento + configuração básica):
   ```bash
   ansible-playbook -i hosts playbook.yml
   ```

## 📚 Referências

- [Documentação Ansible](https://docs.ansible.com/)
- [Módulos AWS no Ansible](https://docs.ansible.com/ansible/latest/collections/amazon/aws/index.html)
- [Inventário AWS EC2 dinâmico](https://docs.ansible.com/ansible/latest/plugins/inventory/aws_ec2.html)
- [Boto3 AWS SDK for Python](https://boto3.amazonaws.com/v1/documentation/api/latest/index.html)

## ⚠️ Aviso

> **Cuidado**: recursos criados na AWS podem gerar **custos reais**. Certifique-se de encerrar as instâncias e limpar os recursos após seus testes.

---

**Autor:** [Jônathan Souza](https://github.com/JHONBIG)  
**Licença:** MIT
```
---
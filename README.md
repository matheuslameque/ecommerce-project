# 🚀 E-commerce na AWS – Arquitetura Otimizada para Custos / E-commerce on AWS – Cost-Optimized Architecture

---

## 🇧🇷 Português

### 📌 Tecnologias e Serviços Utilizados
- **AWS Route 53** – Gerenciamento de DNS
- **AWS CloudFront** – CDN para caching e performance
- **Amazon S3** – Armazenamento estático
- **Elastic Load Balancer (ELB)** – Distribuição de tráfego
- **Amazon EC2 (Auto Scaling)** – Aplicações em subnets públicas
- **Amazon RDS Aurora** – Banco de dados escalável em subnets privadas
- **Amazon CloudWatch** – Monitoramento e logging

### 🎯 Objetivo do Projeto
Criar uma infraestrutura **segura**, **escalável** e de **baixo custo** para um e-commerce. O desafio foi equilibrar performance, resiliência e otimização financeira dentro das restrições orçamentárias.

### 🔥 Desafios e Soluções
#### 🔹 Controle de Custos com Alta Disponibilidade
- **Problema:** Garantir disponibilidade com orçamento mensal de **$500**.
- **Solução:** Uso de **Auto Scaling** e instâncias utilizando **Saving Plans** para reduzir custos das EC2, além de **Aurora Serverless** para o banco de dados.

#### 🔹 Performance e Cache
- **Problema:** Reduzir latência e melhorar experiência do usuário.
- **Solução:** Implementação do **CloudFront** para caching de conteúdo e otimização do uso do **S3**.

#### 🔹 Segurança e Restrições de Rede
- **Problema:** Evitar exposição direta do banco de dados.
- **Solução:** **VPC** com subnets privadas para **RDS Aurora** e uso de **Security Groups** bem configurados.

### 📊 Estimativa de Custos
| Serviço                  | Custo Mensal Estimado |
|--------------------------|-----------------------|
| EC2 Saving Plans + Auto Scaling | $31            |
| RDS Aurora Serverless    | $296                  |
| CloudFront + S3          | $27                   |
| ELB + Route 53           | $28                   |
| CloudWatch Logs          | $63                   |
| **Total**                | **$445**              |

---

## 🇺🇸 English

### 📌 Technologies and Services Used
- **AWS Route 53** – DNS management
- **AWS CloudFront** – CDN for caching and performance
- **Amazon S3** – Static storage
- **Elastic Load Balancer (ELB)** – Traffic distribution
- **Amazon EC2 (Auto Scaling)** – Applications in public subnets
- **Amazon RDS Aurora** – Scalable database in private subnets
- **Amazon CloudWatch** – Monitoring and logging

### 🎯 Project Objective
Create a **secure**, **scalable**, and **low-cost** infrastructure for an e-commerce platform. The challenge was to balance performance, resilience, and financial optimization within the budget constraints.

### 🔥 Challenges and Solutions
#### 🔹 Cost Control with High Availability
- **Problem:** Ensure availability with a monthly budget of **$500**.
- **Solution:** Use of **Auto Scaling** and **Saving Plans** for instances to reduce EC2 costs, along with **Aurora Serverless** for the database.

#### 🔹 Performance and Caching
- **Problem:** Reduce latency and improve user experience.
- **Solution:** Implementation of **CloudFront** for content caching and optimization of **S3** usage.

#### 🔹 Security and Network Restrictions
- **Problem:** Avoid direct exposure of the database.
- **Solution:** **VPC** with private subnets for **RDS Aurora** and well-configured **Security Groups**.

### 📊 Cost Estimation
| Service                  | Estimated Monthly Cost |
|--------------------------|------------------------|
| EC2 Spot + Auto Scaling  | $200                  |
| RDS Aurora Serverless    | $100                  |
| CloudFront + S3          | $50                   |
| ELB + Route 53           | $50                   |
| CloudWatch Logs          | $50                   |
| **Total**                | **$450-$500**         |

---

## 🌐 Links Úteis / Useful Links
- [Escola da Nuvem](https://www.escoladanuvem.org/)
- [AWS Cloud Practitioner](https://aws.amazon.com/certification/certified-cloud-practitioner/)

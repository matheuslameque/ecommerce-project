# Arquitetura da Solução / Solution Architecture

---

## 🇧🇷 Português

### Visão Geral

Esta arquitetura foi projetada para um e-commerce na AWS, com foco em **escalabilidade**, **segurança** e **otimização de custos**. O design segue uma abordagem baseada em alta disponibilidade e redundância, utilizando múltiplas zonas de disponibilidade (AZs) para garantir resiliência e desempenho.

---

### Diagrama da Arquitetura

![Arquitetura do E-commerce na AWS](./images/project-diagram.jpg)

_Nota: O diagrama acima foi criado utilizando os [AWS Architecture Icons](https://aws.amazon.com/architecture/icons/)._

---

### Componentes Principais

#### 1. Gerenciamento de Domínio e Cache

- **Amazon Route 53**: Gerenciamento de DNS para fornecer resolução de domínio rápida e confiável.
- **Amazon CloudFront**: Content Delivery Network (CDN) para armazenar em cache os ativos estáticos e reduzir a latência globalmente.
- **Amazon S3**: Armazena arquivos estáticos como imagens, CSS e JavaScript, reduzindo a carga sobre os servidores de aplicação.

#### 2. Camada de Aplicação

- **Elastic Load Balancer (ELB)**: Distribui o tráfego entre as instâncias do EC2, garantindo escalabilidade e tolerância a falhas.
- **Amazon EC2 (Auto Scaling Group)**: Instâncias em subnets públicas responsáveis pelo processamento da aplicação, podendo escalar conforme a demanda.

#### 3. Banco de Dados

- **Amazon Aurora (RDS) em Subnets Privadas**: Gerencia os dados da aplicação, oferecendo alta disponibilidade e failover automático.
- **Réplica de Aurora**: Melhora a resiliência e distribui consultas de leitura para otimizar o desempenho.

#### 4. Monitoramento e Logs

- **Amazon CloudWatch**: Coleta logs e métricas de desempenho para monitoramento e depuração.
- **AWS Config e IAM**: Garantem conformidade com boas práticas de segurança e controle de acesso adequado.

---

### Fluxo de Requisição

1. O cliente acessa o site via **Route 53**, que direciona o tráfego ao **CloudFront**.
2. O **CloudFront** entrega arquivos estáticos do **S3** e encaminha outras requisições para o **ELB**.
3. O **ELB** distribui o tráfego entre as instâncias do **EC2**, que processam a lógica da aplicação.
4. O **EC2** se conecta ao **Aurora RDS** para obter os dados necessários.
5. Logs e métricas são armazenados no **CloudWatch** para monitoramento e análise.

---

### Justificativa das Escolhas

- **Alta Disponibilidade**: Utiliza instâncias distribuídas em várias zonas de disponibilidade (AZs).
- **Escalabilidade**: Auto Scaling para adaptação à demanda.
- **Otimização de Custos**: Uso de instâncias EC2 com Saving Plans, CloudFront e Aurora Serverless para reduzir despesas.
- **Segurança**: Bancos de dados em subnets privadas e controle de acesso refinado.

---

### Possíveis Melhorias Futuras

- **Implementação de Lambda Functions**: Para otimizar workloads event-driven.
- **Uso de DynamoDB**: Para armazenar sessões e melhorar escalabilidade.
- **Integração com AWS WAF**: Para proteção contra ataques como SQL Injection e DDoS.

---

## 🇺🇸 English

### Overview

This architecture was designed for an e-commerce platform on AWS, focusing on **scalability**, **security**, and **cost optimization**. The design follows a high-availability and redundancy approach, using multiple availability zones (AZs) to ensure resilience and performance.

---

### Architecture Diagram

![E-commerce Architecture on AWS](./images/project-diagram.jpg)

_Note: The diagram above was created using [AWS Architecture Icons](https://aws.amazon.com/architecture/icons/)._

---

### Key Components

#### 1. Domain Management and Caching

- **Amazon Route 53**: DNS management for fast and reliable domain resolution.
- **Amazon CloudFront**: Content Delivery Network (CDN) to cache static assets and reduce global latency.
- **Amazon S3**: Stores static files such as images, CSS, and JavaScript, reducing the load on application servers.

#### 2. Application Layer

- **Elastic Load Balancer (ELB)**: Distributes traffic across EC2 instances, ensuring scalability and fault tolerance.
- **Amazon EC2 (Auto Scaling Group)**: Instances in public subnets responsible for application processing, scaling according to demand.

#### 3. Database

- **Amazon Aurora (RDS) in Private Subnets**: Manages application data, offering high availability and automatic failover.
- **Aurora Replica**: Improves resilience and distributes read queries to optimize performance.

#### 4. Monitoring and Logging

- **Amazon CloudWatch**: Collects logs and performance metrics for monitoring and debugging.
- **AWS Config and IAM**: Ensures compliance with security best practices and proper access control.

---

### Request Flow

1. The client accesses the website via **Route 53**, which directs traffic to **CloudFront**.
2. **CloudFront** delivers static files from **S3** and forwards other requests to the **ELB**.
3. The **ELB** distributes traffic across **EC2** instances, which process the application logic.
4. The **EC2** instances connect to **Aurora RDS** to fetch the necessary data.
5. Logs and metrics are stored in **CloudWatch** for monitoring and analysis.

---

### Justification of Choices

- **High Availability**: Uses instances distributed across multiple availability zones (AZs).
- **Scalability**: Auto Scaling to adapt to demand.
- **Cost Optimization**: Use of EC2 Instances with Saving Plans, CloudFront, and Aurora Serverless to reduce expenses.
- **Security**: Databases in private subnets and refined access control.

---

### Possible Future Improvements

- **Implementation of Lambda Functions**: To optimize event-driven workloads.
- **Use of DynamoDB**: To store sessions and improve scalability.
- **Integration with AWS WAF**: For protection against attacks such as SQL Injection and DDoS.

---

## 🌐 Links Úteis / Useful Links

- [Amazon Route 53](https://aws.amazon.com/route53/)
- [Amazon CloudFront](https://aws.amazon.com/cloudfront/)
- [Amazon Aurora](https://aws.amazon.com/rds/aurora/)
- [AWS Auto Scaling](https://aws.amazon.com/autoscaling/)
- [Amazon CloudWatch](https://aws.amazon.com/cloudwatch/)

# Estimativa de Custos da Arquitetura / Architecture Cost Estimation

---

## 🇧🇷 Português

### Visão Geral

A arquitetura foi projetada para se manter dentro do orçamento mensal de **$500**, utilizando serviços otimizados para custo-benefício. Abaixo estão os detalhes dos custos estimados e as estratégias de redução de custos.

---

### 📊 Resumo dos Custos

| Serviço                  | Custo Mensal Estimado |
|--------------------------|-----------------------|
| EC2 Saving Plans + Auto Scaling | $31            |
| RDS Aurora Serverless    | $296                  |
| CloudFront + S3          | $27                   |
| ELB + Route 53           | $28                   |
| CloudWatch Logs          | $63                   |
| **Total**                | **$445**              |

---

### 📌 Estratégias de Redução de Custos

- **Uso de Saving Plans para as instâncias**: Conhecendo o período determinado de uso das instâncias e tendo orçamento para adiantar os custos, é possível reduzir consideravelmente o custo das EC2 sem comprometer a disponibilidade.
- **Aurora Serverless**: Escalabilidade automática do banco de dados, evitando custos fixos elevados.
- **CloudFront**: Reduz requisições diretas ao EC2, otimizando a largura de banda.
- **Auto Scaling**: Garante que apenas a capacidade necessária esteja ativa em momentos de baixa demanda.
- **Monitoramento com CloudWatch**: Configurado para coletar apenas logs essenciais, reduzindo o custo de armazenamento.

---

### 🔍 Monitoramento de Gastos

- **AWS Cost Explorer**: Acompanhamento contínuo dos custos.
- **AWS Budgets**: Alertas configurados para evitar ultrapassagem do orçamento.

Esta abordagem garante que a infraestrutura suporte um e-commerce funcional sem exceder os **$500/mês**.

---

## 🇺🇸 English

### Overview

The architecture was designed to stay within the monthly budget of **$500**, using cost-optimized services. Below are the details of the estimated costs and cost-reduction strategies.

---

### 📊 Cost Summary

| Service                  | Estimated Monthly Cost |
|--------------------------|------------------------|
| EC2 Saving Plans + Auto Scaling  | $31            |
| RDS Aurora Serverless    | $296                   |
| CloudFront + S3          | $27                    |
| ELB + Route 53           | $28                    |
| CloudWatch Logs          | $63                    |
| **Total**                | **$445**               |

---

### 📌 Cost Reduction Strategies

- **Use of Saving Plans for instances**: Knowing the fixed period of use of the instances and having the budget to pay upfront, it is possible to sustantially reduce EC2 costs without compromising availability.
- **Aurora Serverless**: Automatic database scaling, avoiding high fixed costs.
- **CloudFront**: Reduces direct requests to EC2, optimizing bandwidth.
- **Auto Scaling**: Ensures only the necessary capacity is active during low-demand periods.
- **CloudWatch Monitoring**: Configured to collect only essential logs, reducing storage costs.

---

### 🔍 Cost Monitoring

- **AWS Cost Explorer**: Continuous cost tracking.
- **AWS Budgets**: Alerts configured to prevent budget overruns.

This approach ensures that the infrastructure supports a functional e-commerce platform without exceeding **$500/month**.

---

## 🌐 Links Úteis / Useful Links

- [AWS Cost Explorer](https://aws.amazon.com/aws-cost-management/aws-cost-explorer/)
- [AWS Budgets](https://aws.amazon.com/aws-cost-management/aws-budgets/)
- [Amazon EC2 Saving Plans](https://aws.amazon.com/savingsplans/)
- [Amazon Aurora Serverless](https://aws.amazon.com/rds/aurora/serverless/)
- [Amazon CloudFront](https://aws.amazon.com/cloudfront/)

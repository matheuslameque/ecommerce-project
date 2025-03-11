# Desafios e Soluções / Challenges and Solutions

---

## 🇧🇷 Português

### 🎯 Principais Desafios

#### 1️⃣ Controle de Custos com Alta Disponibilidade

- **Desafio**: Garantir alta disponibilidade do e-commerce dentro do orçamento mensal de **$500**.
- **Solução**:
  - Implementação de instâncias **EC2 Spot** para reduzir custos computacionais.
  - Uso de **Aurora Serverless** para escalabilidade automática do banco de dados.
  - Configuração de **Auto Scaling** para ajustar a capacidade conforme a demanda.

#### 2️⃣ Performance e Tempo de Resposta

- **Desafio**: Melhorar a experiência do usuário reduzindo a latência das requisições.
- **Solução**:
  - Uso de **Amazon CloudFront** para caching e distribuição global de conteúdo estático.
  - Armazenamento de arquivos estáticos no **Amazon S3** para evitar sobrecarga no EC2.

#### 3️⃣ Segurança e Restrições de Rede

- **Desafio**: Evitar exposição direta do banco de dados e proteger a infraestrutura contra ataques.
- **Solução**:
  - Subnets privadas para hospedar o **Amazon Aurora RDS**, impedindo acesso externo direto.
  - Configuração rigorosa de **Security Groups** e **IAM Roles**.
  - Monitoramento com **AWS CloudWatch** e **AWS WAF** para detectar ameaças.

#### 4️⃣ Escalabilidade e Gerenciamento de Tráfego

- **Desafio**: Garantir que o ambiente suporte picos de tráfego sem degradação de performance.
- **Solução**:
  - Implementação de **Elastic Load Balancer (ELB)** para distribuir requisições entre instâncias EC2.
  - **Auto Scaling** configurado para responder automaticamente ao aumento de carga.

---

### 🚀 Conclusão

Os desafios foram superados com uma abordagem estratégica de otimização de recursos, garantindo que a arquitetura fosse **escalável**, **segura** e **financeiramente viável**.

---

## 🇺🇸 English

### 🎯 Key Challenges

#### 1️⃣ Cost Control with High Availability

- **Challenge**: Ensure high availability for the e-commerce platform within the monthly budget of **$500**.
- **Solution**:
  - Implementation of **EC2 Spot Instances** to reduce computational costs.
  - Use of **Aurora Serverless** for automatic database scaling.
  - Configuration of **Auto Scaling** to adjust capacity based on demand.

#### 2️⃣ Performance and Response Time

- **Challenge**: Improve user experience by reducing request latency.
- **Solution**:
  - Use of **Amazon CloudFront** for caching and global distribution of static content.
  - Storage of static files in **Amazon S3** to avoid overloading EC2.

#### 3️⃣ Security and Network Restrictions

- **Challenge**: Prevent direct exposure of the database and protect the infrastructure against attacks.
- **Solution**:
  - Private subnets to host **Amazon Aurora RDS**, preventing direct external access.
  - Rigorous configuration of **Security Groups** and **IAM Roles**.
  - Monitoring with **AWS CloudWatch** and **AWS WAF** to detect threats.

#### 4️⃣ Scalability and Traffic Management

- **Challenge**: Ensure the environment can handle traffic spikes without performance degradation.
- **Solution**:
  - Implementation of **Elastic Load Balancer (ELB)** to distribute requests across EC2 instances.
  - **Auto Scaling** configured to automatically respond to increased load.

---

### 🚀 Conclusion

The challenges were overcome with a strategic approach to resource optimization, ensuring the architecture is **scalable**, **secure**, and **financially viable**.

---

## 🌐 Links Úteis / Useful Links

- [Amazon EC2 Spot Instances](https://aws.amazon.com/ec2/spot/)
- [Amazon Aurora Serverless](https://aws.amazon.com/rds/aurora/serverless/)
- [Amazon CloudFront](https://aws.amazon.com/cloudfront/)
- [Amazon S3](https://aws.amazon.com/s3/)
- [AWS WAF](https://aws.amazon.com/waf/)
- [AWS CloudWatch](https://aws.amazon.com/cloudwatch/)

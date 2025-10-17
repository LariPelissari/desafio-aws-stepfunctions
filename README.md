
<div align="center">

# 🌩️ Desafio DIO AWS Step Functions  
### 🧠 Desafio das Aulas de AWS – Criando Fluxos Automatizados na Nuvem

![Status](https://img.shields.io/badge/Build-Passing-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)
![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazon-aws&logoColor=FF9900)
![StepFunctions](https://img.shields.io/badge/Step%20Functions-FF4F00?style=for-the-badge&logo=amazons3&logoColor=white)
![Lambda](https://img.shields.io/badge/Lambda-F7A81B?style=for-the-badge&logo=awslambda&logoColor=black)
![ECS](https://img.shields.io/badge/ECS-FF9900?style=for-the-badge&logo=docker&logoColor=white)
![EKS](https://img.shields.io/badge/EKS-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)
![SNS](https://img.shields.io/badge/SNS-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)
![SQS](https://img.shields.io/badge/SQS-4D27AA?style=for-the-badge&logo=amazonaws&logoColor=white)

</div>

---

## 🧭 Visão Geral

Este repositório foi criado como parte do **Desafio DIO AWS Step Functions**, que tem como objetivo explorar e demonstrar o uso de **serviços da AWS para automação de fluxos e integração entre microsserviços**.

A **Amazon Web Services (AWS)** oferece uma infraestrutura escalável e flexível, permitindo criar aplicações **serverless**, **containerizadas** e **altamente disponíveis**.

---

## ⚙️ Principais Serviços Utilizados

### 🧠 AWS Lambda
> Executa código **sem precisar gerenciar servidores**.

- Ideal para tarefas pequenas e rápidas.  
- Acionado por eventos (ex: upload no S3).  
- Suporta linguagens como Python, Node.js, Go e Java.  

---

### 🐳 Amazon ECS (Elastic Container Service)
> Gerencia containers **Docker** de forma automatizada.

- Controla tarefas e serviços de containers.  
- Permite balanceamento de carga e escalabilidade.  
- Integra-se facilmente com o CloudWatch e IAM.  

---

### ☸️ Amazon EKS (Elastic Kubernetes Service)
> Orquestra containers com **Kubernetes**.

- Clusters gerenciados com alta disponibilidade.  
- Ideal para microsserviços complexos.  
- Oferece portabilidade entre ambientes cloud e on-premise.  

---

### 📣 Amazon SNS (Simple Notification Service)
> Serviço de **notificações e mensagens broadcast** (*um-para-muitos*).

- Envia alertas para múltiplos assinantes.  
- Suporta e-mails, SMS e integração com Lambda.  
- Muito usado para notificações em tempo real.  

---

### 📨 Amazon SQS (Simple Queue Service)
> Serviço de **filas de mensagens confiável** (*um-para-um*).

- Garante a entrega de mensagens entre serviços.  
- Ideal para comunicações assíncronas.  
- Suporta modo **FIFO** (First In, First Out).  

---

### 🔁 AWS Step Functions
> Orquestra **fluxos de trabalho** entre diferentes serviços AWS.

- Cria pipelines de automação e aprovação.  
- Integra Lambda, ECS, SQS e outros serviços.  
- Exibe um fluxo visual das etapas executadas.  

---

## 🧩 Integração dos Serviços

| Serviço | Função | Comunicação |
|:--|:--|:--|
| 🧠 **Lambda** | Executa código sob demanda | Eventos |
| 🐳 **ECS / EKS** | Gerenciam containers | Interna |
| 📣 **SNS** | Envia notificações | Um-para-muitos |
| 📨 **SQS** | Armazena mensagens | Um-para-um |
| 🔁 **Step Functions** | Orquestra todo o fluxo | Workflow |

---

## 🌐 Arquitetura Simplificada

```mermaid
flowchart TD
    A[📁 Evento: Upload no S3] --> B[⚙️ Lambda Executa Função]
    B --> C[📣 SNS Envia Notificação]
    C --> D[📨 SQS Armazena Mensagem]
    D --> E[🐳 ECS/EKS Processam Dados]
    E --> F[🔁 Step Functions Orquestra o Fluxo]
    F --> G[✅ Resultado Final: Processo Automatizado]
````

---

## 🧰 Como Executar Localmente

> 🔧 *As etapas abaixo simulam o fluxo localmente antes da implantação na AWS.*

### 1️⃣ Clonar o repositório

```bash
git clone https://github.com/seu-usuario/desafio-aws-stepfunctions.git
cd desafio-aws-stepfunctions
```

### 2️⃣ Instalar dependências (se houver Lambda local)

```bash
npm install
# ou
pip install -r requirements.txt
```

### 3️⃣ Executar o Lambda localmente (exemplo em Node.js)

```bash
node lambda/index.js
```

### 4️⃣ Simular o fluxo Step Functions

Use o AWS CLI:

```bash
aws stepfunctions start-execution \
  --state-machine-arn arn:aws:states:us-east-1:123456789012:stateMachine:MeuFluxoAWS \
  --name ExecucaoTeste \
  --input '{"evento":"upload_arquivo"}'
```

---

## 🧠 Conclusão

Os serviços explorados aqui **se complementam** para criar aplicações **modernas, escaláveis e altamente automatizadas**:

* **Lambda** → executa funções sob demanda
* **ECS/EKS** → gerenciam containers
* **SNS/SQS** → fazem a comunicação entre sistemas
* **Step Functions** → conecta tudo em um único fluxo orquestrado

💡 O resultado é uma arquitetura **serverless**, **resiliente** e **fácil de manter**, ideal para ambientes modernos de nuvem.

---

<div align="center">

👩‍💻 **Autor:** *Lari Pelissari*
🔗 **Desafio:** [DIO – AWS Step Functions](https://www.dio.me/)
☁️ **Tecnologias:** AWS Lambda • ECS • EKS • SNS • SQS • Step Functions

![Made with Love](https://img.shields.io/badge/Made%20with%20❤️%20in%20AWS-232F3E?style=for-the-badge)

</div>
# Desafio AWS Step Functions



---



````markdown

\# 🚀 Desafio DIO AWS Step Functions  

\*\*Desafio das Aulas de AWS\*\*



\## 🧭 Documentação – Principais Serviços AWS e Seus Usos



A \*\*Amazon Web Services (AWS)\*\* oferece uma ampla variedade de ferramentas que ajudam empresas e desenvolvedores a \*\*criar, automatizar e escalar aplicações na nuvem\*\*.  

Neste projeto, exploramos os serviços \*\*Lambda\*\*, \*\*ECS\*\*, \*\*EKS\*\*, \*\*SNS\*\*, \*\*SQS\*\* e \*\*Step Functions\*\*, que trabalham juntos para construir soluções modernas e eficientes.



---



\## ⚙️ AWS Lambda

> Executa código \*\*sem precisar gerenciar servidores\*\*.



📌 \*\*O que faz:\*\*  

\- Executa funções (em Python, Node.js etc.) sob demanda.  

\- É acionado por eventos (ex: upload no S3, atualização no banco).  



💡 \*\*Quando usar:\*\*  

\- Tarefas pequenas e rápidas.  

\- Processamento de eventos.  

\- Automação sem servidores ativos.  



---



\## 🐳 Amazon ECS (Elastic Container Service)

> Serviço gerenciado para \*\*execução de containers Docker\*\*.



📌 \*\*O que faz:\*\*  

\- Cria e gerencia tarefas e serviços baseados em containers.  

\- Controla a infraestrutura de execução.  



💡 \*\*Quando usar:\*\*  

\- Aplicações baseadas em containers.  

\- Quando há necessidade de controle sobre a infraestrutura.  

\- Integração simples com outros serviços da AWS.  



---



\## ☸️ Amazon EKS (Elastic Kubernetes Service)

> Gerencia clusters \*\*Kubernetes\*\* dentro da AWS.



📌 \*\*O que faz:\*\*  

\- Orquestra containers usando o Kubernetes.  

\- Oferece escalabilidade e portabilidade entre ambientes.  



💡 \*\*Quando usar:\*\*  

\- Se você já utiliza Kubernetes em outro ambiente.  

\- Projetos complexos com muitos microsserviços.  

\- Necessidade de alta escalabilidade.  



---



\## 📣 Amazon SNS (Simple Notification Service)

> Serviço de \*\*mensageria e notificações\*\* “um-para-muitos”.



📌 \*\*O que faz:\*\*  

\- Envia mensagens e alertas em tempo real.  

\- Entrega notificações para múltiplos destinos (e-mail, SMS, Lambda etc.).  



💡 \*\*Quando usar:\*\*  

\- Notificações e alertas automáticos.  

\- Comunicação entre serviços ou usuários.  

\- Integração com múltiplos assinantes.  



---



\## 📨 Amazon SQS (Simple Queue Service)

> Serviço de \*\*filas de mensagens\*\* “um-para-um”.



📌 \*\*O que faz:\*\*  

\- Garante entrega confiável de mensagens entre sistemas.  

\- Permite processamento assíncrono e desacoplado.  



💡 \*\*Quando usar:\*\*  

\- Processamento de pedidos, uploads, eventos etc.  

\- Comunicação entre microsserviços.  

\- Evitar sobrecarga e perda de mensagens.  



---



\## 🔁 AWS Step Functions

> Serviço para \*\*orquestrar fluxos de trabalho (workflows)\*\*.



📌 \*\*O que faz:\*\*  

\- Coordena vários serviços AWS (Lambda, SQS, ECS etc.).  

\- Automatiza processos em uma sequência de etapas.  



💡 \*\*Quando usar:\*\*  

\- Automação de processos complexos.  

\- Coordenação de múltiplas funções Lambda.  

\- Criação de pipelines e fluxos de aprovação.  



---



\## 🧩 Conclusão – Como Tudo se Conecta



| Serviço | Função Principal | Tipo de Comunicação |

|----------|------------------|---------------------|

| 🧠 \*\*Lambda\*\* | Executa funções sob demanda | Eventos |

| 🐳 \*\*ECS / EKS\*\* | Gerenciam containers e aplicações | Interna |

| 📣 \*\*SNS\*\* | Envia notificações e mensagens | Um-para-muitos |

| 📨 \*\*SQS\*\* | Armazena mensagens entre sistemas | Um-para-um |

| 🔁 \*\*Step Functions\*\* | Orquestra e coordena tudo | Workflow |



---



\## 🌐 Arquitetura Simplificada



```mermaid

flowchart TD

&nbsp;   A\[Evento: Upload no S3] --> B\[Lambda Executa Função]

&nbsp;   B --> C\[SNS Envia Notificação]

&nbsp;   C --> D\[SQS Armazena Mensagem]

&nbsp;   D --> E\[ECS/EKS Processam Dados]

&nbsp;   E --> F\[Step Functions Orquestra o Fluxo]

&nbsp;   F --> G\[Resultado Final: Processo Automatizado]

````



---



\## 🧠 Conclusão



Esses serviços \*\*se complementam\*\* e formam a base de \*\*arquiteturas modernas e serverless\*\* na AWS:

💡 Juntos, permitem criar sistemas \*\*escaláveis, resilientes e automatizados\*\*, reduzindo custos e aumentando a eficiência operacional.



---



📘 \*\*Autor:\*\* \*Lari Pelissari\*

🔗 \*\*Desafio:\*\* \[DIO AWS Step Functions](https://www.dio.me/)

☁️ \*\*Tecnologias:\*\* AWS Lambda | ECS | EKS | SNS | SQS | Step Functions



```








# AzureContainerLab
Desenvolvi o AzureContainerLab, um laboratório de Cloud Computing no Microsoft Azure, onde implantei a aplicação OWASP Juice Shop como container Docker via interface gráfica (GUI). Configurei a região, grupo de recursos, plano de serviço e variáveis de ambiente, validando o deploy e o funcionamento da aplicação em nuvem.


---

## 🧠 Descrição longa (para README.md).

Criei o **JuiceDockLab**, um laboratório prático de **Cloud Computing** voltado para o estudo de **deploy de aplicações containerizadas (Docker)** no **Microsoft Azure**, utilizando apenas a **interface gráfica (GUI)** do portal Azure.

O objetivo deste laboratório foi compreender o fluxo completo de **provisionamento de recursos**, **configuração de containers** e **execução de aplicações em nuvem**, sem o uso do CLI, apenas com a interface visual — simulando um cenário corporativo de deploy rápido via painel.

---

### 🧩 Contexto do laboratório

Escolhi a aplicação **OWASP Juice Shop**, uma aplicação deliberadamente vulnerável desenvolvida para estudos de **segurança web**, **DevSecOps** e **testes de penetração ética**.
Ela é disponibilizada como imagem Docker oficial no **Docker Hub**, o que a torna perfeita para este tipo de ambiente.

O foco do laboratório não foi desenvolver código, mas **entender como hospedar uma aplicação containerizada na nuvem**, configurando **App Service**, **variáveis de ambiente** e **recursos de rede** de forma visual e intuitiva.

---

### ⚙️ Etapas que realizei (via Portal Azure - GUI)

#### **1. Criação do grupo de recursos**

Através do portal do Azure, criei um **Resource Group** dedicado ao laboratório, nomeado `JuiceDockLab-RG`, localizado na região **East US**.
O objetivo foi manter os recursos organizados e facilmente gerenciáveis.

#### **2. Criação do App Service (Web App for Containers)**

No menu *App Services*, selecionei **Criar** → **Web App** e configurei:

* **Assinatura:** minha assinatura ativa do Azure
* **Grupo de recursos:** `JuiceDockLab-RG`
* **Nome do App:** `juicedocklab-app`
* **Publicar:** Docker Container
* **Sistema Operacional:** Linux
* **Região:** East US

#### **3. Configuração do container Docker**

Na aba **Docker**, selecionei:

* **Opção:** *Docker Hub*
* **Tipo de imagem:** *Public*
* **Imagem:** `bkimminich/juice-shop`
* **Tag:** `latest`

Isso permitiu que o App Service puxasse automaticamente a imagem pública do Juice Shop direto do Docker Hub.

#### **4. Configuração das variáveis de ambiente**

Na aba **Configurações → Variáveis de Aplicativo (Application Settings)**, adicionei variáveis para ajustar o ambiente da aplicação, por exemplo:

* `NODE_ENV = production`
* `PORT = 3000`
* `WEBSITE_NODE_DEFAULT_VERSION = 16.x`

Essas variáveis controlam o comportamento interno da aplicação e garantem compatibilidade com o ambiente do App Service.

#### **5. Deploy e validação**

Após clicar em **Revisar + Criar**, o Azure provisionou automaticamente:

* O **App Service Plan (Linux)**
* O **Web App** com suporte a container
* A configuração do container e as variáveis

Assim que o deploy terminou, acessei a URL pública do App Service, e a aplicação **OWASP Juice Shop** foi carregada corretamente.
Verifiquei o funcionamento da aplicação acessando o painel principal, validando o carregamento do container e a execução do serviço HTTP.

---

### 📸 Evidências

Durante o processo, capturei **prints de tela** de cada etapa:

* Criação do Resource Group
* Seleção da imagem Docker
* Configuração das variáveis de ambiente
* Tela do App Service com o container em execução
* Página inicial do OWASP Juice Shop acessível via URL do Azure

Esses registros foram incluídos no repositório na pasta `screenshots/`.

---

### 🧰 Recursos e tecnologias utilizados

* **Microsoft Azure (Portal GUI)**
* **Azure App Service for Containers**
* **Docker Hub (imagem pública bkimminich/juice-shop)**
* **Linux App Service Plan**
* **Variáveis de ambiente (Application Settings)**
* **Browser + Azure Portal (sem CLI)**

---

### 🌐 Infraestrutura criada

| Recurso                    | Descrição                                    |
| -------------------------- | -------------------------------------------- |
| **Resource Group**         | `JuiceDockLab-RG` — agrupamento dos recursos |
| **App Service Plan**       | Plano de hospedagem em Linux                 |
| **Web App for Containers** | Executa o container Docker (Juice Shop)      |
| **Imagem Docker**          | `bkimminich/juice-shop:latest` (Docker Hub)  |
| **Variáveis de ambiente**  | Configuram o ambiente de execução            |

---

### 📘 O que aprendi com este laboratório

* Compreendi o fluxo de deploy de aplicações containerizadas via **GUI do Azure Portal**.
* Aprendi a configurar **App Service for Containers** e ajustar variáveis de ambiente.
* Entendi o conceito de **imagens Docker públicas e privadas** e como o Azure as consome.
* Reforcei conhecimentos sobre **Cloud Computing**, **PaaS (Platform as a Service)** e **integração com containers**.
* Aprofundei a compreensão sobre como aplicações containerizadas podem ser geridas em ambientes corporativos sem CLI.

---

### 🧾 Estrutura sugerida do repositório

```
JuiceDockLab/
├─ README.md
├─ screenshots/
│  ├─ 01-resource-group.png
│  ├─ 02-docker-config.png
│  ├─ 03-env-vars.png
│  ├─ 04-app-running.png
│  └─ 05-portal-overview.png
└─ LICENSE
```

---

### ✍️ Versão resumida (para LinkedIn)

> Desenvolvi o **JuiceDockLab**, um laboratório de **Cloud Computing** no **Microsoft Azure**, onde implantei a aplicação **OWASP Juice Shop** como container Docker via **interface gráfica (GUI)**. Configurei a região, grupo de recursos, plano de serviço e variáveis de ambiente, validando o deploy e o funcionamento da aplicação em nuvem.

---


Quer que eu gere agora a **versão completa em Markdown (README.md pronto para GitHub)** com emojis, blocos de código e seções visuais?
Posso montar o arquivo completo com base no nome **JuiceDockLab**. Deseja que eu use esse nome mesmo?

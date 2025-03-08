# Azure Cognitive Search

Este repositório contém um guia passo a passo para configurar e utilizar o **Azure Cognitive Search**, utilizando **AI Search** para indexação e consulta de dados. Aqui, abordaremos insights, ferramentas que podem se beneficiar dessa tecnologia e os aprendizados adquiridos durante o processo.

## 🚀 Introdução

O **Azure Cognitive Search** é um serviço de pesquisa baseado na nuvem que usa **inteligência artificial (AI Search)** para indexação e consulta de dados estruturados e não estruturados. Ele permite a implementação de buscas poderosas em bases de dados, enriquecendo os resultados com técnicas de IA, como:

- Processamento de linguagem natural (NLP)
- Análise de sentimentos
- Tradução automática
- Extração de entidades
- Correção ortográfica automática

## 🛠️ Pré-requisitos

Antes de começar, você precisará de:

- Uma conta no **Microsoft Azure** ([crie uma aqui](https://azure.microsoft.com/)).
- Um **Azure Cognitive Search Service** provisionado.
- Dados para indexação (JSON, SQL, Blob Storage, etc.).
- Familiaridade com **REST APIs** ou SDKs do Azure.

## 📌 Passo a Passo para Configuração

### 1️⃣ Criar um Serviço de Pesquisa no Azure

1. Acesse o portal do **Azure** ([portal.azure.com](https://portal.azure.com)).
2. Navegue até **Serviços do Azure** > **Azure AI Services** > **AI Search (Create)**.
3. Defina a **Assinatura**, **Nome do Serviço**, **Grupo de Recursos** e **Região**.
4. Escolha um **Plano de Preços** baseado nas suas necessidades.
5. Clique em **Criar** e aguarde a implantação.

### 2️⃣ Criar um Serviço de AI

1. No portal do **Azure**, acesse **Criar um Recurso** > **IA + Machine Learning** > **Azure AI Service (Criar)**.
2. Defina a **Assinatura**, **Nome do Serviço**, **Grupo de Recursos** e **Região**.
3. Escolha um **Plano de Preços** adequado.
4. Clique em **Examinar + Criar** e aguarde a implantação.

### 3️⃣ Configurar um Índice de Pesquisa

1. No portal do Azure, acesse seu **Serviço de Pesquisa**.
2. Navegue até **Índices** e clique em **Adicionar Índice**.
3. Defina o **Nome do Índice** e configure os **Campos** (chave primária, texto pesquisável, filtros, etc.).
4. Configure **Analisadores de Texto** (padrão, Lucene, Microsoft Language Analyzer, etc.).
5. Salve e publique o índice.

### 4️⃣ Criar uma Conta de Armazenamento

1. No portal do **Azure**, acesse **Criar um Recurso** > **Armazenamento** > **Conta de Armazenamento (Criar)**.
2. Defina a **Assinatura**, **Nome da Conta de Armazenamento**, **Grupo de Recursos** e **Região**.
3. Escolha um **Serviço Primário** adequado.
4. Configure **Desempenho** e **Redundância** conforme suas necessidades.
5. Clique em **Examinar + Criar** e aguarde a implantação.

### 5️⃣ Configurar o Armazenamento de Dados

1. Acesse sua **Conta de Armazenamento** e expanda a opção **Configurações**.
2. Selecione **Configuração** e habilite o **Acesso Anônimo ao Blob**.
3. Navegue até **Armazenamento de Dados** > **Contêiners** > **+ Criar Contêiner**.
4. Defina um **Nome** e escolha **Nível de acesso anônimo** como **Contêiner**.
5. Clique em **Criar** e aguarde a implantação.

### 6️⃣ Consultar os Dados Indexados

Você pode consultar os dados indexados via **REST API** ou SDKs do Azure. Exemplo de requisição usando `curl`:

```sh
curl -X GET "https://{NOME_DO_SERVICO}.search.windows.net/indexes/{NOME_DO_INDICE}/docs?search=exemplo&api-version=2023-07-01" \
-H "Content-Type: application/json" \
-H "api-key: {SUA_API_KEY}"
```

## 🔍 Insights e Aprendizados

- **Facilidade de implementação**: O Azure Cognitive Search reduz a complexidade de criar um sistema de pesquisa robusto.
- **Enriquecimento de Dados com IA**: Recursos como análise de sentimentos e extração de entidades agregam inteligência às buscas.
- **Escalabilidade**: Suporte para grandes volumes de dados, mantendo a performance otimizada.

## 🔗 Ferramentas que se Beneficiam

- **Aplicações Web e Mobile** que necessitam de busca eficiente.
- **E-commerce**, melhorando a descoberta de produtos.
- **Chatbots e Assistentes Virtuais**, enriquecendo interações com respostas mais inteligentes.

---

📌 **Quer contribuir?** Fique à vontade para abrir issues ou enviar PRs!




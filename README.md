# 🚀 Desafio DIO - Azure Speech Studio e Language Studio (com Chatbot)

## 📖 Descrição do Projeto

Este repositório faz parte do desafio prático da [DIO](https://dio.me), com foco no uso das ferramentas **Azure Speech Studio** e **Azure Language Studio**.
O objetivo é aplicar conceitos de análise de fala e linguagem natural, documentar a experiência e compartilhar os resultados de forma estruturada.

---

## 🎯 Objetivos de Aprendizagem

* Aplicar os conceitos aprendidos em um ambiente prático.
* Documentar processos técnicos de forma clara e estruturada.
* Utilizar o GitHub como ferramenta de compartilhamento de documentação técnica.

---

## 🛠️ Tecnologias Utilizadas

* [Microsoft Azure Speech Studio](https://speech.microsoft.com/)
* [Microsoft Azure Language Studio](https://language.cognitive.azure.com/)
* Git e GitHub para versionamento e documentação

---

## 🔧 Atividades Realizadas

### 1️⃣ Criação dos Recursos no Azure Portal

1. Acesse o [Azure Portal](https://portal.azure.com/).
2. Clique em **Criar um recurso**.
3. Pesquise por **Speech** e clique em **Criar**.

   * Preencha **Assinatura**, **Grupo de Recursos** (ou crie um novo), **Região** e **Nome do recurso**.
   * Clique em **Revisar + Criar** e depois em **Criar**.
4. Repita o processo para **Language Service**.

   * Selecione a opção **Language**.
   * Configure os campos da mesma forma (Assinatura, Grupo, Região, Nome).

---

### 2️⃣ Azure Speech Studio

1. Entre em [Speech Studio](https://speech.microsoft.com/).
2. Clique em **Conversão de fala em texto (Speech-to-Text)**.

   * Selecione o recurso criado no Azure.
   * Faça upload de um arquivo de áudio ou grave diretamente.
   * Visualize a transcrição automática.
3. Clique em **Conversão de texto em fala (Text-to-Speech)**.

   * Digite um texto.
   * Escolha uma voz neural e clique em **Reproduzir**.

---

### 3️⃣ Azure Language Studio – Custom Question Answering (QnA)

1. Acesse [Language Studio](https://language.cognitive.azure.com/).
2. Clique em **Criar projeto de Perguntas e Respostas Personalizadas**.
3. Preencha os campos:

   * Nome do projeto.
   * Idioma.
   * Escolha o recurso **Language** criado.
4. Adicione fontes de conhecimento:

   * Upload de arquivos FAQ.
   * Links para páginas da web com perguntas e respostas.
5. Clique em **Salvar e Treinar**.
6. Teste no **Playground**.

---

### 4️⃣ Azure Language Studio – CLU (Conversational Language Understanding)

1. No **Language Studio**, selecione **Conversational Language Understanding**.
2. Clique em **Criar novo projeto**.
3. Preencha:

   * Nome do projeto.
   * Idioma.
   * Selecione o recurso Language.
4. Adicione **Intenções** (ex.: `Saudação`, `AgendarConsulta`).
5. Adicione **Exemplos de frases** para cada intenção.
6. (Opcional) Crie **Entidades** para capturar valores (datas, locais, números).
7. Clique em **Treinar** → **Testar**.

---

### 5️⃣ Orchestration Workflow (Integrando QnA + CLU)

1. Ainda no **Language Studio**, clique em **Criar projeto de Orchestration**.
2. Configure:

   * Nome do projeto.
   * Recurso Language.
3. Dentro do projeto, adicione:

   * **Skill de QnA** (seu projeto Custom QnA).
   * **Skill de CLU** (seu projeto CLU).
4. Clique em **Salvar e Treinar**.
5. Teste no Playground para verificar o roteamento.

---

### 6️⃣ (Opcional) Conectar ao Azure Bot Service

1. Acesse o [Azure Portal](https://portal.azure.com/).
2. Clique em **Criar recurso** → **Web App Bot** ou **Azure Bot**.
3. Configure:

   * Nome.
   * Grupo de recursos.
   * Plano de preços (pode ser gratuito F0).
4. Após criar, vá em **Configurações do Bot** → **Canais**.

   * Adicione **Direct Line Speech** ou **Direct Line**.
   * Copie a chave e o endpoint.
5. Configure um cliente (por exemplo, usando **Bot Framework Emulator** ou um app com **Speech SDK**).

---

## 📂 Estrutura do Repositório

```
/dio-azure-speech-language-lab
   ├── README.md      # documentação principal
   └── insights.md    # anotações e aprendizados adicionais (opcional)
```

---

## 💡 Insights e Aprendizados

* O **Speech Studio** é excelente para transcrição em tempo real e geração de fala natural.
* O **Language Studio** permite criar tanto FAQs (QnA) quanto modelos de intenção (CLU).
* O **Orchestration Workflow** é essencial para unir CLU + QnA, tornando o chatbot mais inteligente.
* Com a integração ao **Azure Bot Service**, o chatbot pode ser usado em **sites, apps ou até integrado ao WhatsApp**.

---

## ✅ Conclusão

Este desafio permitiu explorar ferramentas de IA da Microsoft aplicadas à **voz** e **linguagem natural**, reforçando a importância de documentar e compartilhar os aprendizados.
Com isso, o repositório serve como base de consulta e apoio para estudos futuros.

---

## 📌 Autor

Feito por [Fernado Jarski](https://github.com/Farski96)
Projeto prático da [DIO](https://dio.me)

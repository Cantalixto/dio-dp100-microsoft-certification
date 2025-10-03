# 💬 Chatbot Inteligente com RAG (Retrieval-Augmented Generation) em PDFs

## 📌 Introdução

Este é o segundo projeto prático do **Microsoft Certification Challenge #4 (DP-100) da DIO**.

O objetivo deste desafio é desenvolver um **chatbot interativo** que gera respostas precisas e contextuais, utilizando como base de conhecimento o conteúdo de arquivos **PDF** carregados pelo usuário. Diferente de um modelo de IA genérico, este sistema utiliza técnicas de **Busca Vetorial** e **Geração Aumentada por Recuperação (RAG)** para garantir que as respostas sejam **fundamentadas** unicamente nos documentos fornecidos.

Este projeto simula um assistente virtual ideal para revisão de artigos científicos, documentos técnicos ou qualquer corpus de conhecimento proprietário.

---

## 🎯 Objetivos do Projeto

Este projeto visa atingir os seguintes objetivos técnicos e funcionais:

1.  **Ingestão de Dados PDF:** Implementar um processo para carregar e extrair texto de arquivos PDF.
2.  **Criação de Embeddings:** Utilizar modelos de **NLP** para converter blocos de texto dos PDFs em **vetores numéricos** (embeddings).
3.  **Busca Vetorial:** Criar um **índice vetorial** para armazenar e consultar os embeddings de forma eficiente, permitindo a recuperação rápida dos trechos de texto mais relevantes.
4.  **Geração de Resposta (RAG):** Integrar um **Modelo de Linguagem Grande (LLM)** para receber o trecho de texto recuperado e a pergunta do usuário, e gerar a resposta final e coerente.
5.  **Interface Interativa:** Desenvolver uma interface de chat para que o usuário possa fazer perguntas em tempo real.

---

## 🛠 Tecnologias e Ferramentas

| Categoria | Tecnologia/Ferramenta | Uso no Projeto |
| :--- | :--- | :--- |
| **Linguagem** | Python | Linguagem principal para todo o desenvolvimento. |
| **PDF Processing** | PyPDF2, Tesseract ou similar | Extração de texto dos documentos. |
| **NLP/Embeddings** | Sentence Transformers, OpenAI/Hugging Face APIs | Geração dos vetores de texto. |
| **Busca Vetorial** | FAISS, Pinecone, ChromaDB ou similar | Armazenamento e busca eficiente dos embeddings. |
| **IA Generativa** | OpenAI, LLama (Hugging Face) ou outro LLM | Geração da resposta final a partir do contexto recuperado. |
| **Interface** | Streamlit, Gradio ou Flask | Criação da interface interativa do chatbot. |

---

## 🚀 Arquitetura da Solução (Pipeline RAG)

A solução segue o padrão RAG, que funciona em duas etapas principais:

1.  **Indexação (Offline):**
    * **Carregamento de PDFs** $\rightarrow$ **Extração de Texto** $\rightarrow$ **Criação de Chunks** (divisão do texto em pequenos blocos).
    * Cada *chunk* é transformado em um **Embedding** (vetor) e armazenado no **Índice Vetorial**.

2.  **Consulta (Online):**
    * **Pergunta do Usuário** $\rightarrow$ **Criação de Embedding da Pergunta**.
    * **Busca Vetorial:** O embedding da pergunta é comparado com todos os vetores no Índice, recuperando os **N** *chunks* de texto mais semanticamente próximos.
    * **LLM (Geração):** A pergunta original e os *chunks* recuperados são passados ao LLM, que gera uma resposta **fundamentada** nesse contexto.

---

## 📂 Estrutura do Repositório

```bash
.
├── 02-chatbot-rag-pdfs/
│   ├── inputs/
│   │   └── documentos_tcc.pdf      # Arquivos PDF de exemplo.
│   ├── src/
│   │   ├── document_processor.py   # Script para carregar e criar embeddings.
│   │   └── chatbot_app.py          # Script principal com a lógica RAG e interface.
│   ├── notebooks/
│   │   └── testes_embeddings.ipynb # Notebooks de teste de vetorização.
│   └── README.md                   # Este arquivo.
├── README.md                       # README.md Central do Desafio DP-100.
└── ...

# Agente de RH Inteligente com IA (RAG + LLM)

Aplicação desenvolvida em Python utilizando Streamlit, LangChain, HuggingFace e Groq, que implementa um assistente inteligente de Recursos Humanos capaz de responder perguntas com base em documentos institucionais.

O sistema utiliza a técnica de RAG (Retrieval-Augmented Generation) para combinar busca semântica com modelos de linguagem (LLMs), garantindo respostas mais precisas, contextualizadas e confiáveis.

---

# Sobre o Projeto

O Agente de RH Inteligente foi desenvolvido para simular um assistente virtual capaz de automatizar o atendimento a dúvidas frequentes dentro de um setor de Recursos Humanos.

Em ambientes corporativos, é comum que colaboradores tenham dúvidas recorrentes sobre:

- políticas internas  
- benefícios  
- férias e licenças  
- processos administrativos  

Este projeto resolve esse problema utilizando Inteligência Artificial, permitindo que o usuário faça perguntas em linguagem natural, enquanto o sistema:

1. interpreta a pergunta  
2. busca informações relevantes em documentos  
3. gera uma resposta baseada em contexto real  

---

# Contexto de Negócio

A solução foi aplicada ao setor de Recursos Humanos (RH), responsável por grande parte da comunicação interna nas organizações.

Esse setor concentra demandas como:

- onboarding de colaboradores  
- políticas corporativas  
- gestão de benefícios  
- suporte administrativo  

A proposta do projeto é reduzir a sobrecarga operacional do RH, automatizando respostas para dúvidas repetitivas e melhorando a experiência do colaborador.

---

# Funcionalidades

## Ingestão de Documentos
- Leitura de arquivos PDF  
- Extração automática de texto  

## Processamento de Texto
- Divisão em chunks  
- Preparação para busca semântica  

## Busca Semântica (RAG)
- Geração de embeddings  
- Armazenamento em banco vetorial  
- Recuperação de trechos relevantes  

## Geração de Respostas
- Integração com LLM (Groq)  
- Respostas baseadas em contexto real  

## Interface Interativa
- Aplicação web com Streamlit  
- Perguntas em linguagem natural  
- Respostas em tempo real  

## Exposição
- Deploy local + ngrok  
- Acesso externo via link público  

---

# Interface do Sistema

## Tela Inicial
> <img width="1842" height="561" alt="image" src="https://github.com/user-attachments/assets/99b0f7dd-c185-4c77-8349-133555b2f52d" />

## Pergunta do Usuário
<img width="1833" height="475" alt="image" src="https://github.com/user-attachments/assets/559e4246-c5b4-4980-b626-d9978e5f9e41" />

## Resposta Gerada pela IA
> <img width="1819" height="601" alt="Captura de tela 2026-03-26 113249" src="https://github.com/user-attachments/assets/2c4358dd-90f0-4a79-af02-6f0391d1235e" />
<img width="1839" height="401" alt="Captura de tela 2026-03-26 113257" src="https://github.com/user-attachments/assets/e378fad6-b1e5-4384-877e-49c69f344355" />

---

# Arquitetura da Solução

O projeto utiliza a arquitetura RAG (Retrieval-Augmented Generation).

## Fluxo da Aplicação

1. Carregamento do PDF  
2. Divisão do texto em chunks  
3. Geração de embeddings semânticos  
4. Armazenamento em banco vetorial (ChromaDB)  
5. Recebimento da pergunta  
6. Busca dos trechos mais relevantes  
7. Envio do contexto ao LLM  
8. Geração da resposta final  

---

# Diferenciais do Projeto

- Aplicação prática de IA em contexto real de negócio  
- Uso de arquitetura moderna (RAG)  
- Integração completa de pipeline de dados e IA  
- Uso de LLM de alta performance (Groq)  
- Estrutura escalável e reutilizável  

---

# Como Rodar o Projeto

## Pré-requisitos

- Python 3.x  
- Google Colab  
- Chave de API da Groq  

---

## Instalação das Dependências

```bash
pip install langchain langchain-community langchain-groq langchain-huggingface chromadb pypdf groq pyngrok streamlit

# Configuração da API

Antes de executar o projeto, defina sua chave da API da Groq:

```python
import os
os.environ['GROQ_API_KEY'] = "SUA_CHAVE_AQUI"
```

---

# Execução do Projeto

O notebook gera automaticamente o arquivo principal da aplicação:

```
app.py
```

Para iniciar a interface web com Streamlit, execute:

```bash
streamlit run app.py
```

---

# Exposição com Ngrok

Caso queira acessar a aplicação externamente (fora do seu ambiente local), utilize o ngrok:

```python
from pyngrok import ngrok
ngrok.connect(8501)
```

Após a execução, será gerado um link público para acesso via navegador.

---

# Estrutura do Projeto

```
├── AGENTE_RH.ipynb
├── app.py
```

---

# Descrição dos Arquivos

* **AGENTE_RH.ipynb** → Responsável por toda a pipeline:

  * RAG (Retrieval-Augmented Generation)
  * Geração de embeddings
  * Processamento de documentos
  * Integração com LLM

* **app.py** → Interface web construída com Streamlit para interação com o usuário

---

# Tecnologias Utilizadas

## Linguagem

* Python

## Inteligência Artificial

* LangChain
* Groq (LLM)
* HuggingFace Embeddings

## Processamento e Armazenamento

* ChromaDB (Vector Database)
* PyPDF

## Interface e Deploy

* Streamlit
* ngrok

---

# Desenvolvedor 

Kauê Silva Matheus

## Contato

- LinkedIn: ([https://www.linkedin.com/in/seu-usuario](https://www.linkedin.com/in/kau%C3%AA-matheus-2487b6353/))

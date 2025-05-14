# Chatbot Educacional Personalizado com IA

Um projeto simples de chatbot educacional baseado em inteligência artificial, com integração à API da OpenAI, que responde dúvidas, gera exercícios e sugestões de estudo, e aceita upload de PDFs para fornecer contexto personalizado nas respostas.

---

## ✨ Funcionalidades

- **Responde dúvidas** de alunos sobre conteúdos escolares.
- **Gera explicações alternativas** e exemplos diferentes conforme solicitado.
- **Cria exercícios e quizzes** sob demanda.
- **Sugere materiais complementares** (vídeos, artigos, etc.).
- **Aceita upload de arquivos PDF** (apostilas, resumos, listas), utilizando o conteúdo para contextualizar as respostas.
- **Interface simples** via terminal, web (opcional), Telegram ou WhatsApp.

---

## 🚀 Tecnologias Utilizadas

- [Python 3.8+](https://www.python.org/)
- [openai](https://pypi.org/project/openai/) — API oficial para modelos GPT.
- [tiktoken](https://pypi.org/project/tiktoken/) — contagem de tokens OpenAI.
- [pandas](https://pypi.org/project/pandas/) — manipulação e análise de dados/tabulados.
- [PyPDF2](https://pypi.org/project/PyPDF2/) ou [pdfplumber](https://pypi.org/project/pdfplumber/) — extração de texto de PDFs.
- [Flask](https://pypi.org/project/Flask/) ou [FastAPI](https://pypi.org/project/fastapi/) — backend (opcional).
- [Streamlit](https://pypi.org/project/streamlit/) — prototipagem de interface web (opcional).
- [python-telegram-bot](https://pypi.org/project/python-telegram-bot/) — integração com Telegram (opcional).
- [twilio](https://pypi.org/project/twilio/) — integração com WhatsApp (opcional).

---

## 💡 Como Funciona

1. O usuário envia uma pergunta, faz upload de um PDF ou solicita exercícios.
2. O sistema extrai e processa (com pandas, se necessário) o conteúdo do PDF.
3. Monta um prompt completo, usando o contexto do PDF, e envia para a API da OpenAI.
4. Exibe a resposta gerada ao usuário.

### Exemplos de Uso

- **Dúvida:**  
  > "Explique a Segunda Lei de Newton."  
  O bot utiliza o PDF enviado (apostila de Física) para contextualizar e responde de forma didática.

- **Exercícios:**  
  > "Me envie 3 exercícios sobre equações do 2º grau."  
  O bot gera exercícios e apresenta as respostas.

- **Explicação alternativa:**  
  > "Explique de outro jeito, por favor."  
  O bot reformula de maneira mais simples ou com exemplos diferentes.

---

## 🛠️ Instalação e Execução

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/seu-usuario/chatbot-educacional-ia.git
   cd chatbot-educacional-ia
   ```
2. **Crie um ambiente virtual e instale as dependências:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # ou venv\Scripts\activate no Windows
   pip install -r requirements.txt
   ```
3. **Configure a chave da OpenAI:**
   - Crie um arquivo `.env` e adicione:
     ```
     OPENAI_API_KEY=sk-...
     ```
4. **Execute a aplicação:**
   - Siga as instruções do README para rodar via terminal, web, ou integrar com Telegram/WhatsApp.

---

## 📁 Estrutura Sugerida do Projeto

```
chatbot-educacional-ia/
├── app.py
├── chatbot/
│   ├── openai_client.py
│   ├── pdf_reader.py
│   └── prompts.py
├── requirements.txt
├── README.md
└── .env.example
```

---

## 🗺️ Roadmap Futuro

- [ ] Persistência de histórico e progresso dos alunos.
- [ ] Dashboard para professores.
- [ ] Personalização e gamificação.
- [ ] Análise preditiva de alunos em risco.
- [ ] Processamento avançado de PDFs (OCR, imagens).

---

## 🤝 Colabore

Contribuições são bem-vindas! Fique à vontade para abrir issues ou pull requests.

---

## 📄 Licença

Este projeto está sob a licença MIT.
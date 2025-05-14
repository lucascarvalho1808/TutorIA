# TutorIA — Chatbot Educacional Personalizado com IA

Um projeto simples de chatbot educacional baseado em inteligência artificial, com integração à API da OpenAI, que responde dúvidas, gera exercícios e sugestões de estudo, e aceita upload de PDFs (ou arquivos CSV) para fornecer contexto personalizado nas respostas.

---

## ✨ Funcionalidades

- **Responde dúvidas** de alunos sobre conteúdos escolares.
- **Gera explicações alternativas** e exemplos diferentes conforme solicitado.
- **Cria exercícios e quizzes** sob demanda.
- **Sugere materiais complementares** (vídeos, artigos, etc.).
- **Aceita upload de arquivos PDF ou CSV** (apostilas, resumos, listas), utilizando o conteúdo para contextualizar as respostas.
- **Interface web moderna** via [Streamlit](https://streamlit.io/) para uma experiência amigável e interativa.

---

## 🚀 Tecnologias Utilizadas

- [Python 3.8+](https://www.python.org/)
- [openai](https://pypi.org/project/openai/) — API oficial para modelos GPT.
- [tiktoken](https://pypi.org/project/tiktoken/) — contagem de tokens OpenAI.
- [pandas](https://pypi.org/project/pandas/) — manipulação e análise de dados/tabulados.
- [PyPDF2](https://pypi.org/project/PyPDF2/) ou [pdfplumber](https://pypi.org/project/pdfplumber/) — extração de texto de PDFs.
- [Streamlit](https://pypi.org/project/streamlit/) — interface web moderna e simples.

---

## 💡 Como Funciona

1. O usuário acessa a aplicação via web (Streamlit).
2. O usuário pode enviar uma pergunta, fazer upload de um PDF ou CSV, ou solicitar exercícios.
3. O sistema extrai e processa (com pandas, se necessário) o conteúdo do arquivo enviado.
4. O bot monta um prompt completo, usando o contexto do arquivo, e envia para a API da OpenAI.
5. O bot exibe a resposta gerada na interface web.

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
   git clone https://github.com/seu-usuario/tutoria.git
   cd tutoria
   ```
2. **Crie um ambiente virtual e instale as dependências:**
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # ou .venv\Scripts\activate no Windows
   pip install -r requirements.txt
   ```
3. **Configure a chave da OpenAI:**
   - Crie um arquivo `.env` e adicione:
     ```
     OPENAI_API_KEY=sk-...
     ```
4. **Execute a aplicação Streamlit:**
   ```bash
   streamlit run app.py
   ```

---

## 📁 Estrutura do Projeto

```
.venv/
.env
.gitignore
app.py
arquivo_teste.pdf  # Ou qualquer PDF/CSV como base de dados/contexto
requirements.txt
```

- **app.py**: Código principal da aplicação Streamlit.
- **arquivo_teste.pdf**: Exemplo de arquivo base (pode ser substituído por PDFs).
- **requirements.txt**: Dependências do projeto.
- **.env**: Variáveis de ambiente (API Key da OpenAI).
- **.venv**: Ambiente virtual (não incluir no git).
- **.gitignore**: Arquivos e pastas a serem ignorados no versionamento.

---

## 🗺️ Roadmap Futuro

- [ ] Persistência de histórico e progresso dos alunos.
- [ ] Dashboard para professores.
- [ ] Personalização e gamificação.
- [ ] Análise preditiva de alunos em risco.
- [ ] Processamento avançado de PDFs (OCR, imagens).

---

## 📄 Licença

Este projeto está sob a licença MIT.

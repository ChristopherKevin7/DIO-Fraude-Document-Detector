# Verificador de Veracidade de Cartão de Crédito

Este projeto é uma aplicação desenvolvida como parte do desafio do **Bootcamp Microsoft Certification Challenge #1 - AI 1027** oferecido pela DIO. O objetivo é criar uma solução para verificar a veracidade de cartões de crédito enviados como imagem, utilizando serviços da Microsoft Azure.

## Funcionalidades

- **Upload de imagens**: Suporta arquivos nos formatos `.png`, `.jpg` e `.jpeg`.
- **Armazenamento no Azure Blob Storage**: As imagens são carregadas e armazenadas em um container do Azure.
- **Validação de cartões de crédito**: Utiliza o **Azure Document Intelligence** para analisar os dados e verificar a validade do cartão.
- **Interface intuitiva**: Desenvolvida com **Streamlit**, oferece uma interface amigável e responsiva.

---

## Tecnologias Utilizadas

- **Python**
  - [Streamlit](https://streamlit.io/) para a interface do usuário.
  - [Azure Storage Blob](https://learn.microsoft.com/en-us/azure/storage/blobs/) para upload e armazenamento das imagens.
  - [Azure Document Intelligence](https://learn.microsoft.com/en-us/azure/ai-services/document-intelligence/) para análise de documentos.
- **Azure Cloud**
  - **Blob Storage** para armazenamento de arquivos.
  - **Document Intelligence** para análise dos dados.

---


## Como Executar

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/ChristopherKevin/DIO-Fraude-Document-Detector.git
   cd DIO-Fraude-Document-Detector
    ```

2. **Crie um ambiente virtual e ative-o:**
  ```bash
    python -m venv venv
    # Ativar no Windows
    .\venv\Scripts\activate
    # Ativar no Linux/Mac
    source venv/bin/activate
  ```

3. **Instale as dependências:**

  ```bash
  pip install -r requirements.txt
  ```

4. **Configure suas credenciais no arquivo Config.py:**

  ```bash
  class Config:
    ENDPOINT = "seu-endpoint-do-azure"
    KEY = "sua-chave-do-azure"
    AZURE_STORAGE_CONNECTION_STRING = "Sua connection string do Azure Blob Storage"
    CONTAINER_NAME = "nome-do-container"
  ```
5. **Execute o aplicativo:**

  ```bash
  streamlit run app.py
  ```

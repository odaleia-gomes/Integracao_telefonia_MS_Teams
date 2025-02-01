<<<<<<< HEAD
# ETL para Proposta Técnica - Integração telefonia MS Teams

Este projeto implementa um pipeline ETL (Extração, Transformação e Carga) para processar e estruturar documentos PDF contendo propostas técnicas. O código baixa o documento de um bucket S3, extrai seu conteúdo, processa as seções e converte o conteúdo em um formato JSON estruturado. O JSON resultante é armazenado novamente no S3, facilitando a análise e armazenamento de dados.

## Funcionalidades

- **Extração de Dados**: O arquivo PDF é baixado de um bucket S3 utilizando a biblioteca `boto3`.
- **Transformação de Dados**: O conteúdo do PDF é extraído e dividido em seções lógicas. As seções são processadas para garantir uma estrutura hierárquica e clara.
- **Carga e Armazenamento**: O conteúdo processado é convertido em JSON e salvo de volta no bucket S3 em um diretório de saída específico.

## Como Funciona

1. **Baixar Documento**: O código acessa um bucket S3 e baixa o arquivo PDF usando a chave de acesso e o nome do bucket.
2. **Extrair Texto**: O arquivo PDF é processado para extrair seu texto utilizando uma função dedicada.
3. **Processar Conteúdo**: O texto extraído é segmentado em seções lógicas e processado para estruturar melhor as informações.
4. **Salvar Resultado**: O conteúdo processado é convertido em JSON e armazenado de volta no S3 em um novo diretório, facilitando o acesso e uso posterior.

## Tecnologias Utilizadas

- **Python**: A linguagem principal do projeto.
- **boto3**: Biblioteca para interação com o AWS S3.
- **Tempfile**: Utilizada para criar arquivos temporários durante o processamento.
- **JSON**: Formato usado para armazenar e estruturar os dados.
- **PDFplumber**: Utilizada para extrair texto dos arquivos PDF.

## Fluxo de Processamento

1. O arquivo PDF é baixado de um bucket S3.
2. O texto do PDF é extraído e as seções do conteúdo são identificadas.
3. As seções extraídas são processadas e transformadas em uma estrutura hierárquica.
4. O conteúdo transformado é armazenado no formato JSON em outro diretório do S3.

## Como Usar

### Pré-requisitos

Antes de rodar o código, certifique-se de que as seguintes dependências estão instaladas:

```bash
pip install boto3 pdfplumber
=======
# **ETL - Estruturação do Manual de Atendimento L5**  

Este projeto implementa um pipeline **ETL (Extração, Transformação e Carga)** para estruturar o **Manual de Atendimento L5**, convertendo seu conteúdo para o formato JSON.  

## **Descrição Técnica**  

### **1. Extração de Dados**  
- O código acessa um bucket S3 utilizando **boto3**, a biblioteca da AWS para Python.  
- O arquivo **Manual de Atendimento L5.txt** é lido e carregado na memória.  

### **2. Transformação dos Dados**  
- O conteúdo é processado e estruturado, convertendo seções e tópicos em um formato hierárquico.  
- **NLTK** é utilizado para segmentar o texto em partes lógicas.  
- A biblioteca **json** é usada para serializar os dados em um formato estruturado.  

### **3. Carga e Armazenamento**  
- O JSON resultante é salvo localmente ou pode ser enviado para um bucket S3 para armazenamento e análise futura.  

## **Tecnologias Utilizadas**  
- **Python**  
- **boto3** (para acesso ao S3)  
- **NLTK** (para processamento de texto)  
- **JSON** (para serialização de dados)  
>>>>>>> master

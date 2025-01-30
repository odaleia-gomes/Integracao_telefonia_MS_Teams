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

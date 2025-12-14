# uipath-invoice-pdf-automation
Automação de extração de PDFs de faturas construída com UiPath Document Understanding, processando múltiplos PDFs e exportando dados estruturados para Excel.


📄 ExpoHub Account Invoice Automation Project
Automação de Extração de Faturas em PDF – UiPath
📌 Descrição do Projeto
Este projeto tem como objetivo automatizar a extração de dados de faturas em PDF utilizando o UiPath Document Understanding.
O robô acessa automaticamente todos os arquivos PDF localizados na pasta Invoices, extrai campos específicos das faturas e armazena as informações em um arquivo Excel.
O uso de caminhos relativos garante que a automação funcione corretamente em qualquer máquina, sem necessidade de ajustes manuais.

🎯 Objetivo da Automação
Acessar automaticamente todos os arquivos PDF da pasta Invoices
Classificar e processar as faturas com Document Understanding
Extrair os seguintes campos:
Invoice Number
Billed To
Due Date
Amount Due
Armazenar os dados extraídos em um arquivo Excel

🛠 Tecnologias Utilizadas
UiPath Studio (Windows / VB.NET)
UiPath Document Understanding
UiPath Intelligent OCR
UiPath PDF Activities
Microsoft Excel

📂 Estrutura do Projeto
📁 ExpoHub Account Invoice Automation Project
│
├── 📁 DocumentProcessing
│   ├── Keyword.json
│   └── taxonomy.json
│
├── 📁 Invoices
│   ├── Invoice #1.pdf
│   ├── Invoice #2.pdf
│   ├── Invoice #3.pdf
│   ├── Invoice #4.pdf
│   └── Invoice #5.pdf
│
├── Main.xaml
├── project.json
├── project.uiproj
├── entry-points.json
├── .settings
└── .tmh


📑 Campos Extraídos
Campo
Descrição
Invoice Number
Número único da fatura
Billed To
Cliente ou empresa faturada
Due Date
Data de vencimento da fatura
Amount Due
Valor total a pagar


🔄 Fluxo da Automação
Leitura dos PDFs
O robô obtém automaticamente todos os arquivos PDF da pasta Invoices.
Classificação do Documento
Identifica o documento como fatura usando palavras-chave e taxonomia.
Extração de Dados
Extrai os campos definidos na taxonomia:
Invoice Number
Billed To
Due Date
Amount Due
Validação (Opcional)
Possibilidade de validação humana via Action Center.
Gravação no Excel
Os dados são gravados no Excel, com uma fatura por linha.

📊 Estrutura do Excel de Saída
Invoice Number
Billed To
Due Date
Amount Due
INV-001
ExpoHub
15/08/2025
2.350,00


▶️ Como Executar o Projeto
Abrir o UiPath Studio
Abrir o projeto ExpoHub Account Invoice Automation Project
Colocar os arquivos PDF de faturas na pasta:Invoices
Executar o arquivo Main.xaml
Verificar o Excel gerado com os dados extraídos

🔧 Implementação Técnica (Caminho Relativo)
O caminho da pasta de entrada é resolvido dinamicamente no fluxo:
Directory.GetFiles(Environment.CurrentDirectory & "\Invoices", "*.pdf")
Isso garante:
Portabilidade entre máquinas
Eliminação de caminhos absolutos
Facilidade de manutenção

✅ Pré-requisitos
UiPath Studio instalado
Pacotes instalados:
UiPath.DocumentUnderstanding.ML
UiPath.IntelligentOCR.Activities
UiPath.PDF.Activities
UiPath.Excel.Activities
OCR configurado corretamente
Microsoft Excel (se aplicável)

🚀 Benefícios da Automação
Redução de esforço manual
Extração padronizada de dados
Processamento em massa de PDFs
Maior confiabilidade e precisão
Facilidade de escalar o processo






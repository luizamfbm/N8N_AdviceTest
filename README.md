# N8N_AdviceTest
# n8n Advice Collector Workflow

This project is a simple N8N automation that fetches random pieces of advice from a public API and logs them into a Google Sheets spreadsheet.

## 🛠 What It Does

Every time the workflow runs, it performs the following steps:

1. **Manual Trigger**  
   Starts the workflow manually for testing or demonstration purposes.

2. **HTTP Request**  
   Sends a GET request to the public Advice Slip API:  
   `https://api.adviceslip.com/advice`

3. **Code (JavaScript)**  
   Parses the API response and extracts two pieces of data:
   - `id`: The unique ID of the advice
   - `advice`: The actual advice text  
   Then it structures the output in a format that Google Sheets can understand.

4. **Google Sheets Node**  
   Appends the extracted `id` and `advice` as a new row in a specified spreadsheet, using columns `ID` and `Advice`.

## 📂 Files

- `workflow.json`: Contains the exported N8N workflow.  
  You can import it directly into your N8N instance.

## 📝 How to Use

1. Clone this repo or download the `.json` file.
2. Open your N8N instance.
3. Use the "Import workflow" option and select `workflow.json`.
4. Set up your Google Sheets credentials in N8N (OAuth2).
5. Replace the spreadsheet link with your own (if needed).
6. Click "Execute Workflow" to test it.

## 🔒 Notes

This workflow does not contain sensitive information, but if you're using your own Google Sheets document, make sure to **avoid uploading credentials or access tokens** to a public repo.

---

Feel free to adapt and build on top of this!


# Workflow n8n: Coletor de Conselhos

Este projeto é uma automação simples no N8N que busca conselhos aleatórios de uma API pública e registra os dados em uma planilha do Google Sheets.

## 🛠 O que esse workflow faz

Sempre que o workflow é executado, ele segue os seguintes passos:

1. **Disparo Manual**  
   Inicia o workflow manualmente, ideal para testes e demonstrações.

2. **Requisição HTTP**  
   Faz uma requisição GET para a API pública:  
   `https://api.adviceslip.com/advice`

3. **Código (JavaScript)**  
   Interpreta a resposta da API e extrai duas informações:
   - `id`: O ID único do conselho
   - `advice`: O texto do conselho  
   Em seguida, organiza os dados em um formato compatível com o Google Sheets.

4. **Google Sheets**  
   Adiciona uma nova linha à planilha informada, preenchendo as colunas `ID` e `Advice` com os dados extraídos.

## 📂 Arquivos

- `workflow.json`: Contém o workflow exportado do N8N.  
  Pode ser importado diretamente em uma instância do N8N.

## 📝 Como usar

1. Clone este repositório ou baixe o arquivo `.json`.
2. Acesse sua instância do N8N.
3. Use a opção “Importar workflow” e selecione `workflow.json`.
4. Configure suas credenciais do Google Sheets no N8N (OAuth2).
5. Substitua o link da planilha pelo seu, se necessário.
6. Clique em “Executar workflow” para testar.

## 🔒 Observações

Este workflow não contém informações sensíveis. Ainda assim, se você estiver usando sua própria planilha do Google, evite subir **credenciais ou tokens de acesso** em repositórios públicos.

---

Sinta-se à vontade para adaptar e expandir esse projeto!


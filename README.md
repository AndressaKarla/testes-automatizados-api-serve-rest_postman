---
# :test_tube: Projeto de Testes Funcionais Automatizados de API REST | Postman | Javascript | JSON Schema | Newman | GitHub Actions | GitHub Pages | Azure Pipelines
[![Badge ServeRest](https://img.shields.io/badge/API-ServeRest-green)](https://github.com/ServeRest/ServeRest/)
---
# :information_source: Introdução 
Este projeto "testes-automatizados-api-serve-rest_postman" é executado em um ambiente de produção na ["API REST"](https://serverest.dev) do ["ServeRest"](https://github.com/ServeRest) que simula uma loja virtual, nos Sistemas Operacionais Windows 11 e Linux Ubuntu 22.04, com o objetivo de praticar ainda mais validações de testes de API REST (Ex.: JSON Schema, geração de massa de dados dinâmicos, etc) em Postman, Javascript, Newman, GitHub Actions, GitHub Pages e Azure Pipelines.

---
# :warning: _Instruções considerando Windows 11, para outras versões do Windows ou outros sistemas operacionais talvez seja necessário algumas adaptações_ 

# :dart: Executar testes automatizados e Gerar os resultados dos testes no GitHub Actions, GitHub Pages e nas pipelines do Azure DevOps
## :triangular_flag_on_post: Executar com Newman testes automatizados de API REST da collection e environment do Postman em um ambiente de produção, Gerar os resultados dos testes no GitHub Actions; GitHub Pages e nas pipelines do Azure DevOps (apenas na branch principal (main))
- Neste repositório, acessar a aba "Actions"
- Na seção "Actions", clicar em "Pipeline Testes Automatizados API ServeRest Postman Newman" << PAREI AQUI
- Em "This workflow has a workflow_dispatch event trigger.", clicar em "Run workflow" > "Run workflow" para executar com Newman testes automatizados de API REST da collection e environment do Postman com um tempo de espera de 2 ms entre as requisições em um ambiente de produção no GitHub Actions
- Após o término da execução, clicar na run "Pipeline Testes Automatizados API ServeRest Postman Newman"
- Na seção "Artifacts", clicar em "postman-reports-html-junit-xml-newman"
- Na janela aberta, escolher um diretório para baixar a(s) pasta(s) compactada(s) "postman-reports-html-junit-xml-newman.zip"

# :mag_right: Verificar o report html gerado anteriormente no GitHub Pages (apenas na branch principal (main))
- Neste repositório, acessar a [url](https://andressakarla.github.io/testes-automatizados-api-serve-rest_postman/postman-api-serve-rest-report-htmlextra-newman.html) abaixo da seção "About" 
- No report html gerado no GitHub Pages (configurado na aba "Settings" deste repositório > "Pages" > "Build and deployment" > "Source = GitHub Actions") e aberto anteriormente, clicar em "Total Requests", em "CAMPOS INFORMADOS CORRETAMENTE / ...", "CAMPOS INFORMADOS INCORRETAMENTE / ...", etc ir clicando em "<" para ir expandindo, e ir clicando em "<" de cada "Iteration" para verificar mais detalhes de "TEST PASS PERCENTAGE", "REQUEST BODY", "RESPONSE BODY", "TEST INFORMATION", etc

# :mag_right: Verificar no navegador padrão o report html gerado e armazenado anteriormente no GitHub Actions e descompactado no computador 
- No Windows 11, abrir uma janela do "Explorador de Arquivos"
- Acessar o diretório onde foi baixada a pasta compactada "postman-reports-html-junit-xml-newman.zip" anteriormente
- Descompactar a pasta
- Acessar a pasta descompactada "postman-reports-html-junit-xml-newman"
- Clicar 2 vezes sob o report "postman-api-serve-rest-report-htmlextra-newman.html" gerado e armazenado anteriormente no GitHub Actions e descompactado para ser aberto e verificado no navegador padrão no computador

# :mag_right: Verificar na funcionalidade "XML Viewer" do site "Code Beautify" o report xml gerado e armazenado anteriormente no GitHub Actions, utilizado nas pipelines do Azure DevOps (apenas na branch principal (main)) e descompactado no computador 
- Abrir uma janela do "Explorador de Arquivos"
- Acessar o diretório onde foi descompactada a pasta "postman-reports-html-junit-xml-newman"
- Copiar este diretório 
- Acessar a funcionalidade "[XML Viewer](https://codebeautify.org/xmlviewer)" do site "Code Beautify"
- Clicar em "File"
- Informar o diretório copiado anteriormente

Ex.: 
> C:\Users\usuario\Downloads\postman-reports-html-junit-xml-newman

- Realizar o upload do report "postman-api-serve-rest-report-junit-xml-newman.xml" gerado e armazenado anteriormente no GitHub Actions, utilizado nas pipelines do Azure DevOps e descompactado para ser verificado na seção "Output" da funcionalidade "XML Viewer" do site "Code Beautify"

---
# :warning: Antes de clonar ou executar este projeto localmente no computador, é necessário seguir as instruções abaixo :point_down:

## :hammer_and_wrench: Instalar algumas dependências necessárias 
### Janela do "Explorador de Arquivos" > "Visualizar" > "Mostrar" e marcar algumas opções
- No Windows 11, abrir uma janela do "Explorador de Arquivos"
- Clicar em "Visualizar" > "Mostrar"
- Clicar em "Extensões de nomes de arquivos" 
- Clicar em "Itens ocultos"

### Baixar e instalar o git e gitbash; configurar o git
- Caso ainda não tenha o git e gitbash baixado e instalado, acessar o link do [git e gitbash](https://git-scm.com/download/win), baixar e instalar como administrador
- Caso ainda não tenha configurado o git, seguir os passos apresentados neste link ["Configure a ferramenta"](https://training.github.com/downloads/pt_BR/github-git-cheat-sheet/#:~:text=Configure%20a%20ferramenta) e configurar

### Desinstalar completamente Node.js e npm que já foram instalados em algum outro momento 
- Seguir os passos apresentados neste [link](https://www.google.com/search?q=desinstalar+completamente+nodejs+e+res%C3%ADduos+windows+11+pt-br+sem+programas+terceiros)
  
### Node versão 18.12.1
- Baixar e instalar o [node v18.12.1](https://nodejs.org/dist/v18.12.1/) > node-v18.12.1-x64.msi
- Abrir um novo gitbash ou outro terminal  
- Informar o comando abaixo para confirmar se o node realmente foi instalado
```
node --version
```
- Verificar se foi retornada a mesma versão do node instalada anteriormente:
> v18.12.1
- Informar o comando abaixo para confirmar se o npm realmente foi instalado
```
npm --version
```
- E verificar se foi retornada essa mesma versão do npm:
> 8.19.2
- Fechar este gitbash ou terminal

### Newman
- Abrir um novo gitbash 
- Informar o comando abaixo para instalar o newman globalmente
```
npm install -g newman
```
- Informar o comando abaixo para verificar se foi retornada alguma versão e confirmar se o newman realmente foi instalado
```
newman --version
```
- Fechar este gitbash

### Newman reporter htmlextra
- Abrir um novo gitbash 
- Informar o comando abaixo para instalar o newman-reporter-htmlextra globalmente
```
npm install -g newman-reporter-htmlextra
```
- Informar o comando abaixo para verificar se foi retornada alguma versão e confirmar se o newman-reporter-htmlextra realmente foi instalado
```
newman-reporter-htmlextra --version
```
- Fechar este gitbash 

---
# :hammer_and_wrench: Clonar o projeto
- Abrir uma janela do "Explorador de Arquivos"
- Acessar o diretório onde será clonado o projeto "testes-automatizados-api-serve-rest_postman"
- Copiar este diretório 
- Abrir um novo gitbash 
- Informar o comando abaixo para acessar onde será clonado o projeto
> cd "<diretório\copiado\anteriormente>"

Ex.: 
```
cd "C:\Projetos\Automação"
```
- Informar o comando abaixo para clonar este repositório via "HTTPS"

```
git clone https://github.com/AndressaKarla/testes-automatizados-api-serve-rest_postman.git
```

- Ou informar o comando abaixo para clonar este repositório via "SSH"

```
git clone git@github.com:AndressaKarla/testes-automatizados-api-serve-rest_postman.git
```

# :hammer_and_wrench: Instalar as extensões no Visual Studio Code (VS Code)
- Caso ainda não tenha o VS Code baixado e instalado, acessar o site do [Visual Studio Code](https://code.visualstudio.com/download), baixar e instalar com a opção "System Installer"
- Com o Visual Studio Code aberto, caso seja apresentado alguma mensagem de "Instalar pacote de idiomas ...", clicar no ícone de configurações > "Don't Show Again"
- Clicar em "Manage" > "Profiles" > "Create Profile"
- Em "Profile name", informar "Postman"
- Clicar em "Create"
- Clicar em "Extensions", informar e instalar as extensões abaixo:
  - Hyper Term Theme
    - HasseNasse
      - Clicar em "Hyper Term Black" apresentada para habilitar a extensão
  - Material Icon Theme
    - Philipp Kief
      - Clicar em "Material Icon Theme" apresentada para habilitar a extensão 
- Fechar o VS Code

# :bookmark_tabs: Abrir o VS Code diretamente na pasta do projeto "testes-automatizados-api-serve-rest_postman" 
- No gitbash aberto anteriormente, informar o comando abaixo para abrir o VS Code diretamente na pasta do projeto "testes-automatizados-api-serve-rest_postman"
```
code .
```
- Aguardar o VS Code ser aberto
- Fechar este gitbash
- No VS Code aberto, caso seja apresentado "Do you trust the authors on the files in this folder?", marcar "Trust the authors of all files in the parent folder ...."
  - Clicar em "Yes, I trust the authors ...."

---
# :dart: Executar testes automatizados e Gerar os resultados dos testes no computador
## :triangular_flag_on_post: Executar com Newman testes automatizados de API REST da collection e environment do Postman em um ambiente de produção e Gerar report diretamente no terminal no computador
- Abrir uma janela do "Explorador de Arquivos"
- Acessar o diretório onde foi clonado o projeto “testes-automatizados-api-serve-rest_postman”
- Copiar este diretório 
- Abrir um novo gitbash
- Informar o comando abaixo para acessar o projeto "testes-automatizados-api-serve-rest_postman"
> cd "<diretório\copiado\anteriormente>"

Ex.: 
```
cd "C:\Projetos\Automação\testes-automatizados-api-serve-rest_postman"
```

- Informar o comando abaixo para executar com Newman testes automatizados de API REST da collection e environment do Postman com um tempo de espera de 2 ms entre as requisições em um ambiente de produção e Gerar report diretamente no terminal
```
newman run ./nome-collection.json -e ./nome-environment.json --delay-request 2
```
Ex.: 
```
newman run ./api-serve-rest_collection.json -e ./api-serve-rest_prod-environment.json --delay-request 2
```

## :triangular_flag_on_post: Executar com Newman testes automatizados de API REST da collection e environment do Postman em um ambiente de produção e Gerar os resultados dos testes na pasta "reports" no computador
- No gitbash aberto anteriormente, informar o comando abaixo para executar com Newman testes automatizados de API REST da collection e environment do Postman com um tempo de espera de 2 ms entre as requisições em um ambiente de produção (mesmo comando que é utilizado no "Passo 4" da "Pipeline Testes Automatizados API ServeRest Postman Newman" em ".github > workflows > [workflow-testes-automatizados-api-serve-rest-postman-newman.yml](./.github/workflows/workflow-testes-automatizados-api-serve-rest-postman-newman.yml)" no GitHub Actions e mesmo comando que é utilizado em um dos steps de "[azure-pipelines.yml](./azure-pipelines.yml)" nas pipelines do Azure DevOps) e Gerar reports html e xml na pasta "reports" no computador
```
newman run ./nome-collection.json -e ./nome-environment.json --delay-request 2 --reporters cli,htmlextra,junit --reporter-htmlextra-export ./reports/nome-report-htmlextra.html --reporter-junit-export ./reports/nome-report-junit-xml.xml
```
Ex.: 
```
newman run ./api-serve-rest_collection.json -e ./api-serve-rest_prod-environment.json --delay-request 2 --reporters cli,htmlextra,junit --reporter-htmlextra-export ./reports/postman-api-serve-rest-report-htmlextra-newman.html --reporter-junit-export ./reports/postman-api-serve-rest-report-junit-xml-newman.xml
```
 
---
# :mag_right: Verificar os resultados das execuções dos testes automatizados de API REST no computador 
## :bookmark_tabs: Report html no computador
- No VS Code aberto anteriormente, acessar "reports" 
- Clicar com botão direito do mouse sob o report "postman-api-serve-rest-report-htmlextra-newman.html" > "Reveal in File Explorer" 
- Na janela do "Explorador de Arquivos" aberta automaticamente, clicar 2 vezes sob o report "postman-api-serve-rest-report-htmlextra-newman.html" 
- No report html aberto anteriormente no navegador padrão no computador, clicar em "Total Requests", em "CAMPOS INFORMADOS CORRETAMENTE / ...", "CAMPOS INFORMADOS INCORRETAMENTE / ...", etc ir clicando em "<" para ir expandindo, e ir clicando em "<" de cada "Iteration" para verificar mais detalhes de "TEST PASS PERCENTAGE", "REQUEST BODY", "RESPONSE BODY", "TEST INFORMATION", etc  

## :bookmark_tabs: Report xml no computador 
- No VS Code aberto anteriormente, acessar "reports"
- Clicar com botão direito do mouse sob o report "postman-api-serve-rest-report-junit-xml-newman.xml" > "Reveal in File Explorer"
- Na janela do "Explorador de Arquivos" aberta automaticamente, copiar este diretório
- Acessar a funcionalidade "[XML Viewer](https://codebeautify.org/xmlviewer)" do site "Code Beautify"
- Clicar em "File"
- Informar o diretório copiado anteriormente

Ex.: 
```
C:\Projetos\Automação\testes-automatizados-api-serve-rest_postman\reports
```

- Realizar o upload do report "postman-api-serve-rest-report-junit-xml-newman.xml" gerado e armazenado anteriormente no computador, utilizado nas pipelines do Azure DevOps e descompactado para ser verificado na seção "Output" da funcionalidade "XML Viewer" do site "Code Beautify"

---
### Feito com ❤️ por Andressa Karla :wave: 

### [![Medium](https://img.shields.io/badge/-Medium-595D60?style=plastic&logo=Medium&logoColor=white&link=https://medium.com/@andressakarla)](https://medium.com/@andressakarla) [![Linkedin](https://img.shields.io/badge/-LinkedIn-595D60?style=plastic&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/andressakarla/)](https://www.linkedin.com/in/andressakarla/)

---

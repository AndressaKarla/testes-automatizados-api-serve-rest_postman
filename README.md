---
# Projeto de Testes Funcionais Automatizados de API REST | Postman | Javascript | JSON Schema | Newman | GitHub Actions | GitHub Pages :test_tube:
---
# :information_source: Introdução 
Esse projeto "testes-automatizados-api-serve-rest_postman" é executado em um ambiente de produção na ["API REST"](https://serverest.dev) do ["ServeRest"](https://github.com/ServeRest) que simula uma loja virtual, com o objetivo de praticar ainda mais validações de testes de API (Ex.: JSON Schema, geração de massa de dados dinâmicos, etc) em Postman, Javascript, Newman, GitHub Actions e GitHub Pages.

---
# :dart: Executar com Newman testes automatizados de API REST da collection e environment do Postman, Gerar e armazenar report html no GitHub Actions 
- Nesse repositório, acessar a aba "Actions"
- Na seção "Actions", clicar em "Pipeline Testes Automatizados API ServeRest Postman Newman"
- Em "This workflow has a workflow_dispatch event trigger.", clicar em "Run workflow" > "Run workflow" para executar com Newman testes automatizados de API REST da collection e environment do Postman com um tempo de espera de 2 ms entre as requisições, gerar e armazenar report html no GitHub Actions
- Após o término da execução, clicar na run "Pipeline Testes Automatizados API ServeRest Postman Newman"
- Na seção "Artifacts", clicar em "postman-api-serve-rest-report-html-newman"
- Na janela aberta, escolher um diretório para baixar a pasta compactada "postman-api-serve-rest-report-html-newman.zip"

# :mag_right: Verificar no navegador padrão o report html gerado e armazenado anteriormente no GitHub Actions e descompactado no computador 
- Abrir uma janela do "Windows Explorer"
- Acessar o diretório onde foi baixada a pasta compactada "postman-api-serve-rest-report-html-newman.zip" anteriormente
- Descompactar a pasta
- Acessar a pasta descompactada "postman-api-serve-rest-report-html-newman"
- Clicar 2 vezes sob o report "postman-api-serve-rest-report-htmlextra-newman.html" gerado e armazenado anteriormente no GitHub Actions e descompactado para ser aberto e verificado no navegador padrão no computador

---
# Antes de clonar ou executar esse projeto localmente no computador, é necessário seguir as instruções abaixo :point_down:
## :hammer_and_wrench: Janela do "Windows Explorer" > aba "Exibir" e marcar algumas opções
- Abrir uma janela do "Windows Explorer"
- Clicar na aba "Exibir" 
- Marcar a opção "Extensões de nomes de arquivos"
- Marcar a opção "Itens ocultos"

## :hammer_and_wrench: Baixar e instalar o git e gitbash; configurar o git
- Caso ainda não tenha o git e gitbash baixado e instalado, acessar o link do [git e gitbash](https://git-scm.com/download/win), baixar e instalar
- Caso ainda não tenha configurado o git, seguir os passos apresentados nesse link [Configure a ferramenta](https://training.github.com/downloads/pt_BR/github-git-cheat-sheet/#:~:text=Configure%20a%20ferramenta) e configurar

## :hammer_and_wrench: Instalar as dependências necessárias 
### Desinstalar completamente Node.js e npm que já foram instalados em algum outro momento
- Seguir os passos apresentados nesse link ["COMO REMOVER COMPLETAMENTE O NODE.JS DO WINDOWS?"](https://acervolima.com/como-remover-completamente-o-node-js-do-windows/#:~:text=Pesquise%20por%20programa%20e%20recursos,js%20e%20desinstale-o.)
  
### Node versão 18.12.1
- Baixar e instalar o [node v18.12.1](https://nodejs.org/dist/v18.12.1/) > node-v18.12.1-x64.msi
- Abrir um novo gitbash ou outro terminal de preferência
- Informar o comando abaixo para confirmar se o node realmente foi instalado
```
node --version
```
- Verificar se foi retornada a mesma versão do node instalada anteriormente:
```
v18.12.1
```
- Informar o comando abaixo para confirmar se o npm realmente foi instalado
```
npm --version
```
- E verificar se foi retornada essa mesma versão do npm:
```
8.19.2
```

### newman
- No gitbash ou terminal aberto anteriormente, informar o comando abaixo para instalar o newman
```
npm install -g newman
```
- Informar o comando abaixo para verificar se foi retornada alguma versão e confirmar se o newman realmente foi instalado
```
newman --version
```

### newman-reporter-htmlextra
- No gitbash ou terminal aberto anteriormente, informar o comando abaixo para instalar o newman-reporter-htmlextra
```
npm install -g newman-reporter-htmlextra
```
- Informar o comando abaixo para verificar se foi retornada alguma versão e confirmar se o newman-reporter-htmlextra realmente foi instalado
```
newman-reporter-htmlextra --version
```
- Fechar esse gitbash ou terminal

---
# :hammer_and_wrench: Clonar o projeto
- Abrir uma janela do "Windows Explorer"
- Acessar o diretório onde será clonado o projeto "testes-automatizados-api-serve-rest_postman"
- Copiar esse diretório 
- Abrir um novo gitbash 
- Informar o comando abaixo para acessar onde será clonado o projeto
```
cd "<diretório copiado anteriormente>"
```
Ex.: 
```
cd "C:\PROJETOS\Automação\Postman"
```
- Informar o comando abaixo para clonar este repositório via "HTTPS"
```
git clone https://github.com/AndressaKarla/testes-automatizados-api-serve-rest_postman.git
```
- Ou informar o comando abaixo para clonar este repositório via "SSH"
```
git clone git@github.com:AndressaKarla/testes-automatizados-api-serve-rest_postman.git
```

---
# :dart: Executar com Newman testes automatizados de API REST da collection e environment do Postman e Gerar report diretamente no terminal no computador
- Informar o comando abaixo para acessar o projeto “testes-automatizados-api-serve-rest_postman” clonado anteriormente
```
cd testes-automatizados-api-serve-rest_postman
```
Ex.: 
```
C:\PROJETOS\Automação\Postman\testes-automatizados-api-serve-rest_postman
```
- Informar o comando abaixo para executar com Newman testes automatizados de API REST da collection e environment do Postman com um tempo de espera de 2 ms entre as requisições e Gerar report diretamente no terminal
```
newman run ./nome-collection.json -e ./nome-environment.json --delay-request 2
```
Ex.: 
```
newman run ./api-serve-rest_collection.json -e ./api-serve-rest_prod-environment.json --delay-request 2
```

# :dart: Executar com Newman testes automatizados de API REST da collection e environment do Postman e Gerar report html na pasta "reports" no computador
- No gitbash aberto anteriormente, informar o comando abaixo para executar com Newman testes automatizados de API REST da collection e environment do Postman com um tempo de espera de 2 ms entre as requisições e Gerar report html na pasta "reports" no computador (mesmo comando que é utilizado no "Passo 4" da "Pipeline Testes Automatizados API ServeRest Postman Newman" em ".github > workflows > [workflow-testes-automatizados-api-serve-rest-postman-newman.yml](https://github.com/AndressaKarla/testes-automatizados-api-serve-rest_postman/blob/main/.github/workflows/workflow-testes-automatizados-api-serve-rest-postman-newman.yml)" no GitHub Actions)
```
newman run ./nome-collection.json -e ./nome-environment.json --delay-request 2 --reporters cli, -r htmlextra --reporter-htmlextra-export ./reports/nome-report.html
```
Ex.: 
```
newman run ./api-serve-rest_collection.json -e ./api-serve-rest_prod-environment.json --delay-request 2 --reporters cli, -r htmlextra --reporter-htmlextra-export ./reports/postman-api-serve-rest-report-htmlextra-newman.html
```

---
# :hammer_and_wrench: Instalar as extensões no Visual Studio Code (VS Code)
- Caso ainda não tenha o VS Code baixado e instalado, acessar o site do [Visual Studio Code](https://code.visualstudio.com/download), baixar e instalar com a opção "System Installer"
- Com o Visual Studio Code aberto, caso seja apresentado alguma mensagem de "Instalar pacote de idiomas ...", clicar no ícone de configurações > "Don't Show Again"
- Clicar na opção "Manage > Profiles > Create Profile"
- Em "Profile name", informar "Postman"
- Clicar na opção "Create"
- Clicar na opção "Extensions", informar e instalar as extensões abaixo:
  - Hyper Term Theme
	- HasseNasse
   		- Clicar na opção "Hyper Term Black" apresentada para habilitar a extensão
  - Material Icon Theme
  	- Philipp Kief
		- Clicar na opção "Material Icon Theme" apresentada para habilitar a extensão 
- Fechar o VS Code
    
## :bookmark_tabs: Abrir o VS Code diretamente na pasta do projeto "testes-automatizados-api-serve-rest_postman"
- No gitbash aberto anteriormente, informar o comando abaixo para abrir o VS Code diretamente na pasta do projeto "testes-automatizados-api-serve-rest_postman"
```
code .
```
- Aguardar o VS Code ser aberto
- No VS Code aberto, caso seja apresentado "Do you trust the authors on the files in this folder?", marcar a opção "Trust the authors of all files in the parent folder ...."
	- Clicar no botão "Yes, I trust the authors ...."
   
---
# :mag_right: Verificar no navegador padrão o report html gerado e armazenado na pasta "reports" anteriormente no computador 
## :bookmark_tabs: Report html no computador
- No VS Code aberto anteriormente, acessar "reports > postman-api-serve-rest-report-htmlextra-newman.html" 
- Clicar com botão direito do mouse sob o arquivo "postman-api-serve-rest-report-htmlextra-newman.html" > "Reveal in File Explorer" 
- Na janela do "Windows Explorer" aberta automaticamente, clicar 2 vezes sob o arquivo "postman-api-serve-rest-report-htmlextra-newman.html" gerado e armazenado anteriormente no computador para ser aberto e verificado no navegador padrão

---
### Feito com ❤️ por Andressa Karla :wave: 

### [![Medium](https://img.shields.io/badge/-Medium-595D60?style=plastic&logo=Medium&logoColor=white&link=https://medium.com/@andressakarla)](https://medium.com/@andressakarla) [![Linkedin](https://img.shields.io/badge/-LinkedIn-595D60?style=plastic&logo=Linkedin&logoColor=white&link=https://www.linkedin.com/in/andressakarla/)](https://www.linkedin.com/in/andressakarla/)

---
